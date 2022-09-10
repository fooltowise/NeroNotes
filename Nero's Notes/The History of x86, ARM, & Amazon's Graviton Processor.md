# The History of x86, ARM, & Amazon's Graviton Processor

by #InPractise 

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### Liz, can you share some context about Honeycombs' business, their customer base and the problems you're trying to solve?

Honeycomb is a software-as-a-service observability company. We enable our clients to export telemetry data from their running services, then analyze that to enable them to understand where their service is slow and for whom, and to debug it and get their services and customers back on track again. That essentially means we are in the big data space, ingesting millions of data points per second and querying billions of rows to answer questions our customers have about what their customers are doing in their systems.

### So you compete with Datadog, Splunk and New Relic?

Yes, that's correct, and we jokingly call them New Splunk Dog. They're the older generation of APM and monitoring tools who have rebranded to observability, but we also consider a modern competitor to be Lightstep which was acquired by ServiceNow. There are some newer generation companies, such as Aspecto, who are also emerging.

### What is the potential advantage Honeycomb has over those older legacy APMs?

The primary difference relates to the data analysis capability and user experience. We can answer questions you did not predict in advance, whereas older platforms rely on you deciding in advance which dimensions you want to group on. I know for instance in Datadog, I want to group by host or service name, but if something is an issue with the host name, user and build ID, Datadog has a hard time answering because those weren't aggregated together. Datadog actually has an ebook on tagging practices, encouraging the reduction of tags used. It basically boils down to the flexibility of the platform, as well as how quickly you can answer those questions. Suppose Datadog did support it or you were paying for the tags at Datadog, can you get those answers within 10 seconds, not five minutes. The differentiation is flexibility and speed. We will discuss later why we care about the performance of our software.

### Which cloud providers did Honeycomb use, historically?

Honeycomb was founded in late 2015, came out of stealth in 2016 and hit product market fit in 2017, 2018. Honeycomb was originally built on AWS because the founders were familiar with that solution and it was about safety at the time. In 2019, within my first six months at the company, we spent some time investigating what it would take to potentially change cloud providers, but we decided to rather stay on Amazon.

### Why?

There had to be a major benefit to performing a switch. Once you're established in a cloud, either you have to see significantly better performance on another cloud, or have better access to your customers or a similar dimension. Fundamentally, it's a matter of data gravity for us. Cloud providers will charge you significant amounts of money to egress to another cloud and it can get quite expensive at scale. Cloud providers will charge much less to egress to another customer who's running inside the same cloud. The majority of our clients are on Amazon, and as a result, we didn't want to change clouds to save a buck, then have our customers spend 7 to 9 cents per gigabyte to egress to us. That would have shot our business in the foot.

### How much does it cost to switch from AWS, for example?

When we're talking about the volume of data a Honeycomb customer sends, we estimate one payload they send us is one kilobyte, and 2.5 million data points per second is effectively many gigabytes per second. So every second, instead of racking up a bill of 1 cent per gigabyte, you're racking up a fee that's nine times as much. If we have a client running who is currently in Google cloud spending $300,000 a year on Honeycomb, they might wind up spending another $20,000 a year in egress fees to transmit that telemetry to us. That might be a rounding fee if they are a customer-facing business already egressing significant traffic over the internet, and they may deem it a worthwhile investment, but it's an additional factor. That may push us in future to offer a version of our platform hosted on GCP, for people who are on GCP to write to, but again, the majority of our clientele are on Amazon. We wouldn't want to suddenly impose that cost on our customers. That's why we chose to stay on Amazon, even though in 2019, we did some math which said although Google cloud might be 20% or 30% cheaper, it would harm our customers, which is something we don't want to happen.

### If someone on AWS were to switch to Azure or GCP, what would the egress fees be?

It depends on the nature of the business. We are a big data company whose clientele are other companies using cloud services, which is why the data gravity of our clients matters. Another company in our cohort cares about the data gravity of their customers, but if you are primarily serving consumers over the internet, you're going to be paying 7 to 9 cents per gigabyte or lower if you've negotiated a bulk discount, to egress your images or other payloads to the internet, unless you're going through a CDN. Consumer-facing companies don't care which cloud they're located in, but software-as-a-services companies doing big data problems, care about making sure they're co-located with the majority of their customers.

### Will any non-SaaS business still pay a huge sum to switch clouds?

It depends where their providers are located and how much you're paying to talk to them, versus how much you're paying regardless to talk to consumers on the public internet. I say this as someone who worked at GCP before; there are certain technical reasons why GCP might be a better cloud for you. Google has advantages in machine learning workloads where some people have gone multi cloud to avail themselves of Google's machine learning, but they keep the majority of their serving in Amazon. There are situations where you would want to mix and match to avail the improved network capabilities on GCP or lower compute costs.

### What is it about GCP that is unique compared to the other cloud providers?

> Taking off my Honeycomb hat and putting on my former GCP employee hat, there are things that GCP does better than the competition. GCP offers you the capability of using Google's world class networking set up and capabilities. Google has lower latency and higher throughput than Amazon or Microsoft. Google pioneered and innovated TensorFlow TPUs, and there are also ideological reasons. Walmart refuse to do business with companies hosted on AWS, which subsidizes their biggest competitor.

### Is it that they have data centers and the experience of running Google Search?

You can reach consumers on the same internet backbone Google web search uses.

### Is that much quicker than AWS?

It's not necessarily quicker, but it is more predictable in the tail latencies

### Is the TensorFlow ML linked to data usage and the advertising algorithms they use?

I don't know to what extent TPUs are used in AdWords, but they were originally developed to assist with Google voice search. Their first use case was being able to rapidly ingest voice samples at scale and figure out what you are saying, to deliver a result to you. Google opened that up for anyone to use through Google Cloud, where you can rent TPUs. Google open sourced TensorFlow to get people using the right SDKs to use their technology. Today, TensorFlow can work with Trainium and GPUs, but it is optimized to run workloads on Google's machine learning infrastructure. Honeycomb does not use any neural network machine learning, so that is outside of my practical knowledge as a user, but I did learn about it when I was a customer reliability engineer on Google Cloud.

### How important is TensorFlow ML for winning cloud market share in future?

It is a key differentiator to cause someone to pick Google cloud over another. That is one of the areas in which they have a large market advantage. A lot of other forces are against Google. They are the smaller of the clouds and have a habit of canceling services. They canceled cloud IoT yesterday. When looking for reasons to go with Google cloud originally, I would have said they offer lower prices than Amazon, but for reasons we'll get into very soon, Google has lost that advantage which is unfortunate. That means that, essentially, its data analysis and machine learning capabilities are what's keeping it in the game at this point.

### So let's move on to Graviton. Can you explain to us non techies, what we need to understand about the major differences between the ARM and X86 architecture?

Here is the brief history lesson I give to people who are trying to understand why Intel and AMD are suddenly in danger. In the 80s and 90s, there were a variety of processor manufacturers to choose from, and software developers supported them all because there was no clear consensus on who the winner would be. In the late 90s and early 2000s, everything concentrated on X86 processors made by Intel mostly and by AMD secondarily. We noticed this happening when that consolidation peaked when Apple decided to stop using Motorola processors and only use Intel. That was a brief moment where everyone thought there was a clear winner; everyone would use the same chips which would be X86. Nobody could have foreseen the competing pressure from mobile phones. X86 may have won on the desktop and server, but it was wholly unsuited to running in the mobile phone environment which required the most power efficient chips to run successfully.

X86 could not successfully run on mobile processors as it was too power hungry and had too much legacy baggage. X86 was one of the players in the 80s and 90s, but became the leading player in the early 2000s. The Assembly code we write today for X86 is substantively similar to the Assembly code we were writing for X86 20 years ago. That means the instruction set manual or the set of operations an X86 processor has to support could fill multiple phone books, which at the end of the day, takes up transistors and surface area on the die to support all those operations, which makes it very power hungry and inefficient.

What wound up happening was in the early 2000s, to get around that problem, at least on the personal computer level, Intel and AMD introduced hyper threading. The idea that in order to deal with this phone book of Assembly instructions that were taking so long to decode and process, they realized they could skimp on the compute course and literally have twice as many translators from the phone book of old instructions dating back 40 years to the actual compute. They could have twice as many decode units as compute units. Hyper threading reuses multiple parts of the same CPU. I love the fact that this personal computer has hyper threading, because I don't use 100% of my computer at all times, nor am I using a computer flat out so it makes sense, but that didn't work for mobile phones because it was too expensive to run the decode units in general.

It made sense to have a leaner, more modern instruction set, that was more power efficient. It didn't work in the data center either, because what we expect today out of our workloads in the data center, is to pack them optimally using cloud computing. We're now renting as small of a unit as we can get in the cloud and loading it optimally rather than having 100 servers and 20 of them are in use and 80 are sitting idle. Those two forces came together, the power efficiency and simplicity story. That's what brought ARM back into the data center, not only confined to mobile phones. ARM in the data center is more power efficient and not burdened by legacy baggage, and it's not hyper threaded. One VCP of ARM is actually one compute unit, not half a compute unit, which means you can saturate it fully and not have it sit there waiting because your workload is competing with itself for usage of the same resource.

Open-source is the reason it took until 2020 to happen. All the legacy baggage was because people preferred X86 processors, and were simply trying to make them as efficient as we could, as power hunger as they were, and people were mostly running closed source software like Microsoft SQL Server or Adobe tools to translate PDFs. ISVs published software which you couldn't change, you had to modify their front end, and you could only do that with an Intel processor. Companies started writing their own software rather than using someone else's, and they started building on top of open-source foundations. That created an opening for ARM to say, we supported multiple processor architectures at the same time in the 80s and 90s, so open-source software in the 2010s and 2020s should also support multiple architectures and not be built only for Intel processors.

That made it finally practical, for the first time, for people to build software for ARM and X86 at the same time, rather than picking one or the other. The last remaining issue was availability. No one will build software unless you can practically run it, and hobbyist software doesn't count. No one will run their data center workload on a mobile phone, so there needed to be mass availability of ARM processors in the data center, as well as developer SDKs for people to develop software for ARM locally, not just cell phones. Those two things came together when Apple released their M1 based laptops which utilized the ARM instruction set, and when Amazon released the Graviton 1, 2 and 3 chips. You may not be able to get it in a box sitting on your desk, but you can get it in the form of a laptop or in a cloud VM. The advantages to switching is the availability of the software and hardware. Those three elements all converged in 2021.

### What's your forecast of ARM’s market share in the next five to 10 years?

> I've seen analyst reports claiming 15% of Amazon's new build chips are ARM. I'm not in a position to substantiate or deny that, but it would be completely reasonable in the next five years for a majority of new data center chip deliveries to be ARM rather than X86. If we're sitting at 15% to 20% today, I don't see a reason why that's not 50% of new deliveries in five years. There is a substantial install base of X86 that may not be going away because people have their legacy payroll apps which need to run on an X86.

### Going back to Amazon, why design Graviton in the first place?

It was a speculate bet at the time. Amazon acquired Annapurna Labs, and put them to work building hardware TPMs like the Nitro chip, which also handles virtualization. They realized they were a fully vertically-integrated software and hardware company, like Google, so brought in an external chip maker to build chips for them. I saw this happen at Google too with Titan Security Keys and the Titan data center chips.

### How is Google competing with Graviton?

That is where Google did the majority and Amazon did the minority opinion thing, and Amazon clearly won. Google brought in an external hardware design team and put them to work building the chips used in Pixel phones and TPMs for their data centers, but they did not build general purpose CPUs. Amazon originally brought in a team to build their TPMs and virtualization assistants, but decided to license ARM for general purpose CPUs, and to start producing their own general purpose CPUs based off ARM IP. That was a major step Microsoft and Google didn't do, despite Google having an in-house chip design team. Both Microsoft and Google, as of a month ago, have become Ampere licensees, and are running Ampere designed chips in their data centers rather than self-designed chips. Amazon bet early on ARM general purpose CPUs, and have that capability in-house which they have scaled up rapidly.

### Why are Microsoft and Google not doing it in-house? Is it too late to catch up?

They cannot catch up. If you look at the history of Nitro to Graviton 1, 2 and 3, that journey took Amazon three or four years, so Google and Microsoft are three years behind. They have no experience deploying any general purpose CPU like the ARM Cortex A72 which Amazon originally deployed as Graviton 1. They're not going to go from sitting to running, which is why they have licensed.

### What can Ampere do for them?

Ampere provides already designed and fabbed chips, so all Microsoft and Google have to do is solder them to motherboards and rack them.

### But they won't be fully integrated with their compute like Graviton would be?

Yes, exactly. Ampere is providing the physical chips to solder to a motherboard, and Google and Microsoft have an additional offering you can use with Google TPUs or Azure, but it's not a core experience of using GCP or Azure. With Amazon, Graviton is for better or worse, a key aspect of running on Amazon. Amazon let this slip a year ago: if you are using an Amazon application load balance or ALB, their ingest and routing layer, you are using Graviton. Amazon doesn't offer you the choice of using a Graviton or Intel-based ALB, because it is a managed Amazon service where Amazon commits to route your packets. Amazon runs that on Graviton which I can assure you is not the case with Google's core services, which are all X86, and Ampere chips are a side attraction.

### How efficient can Ampere get to versus Graviton in the next few years?

It's going to be an interesting race. The difference is that the team at Annapurna are deeply vertically integrated, therefore they can test and deploy in the same data centers their chips will be deployed in. Ampere are designing these chips but don't operate their own data centers. The other challenge is that while Ampere's Altra current generation chip is based on ARM Neoverse, they have stated an intention to continue licensing the ARM instruction set, but not to license the ARM cores. They plan to go their own way designing custom cores which are not based on reference ARM designs. It will be interesting to see how that goes for them, as it is a very high risk move. Either it will succeed wildly and they'll do something ARM didn't anticipate, or it could fail, and that is an immense R&D effort.

The direction I've seen is that Graviton 2, which is competitive with Altra – they are both based on Neoverse-N1 – is that Amazon has already released Graviton 3 which is based on the V1 core. The Annapurna team is focusing on the best vertical integration of ARM Neoverse cores in the data center. Ampere is not going to specialize in vertical integration, but will focus on building the best core, without using ARM IP. I would not be surprised if Amazon releases a Graviton 4 based on the ARM Neoverse N2 core. They're choosing to spend their innovation tokens on integration instead of core design. If we're in a situation where 15% of CPU shipments are ARM today, it is still anyone's game, but not once we reach 50% market share for new shipments of chips.

### Ampere designs effective cores, whereas Annapurna integrates the full stack?

Yes, that's what it will come down to. At the end of the day, it's price performance. Who is able to deliver the most performance for the fewest watts and at the lowest price.

### Who do you think will win?

My money is on Amazon because they've been doing this the longest at scale. Ampere is also behind because they didn't find someone who was willing to believe in them and vertically integrate them from the start, with the exception of Equinix Metal/Packet, who are awesome and I adore them, but Equinix Metal is not a hyperscale cloud. Equinix Metal was one of Ampere's earliest customers as far as deploying their processors, but they're never going to hit the same volume as Amazon.

Amazon has that unique advantage of doing this in the open for at least four years, and privately for longer. They know how to do this which shows in the interval from Graviton 1 to 2 to 3. They are rolling out the newest generation ARM cores every 18 to 24 months. That is a drum beat whereas Ampere are only starting to commercialize their Altra and Altra Max. Their next generation core is nowhere near to being offered to anyone, whereas Amazon already has Graviton 3 deployed in the field.

### It seems like a big bet for Microsoft and Google to loosely partner with Ampere?

They're toast if they don't, so it's better to do something rather than nothing.

### Culturally, why did GCP and Azure not make this decision four or five years ago?

Google were distracted by phones in the hardware business. They put that talented team to work building phone cores rather than data center cores. Microsoft's have done the consumer hardware business with Xboxes and VR headsets, but it's not their DNA.

### Can you provide some context to your decision to first switch to Graviton?

We found out about Graviton 2 at re:Invent in December 2019. Honeycomb was a small series-A company at the time, looking for any advantage we could get. We were willing to spend innovation tokens where it made sense and could give us a leg up over our competition. When we saw Amazon saying, for a modest software engineering investment, you can improve your price performance by 30%, we were like hell yes, sign us up. Our Amazon bill was our second largest expense, with salaries first and office and miscellaneous third. We signed up for early access in February 2020, and by March ran our first workload on Graviton. We were able to quickly validate Amazon was not lying about the 30% price performance. We committed to building and deploying our software on ARM as soon as Amazon GAs it, which they did in July 2020, and by August we were running 50% of our workload on ARM.

### How difficult was it to switch from X86 to ARM?

It was harder back then then than it is today. We were one of the first customers to run on ARM in the data center at scale. That colors my opinion but it was a few weeks of work for me. Not everyone in the industry has my skill set but from an upper bound, starting from a few weeks of work, most people should be able to do it. I've seen Amazon run a few one week Graviton challenges of, follow these instructions, deploy your app on ARM and we will give you a prize if you do it in under a week, and people succeed at that challenge. It's possible but it's very language dependent.

In our case, the hard part was not creating the binaries of our application, which was easy because we used the GO programming language where you set one environment variable to compile for X86 host architecture instead of ARM64. You don't have to touch your source code or install a cross compile chain. GO comes with that capability out of the box so it took me an hour to have my first ARM binary. The challenge was all of the scaffolding. We needed to ensure even a test ARM binary ran on a test machine that complied with security policy, so all security agents and base operating system had to be on ARM. The harder part was the systems integration rather than the raw building of the software.

As we found those issues, we smoothed them out not only for ourselves, but for everyone else. Open-source was a game changer for ARM because it meant you didn't have to fight the same battle 20 times with 20 companies. If any company ran into a problem, you could fix it for everyone else. ARM or Amazon have a team of engineers focused on ARM compatibility that will help smooth out any incompatibilities their customers find.

### If a retailer, CPG or bigger enterprise or legacy business are looking to switch to Graviton, what are the big barriers to switching today?

You need the right leader for the project and several specialists to handle it, who know the set of software you're running and are willing to squish any incompatibilities. If you are a company with a billion dollars of annual revenue, you might want to assign a team of five to 10 people to do this and it will take them a month or two, but it's doable, just on a different scale than we were doing it. It's more a project management challenge than a technical one.

### Can you run two different architectures simultaneously while switching?

Yes, which is what we did for several years. We've chosen to go all-in on Graviton since then, but for a few years we built binaries for X86 and ARM. Our build pipeline had a fork in it, where we would set the environment variable saying built for ARM in one half and built for X86 in the other. They produced two different binary artifacts and we would have Logic at runtime to say which binary artifact I should pull, based on what architecture I'm running.

### Would it be more difficult for the older stacks who do not use GO to switch?

Yes, that's where it depends. GO is one of the cases that is medium difficult. Java is super easy, you simply run the same command to install the Java runtime, regardless of the architecture you're running on; you scrape down your Java jar and it simply works out the box. Interpreted languages such as Java, Ruby and Python simply run. With GO you have to change an environment variable to produce a different binary, then manage which binary to run. If you are a C++ shop, it will take you considerably more work or if you're depending on handwritten Assembly code, which exists in some applications, that can be challenging.

### If Graviton has a 20% to 35% price advantage, why doesn't everyone switch?

I think it's the activation barrier. You need a leader who believes this is a project worth doing, then you need people on the ground who are allowed to spend their time running that experiment. That's what it boils down to today. Two years ago, there were so many barriers with incompatible software and bugs you stumble into. We've squished those and they are no longer a problem.

> I wanted to correct you on something. It's no longer a 20% or 30% difference; it's more like 50% to 60%. If you compare the C6I Intel processor on AWS to the latest C7G ARM processor instance type, it's roughly a 50% to 60% price performance increase. Intel is already optimized as hard as they can, whereas it's just the beginning of the game for Graviton. We have C5 Intel powered instances and C6G instances that are 20% to 30% better price performance. Intel is not going to let itself get eclipsed, so they deliver the C6I which is 15% to 20% better than the C5.

The answer to that on the Grafton side is the C7G processor which is 30% or 40% better than C6G. You see this when you move from Intel to Graviton, going from fifth to six gen, that's 20% to 30% uplift, and you get a further 30% to 40% going to the newest generation of Graviton. Sure, there's been a 15% improvement on the Intel side, but overall, it's literally 50% better performance.

### Companies now have to choose whether to switch to a new Intel process family or to Graviton 3?

Exactly, and the advantage to going with the Intel is you don't have to recompile anything or change your tool chains; you simply increment one digit in your specification, of which Amazon instance type you want to use. The disadvantage is that you're only getting a performance improvement of 15%, not 50%.

### Which company types would best be suited for Graviton?

Companies that write and build their own software and who are primarily using vendors and vendor-written code, who have a legacy install base and don't know how to build their software from scratch. If you are only paying software maintenance teams, not software development teams, you're going to have a rough time. This is why Honeycomb were some of the earliest adopters because software is our bread and butter; it starts with other software-as-a-service companies.

One of our clients is Vanguard, who is an interesting case because they're pretty tech forward and care about performance and user experience and write their own software. Software to them is not a cost center but a profit center. If you're using ALBs, you're using Graviton, whether you like it or not. Amazon has already started tiering their offerings, but don't offer you an architecture choice, they simply give you whatever they think will be the most efficient. Another tier called managed services allows you to run an M5 or M6I like RDS MySQL instance, but Amazon has made it as easy as, you change from M6I to M6G in your config file, and they simply migrate your MySQL instance automatically.

There are certain categories which don't require rebuilding software that are much more compatible with cost center IT, where you can treat this purely as a cost optimization and not have to think about the technical details. There's a spectrum from things that are automatic versus opt-in, but are accessible to everyone who can write a config file. If you're investing in your software and have a tool chain to rebuild it, of course it's a no brainer to do it, but if you don't, stay on Intel, and you're part of that Intel 50% population set in five years.

### Would a retailer, industrial company or manufacturer who does not write software, be happy with Intel?

Industrial or manufacturing businesses, but retailers have the capability to change. Ecommerce retailers care about this, otherwise Amazon will eat their lunch.

GCP and Azure are offering Ampere because they want to offer both the cost and performance gains without bleeding customers to Amazon.

### Amazon is opting for Graviton for their managed services, so whenever you use a managed service on AWS, you're effectively using Graviton, which scales Graviton instances and gives you a better price performance, therefore AWS's managed services should perform far better than Azure and GCP?

Yes, that is certainly empirically true in our limited set of experiences. We use five or 10 Amazon managed services, not 20 or 30, but our experience in the case of RDS, where we switched all our databases to Graviton 2 processors, we saw a performance uplift. It delayed the rate at which we had to scale up instance sizes because we were using more efficient processors.

### Technically, why is the price performance so good for Graviton?

> That goes to the point I raised about power efficiency. ARM chips aren't burdened by a 40-year-old instruction set, therefore they don't have to devote surface area to extra decode units, which means they are able to offer one for one. If you buy a core of Graviton, it's not half a compute core, therefore you can run the Graviton instance, even though the clock speed is slower than Intel. Graviton is playing the compute per watt game, so you are able to push more workload through at higher saturation because you're not contending on the same compute cores. That takes Amazon less power and Amazon licenses the ARM cores cheaper than the fee per CPU they buy them from Intel. If you buy an Intel core you're paying for Intel's R&D and in the form of energy for the privilege of running Intel cores.

### They also save money by switching?

Yes, we say we get better price performance, but Amazon also gets higher margins on this because it is 1.5 times more power efficient. This is why I love talking to analysts like yourself, because you speak the same language of costs of goods sold. Amazon has a lower costs of goods sold for Graviton because it costs them less power on an ongoing basis, so it's much less opex.

### Which is insane because they saved the money they used to pay Intel, obviously they bring that in-house, pass it along to customers and still have higher margins.

> Yes, they save the money they used to pay Intel. They're paying some of it to ARM, and they're paying less on an hourly basis to run one rack of ARM servers versus Intel servers. They're passing some of the savings along by charging 20% less per core, but I suspect they're getting more than 20% better processing power.

### How does that impact EC2 or AWS's profitability as they switch to Graviton?

I think it's hugely positive. In the case of the managed services where they don't offer you the option, they don't even have to pass along any cost savings. The ALBs cost the same to me as a consumer, whether they're running on Graviton or not, so I think that in general, it raises Amazon's margins across the board.

### How does Graviton impact AWS stickiness?

It massively increased stickiness for us from 2020 to 2022, because Graviton was the only game in town for getting ARM chips with this power efficiency bonus. That nullified any reason I might have had to go to GCP, even ignoring the data locality we talked about and the network trends and costs. Amazon suddenly hands me this 30% silver bullet, now I'm not even going to go look at GCP because they're not going to be able to match the price. In 2022, now that I can get ARM chips on Oracle, Azure and GCP, it makes it not unreasonable for me to look at GCP again, but again, it's a game of catch up. I know it's less mature. It makes it feasible again that Google might be able to beat Amazon in price, but maybe, maybe not.

### Historically, the sense was that obviously GCP was discounted heavily to acquire enterprise customers on cloud.

I can say this having been on the inside: Google data centers, from a PUE perspective, are much more efficient than Amazon data centers. Google has put a lot more investment into them, they have fewer availability zones, but each Google availability zone is super hyper tuned because they were originally built for Google Web Search. Some of that might have been a customer acquisition strategy, but Google was able to afford doing that and did not sell the shit at a loss. Google legitimately had lower PUE and was able to pass those savings through to customers, except they were doing lower PUE, but using Intel chips. When you introduce ARM into the equation, that makes Amazon cost competitive.

### Do you think as Ampere scales, GCP can close the gap on the discount?

Maybe, but then Google is not offering a single managed service on ARM; it is a side show; it's a lack of deployment at scale. Google doesn't think Ampere is ready for prime time such that they can make it a default, because they're not vertically integrated. They're not thinking about this and playing that same game.

### What's the percentage of Graviton instances on AWS today versus X86?

Other analyst reports claim 15% of new Amazon instances are Graviton today, but I don't know how that compares to their existing install base. I don't even know if that 15% number is true; that's more your domain than mine to guess that.

### Back to GCP and Azure, what's the biggest risk to their business versus AWS, given the growth in Graviton and the performance you're seeing?

In 2022, why should someone pick Azure or GCP over Amazon? Amazon is the safe default where you cannot go wrong; it is the benchmark by which other clouds are compared. Originally, someone would switch for cost, quality of network or machine learning capabilities. Can Google and Azure maintain their advantage in the areas they already have an advantage? Can they catch up where they're behind or will Amazon run away with their existing lead?

### How will the market share between the hyperscalers change in 10 years’ time?

Honestly that is not the question I'm looking at. I have my eye on the back to data centers movement. We saw Dropbox build Magic Pocket, their own hosted data center solution to store their files on disk, because they determined Amazon was charging a markup on S3, and thought they could get better cost economics on a core part of their business. The question is, are Amazon's, Azure's and Google's largest customers going to eventually leave and go to custom-built data centers? Uber runs its own data centers but has a small footprint in AWS, which will always be the case. The large companies and largest users will have the most experimental and most elastic parts of their workload running in public cloud, but the private cloud question would be keeping me up at night if I were Amazon. Oxide Computer are marketing that running a data center is no longer as hard as it used to be; you can simply wheel in and plug into our racks.

### Can you use Graviton AWS services and stack them or do you have to use your own?

Oxide Computer is currently using AMD chips and are not yet deploying ARM. If they were deploying ARM, I suspect they would be working with Ampere. For the moment, Amazon has this huge advantage of integrated Graviton up and down the stack. Is there going to be a point where the cost economics dictate that Amazon's largest customers wind up running their own private hardware?

### It seems like a lot of work to run your own data center?

Yes, but that is the bet Oxide Computer is making, that they can lower the amount of work it takes to run your own cloud. Amazon will continue to have the majority of market share but how big will the public cloud pie grow versus the private cloud pie?

### How do you think that will shake out in five to 10 years?

There is a credible enough risk private cloud will become a big thing, but I'm not going to call that yet.

### One of the disruption risks to AWS and the cloud players is that Oxide Computer can effectively transition bigger companies into their own private clouds?

Yes, which is why Amazon has done Amazon Outposts. They are trying to get ahead of this by saying we can offer you your own private data center and manage it for you, but you're still paying Amazon's margins then. Either direction, but it is something I am keeping an eye on.

### Maybe their margin needs to come down, but they capture more market long term?

Yes, there are infinite ways this can play out. I'm not confident calling it in either direction, but it is something I am keeping an eye on.