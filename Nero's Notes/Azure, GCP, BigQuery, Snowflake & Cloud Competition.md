# Azure, GCP, BigQuery, Snowflake & Cloud Competition

by  #InPractise 

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### Can you take us back to the early days of Microsoft and launching Azure? How was Azure positioned, in the early days?

I was fortunate in seeing Azure being launched from the Alpha Days. They used to call it the Red Dog. A lot of people don’t realize it but it was, basically, the founders of Windows NT VMS, a gentleman called David Cutler, who is one of the architects of VMS, of Windows NT. One day, Ray Ozzie brought him over for the internet disruption, in 2005. I remember that infamous memo he sent out to the worldwide employees.

You’ve got to remember, back in 2005 to 2008, AWS was launching EC2, in the beta stages. I think Google had their App offering which is strictly a PaaS platform. But Microsoft was really known for Windows, on one side, and then for the visualstudio.net. That was the most popular development framework.

Initially, they designed Azure to be an extension of Windows, on the internet. How do we take this Windows and put it into the internet and extend it? Then they realized that Microsoft’s strong heritage of development, with .net, should be the one that we should parlay so let’s go ahead and launch it as a PaaS service. But they then realized that the real low-hanging fruit opportunity, and where they could monetize, was IaaS. There is just so much of the core infrastructure, when you talk about computer storage network, that could be done first.

I think that was a wise decision because PaaS is a lot more complicated to a lot of people. They understand the basic components of infrastructure but PaaS was a bit more complicated because it involved stuff such as middleware, runtimes and it involved the operating system. I think they made the right decision, going into the infrastructure, but it was interesting that they chose to go as a PaaS service, in the beginning. I remember doing a market strategy for PaaS and it wasn’t really sticking with our clients. When we shifted over to IaaS, it was a little bit easier.

### How did that compare to AWS?

I think AWS started out with IaaS, with EC2. I think they got traction a lot earlier. I think Microsoft made a mistake in going with PaaS because I think they were trying to be more like an app engine, like Google was and I think that delayed them a little bit. If they had started out as IaaS, I think they would have got closer to AWS. I think going with a PaaS product set us back one or two years.

### Can you just explain IaaS and the basic EC2 offering?

If you take IaaS, PaaS and SaaS, what I like to tell people is, there is this famous infographic called Pizza as a Service; I used it a lot, in the early days. People are familiar with on-premise but in this case, starting with the infrastructure, you have the servers, you have storage and networking. Then you have virtualization, followed by operating systems, such as Windows or Venix. You need middleware components, such as Oracle or DB2. Then there is runtime and APIs, then you had databases and applications on top.

For Infrastructure as a Service, what EC2 did really well is simplify that. They said, we’ll take care of the storage, the networking and we will take care of the VMs and the servers. You, Mr Customer or Mr Enterprise, you can install Linux, you can install Windows, if you want; you can install your middleware components and all your runtimes, so you can bring in all your data and applications. For them, that was an easier lift and shift, over to an IaaS. They didn’t have to recode or rearchitect everything because the underlying elements were mostly infrastructure. If it was already running on Windows or Linux, they could import that over very easily.

This is versus, if you had data PaaS, you would have to think, is the runtime going to be compatible? Is this OS, that’s up in the cloud, the same version and the same patch level as the OS that we were running on-premise? Is the middleware going to be compatible? There were a lot more moving pieces where you had to make sure there was compatibility.

That’s why I think, Amazon doing this, said, let’s crawl first then walk. We will then go from walking to running. That approach was easier for the customers and I think that’s why they gained traction at a much faster pace than Google and Microsoft.

### At a simple level, the Infrastructure as a Service layer is like leasing a virtual machine from Amazon, in a datacenter, which offers you compute and you can get storage, as well?

Plus the network piece.

### What drives a competitive advantage in offering IaaS?

I think the biggest competitive advantage is that customers don’t have to keep up with the maintenance cost of all the servers and the hardware in a datacenter. If you think about an IT executive, they want to do two things. Firstly, they want to reduce the opex cost and complexity. Secondly, they want to be able to create an agile, nimble framework, so they can transform their business. We hear the term digital transformation a lot.

I used to run global datacenters, at AOL, one of the biggest companies back in the day. Every time you had to order a server, that might take you six weeks. Then it might take you two weeks to install, wire it up, cable it, set up the network configuration, set up the security apparatus. Then you have to install the applications. You just saved six weeks of that, because you only have to go into your portal and you have, like you said an APM session that is out in the cloud and you can then just start loading applications. You can then reduce the infrastructure cost and, hopefully, you can reduce the infrastructure footprint in your datacenter. That would save on cooling and power.

### What about the competitive advantage between Amazon and Microsoft? If I’m an enterprise customer, I think it’s clear that everyone is going to move to the cloud to save costs, but what drives a durable competitive advantage in Amazon and Microsoft offering, effectively, a very similar service?

Today, they are all table stakes. There's no real competitive advantage just on the infrastructure service. That is table stakes, everyone is going to do it. Most of the company is going to redo it, though the differentiation is going to be in the PaaS and the SaaS offerings. You see companies like Snowflake and Databricks trying to leverage that momentum.

### Isn’t there a physical infrastructure required to build the datacenters and offer the latency effectively? Let's say that we've got Amazon, Microsoft, Google, and maybe one more, potentially, but those three are definitely going to have the capital and the capabilities to build the physical infrastructure. Is there any competitive advantage that one of those can earn in infrastructures of service?

> That probably goes to a follow up question; what are the real advantages of AWS versus Azure versus GCP? Like I said, infrastructure is table stakes. But I would say the biggest thing that Azure has over AWS is hybrid capabilities. Amazon's go-to market strategy and the technical architecture has always been cloud; let's do cloud native, as much as possible. Since Microsoft started its roots in Windows Server and SQL on premise, they realized that customers were still in the very early innings or stages of moving their critical systems to the cloud. They wanted to provide a path to cloud and so they have a stronger hybrid offering. I think that's a key distinction that people need to realize. From infrastructure, they're all common but you have to think in terms of what my application footprint is going to be like? What is my data footprint is going to be like? Then you're going to have AI and machine learning. Then you have to think about how you are going to interoperate that on premise? It's not like, I'm going to wake up tomorrow, and I'm going move 50% of my SAP applications to the cloud; that takes years. I think having that flexibility of giving people that hybrid choice is a huge advantage.

### How have you seen customers approach that decision to move to the cloud?

I deal with regulated industries like energy, utilities, and also FinServ and then retail when I was at Google. The more legacy customers, such as energy and utility and manufacturing customers, they have more on-premise application, that is not yet cloud ready. Customers have different options to move to the cloud and lift and shift is probably the easiest one. But when you had SAP, or AspenTech, or Schlumberger’s application for Seismic, these were probably made from the 70s and 80s, so that the kernel, and the code needs to be rearchitected to be cloud. What people will agree to do is to create parallel environments. You're going to set up a new instance, in the cloud – your primary instance, is still going to be on-premise – and then you're going to figure out and start slowly moving bits and pieces of this application to the cloud.

But since it's not a seamless, easy migration, lift and shift, you're going to be recoding and rearchitecting. For experiences that I've seen, they like to choose. If they are a huge SAP shop, and if they're a huge Microsoft shop, which everybody is, Azure has a stronger play. But Amazon has done a good job lately, of putting in lots of partners; they use a lot of partners and third parties. They partner with SAP or they'll partner with these types of companies like Schlumberger; they'll partner with a FinServ application and they'll reengineer, have engineering teams with those teams sit together, and help develop these fast tracks or they call it the lighthouse type where they go from on-premise to the cloud in a very seamless way.

### Let's just take that example. You've got a big energy company, a huge on-prem legacy, obviously use Microsoft. What exactly is the pitch from Amazon to win that account versus Azure, for example?

Amazon is always going to go out saying, we're the first to market, we're the most mature, we're clearly the Magic Quadrant leader; we have the most expansive set of services. One thing they really do a good job is saying that, we have the most customers and customers that are large in your industry. They make you feel safe. There was a saying back in the old days, you never get fired for buying IBM. It was safe choice. They make you feel that way. They make you feel like if you choose Azure, you're going to have a mature and high-performance environment. Then it really comes down to, what is the ecosystem going to be like? What is the app support going to be like? What is the innovation going to be around AI and data and ML? If infrastructure is table stakes, there's really no depreciation.

### Is it really table stakes though? Is it literally like it's commoditized and is it really just a given and therefore they don't really look at the value of that? Do they not look at the price, or the latency or anything specific about the infrastructure layer?

There's got to be some differentiations between where the datacenters are located. You've talked about latency, but price is all raced down to zero; it's going to be heavily commoditized and they're going to keep reducing cost to zero as people can scale. Nowadays, when I have conversation with customers, they're not looking at infrastructure as a service, because they already moved that over. The stuff they're having conversation around is around AI and around data. It's more of those conversations around that PaaS layer, and then even the SaaS applications, but you're not having a security conversation anymore; everyone's going to have this high performance DDNs and data and network layers. They're going to have enough redundancy built in around these different locations. I guess every now and then I might have a customer that says, we want to operate in Russia and Ukraine, so how do we deal with that compliance and how do we feel that those type of issues?

### I saw some estimates that roughly 60% to 70% of AWS's revenue is EC2 and Esprit, or are a huge part of it. Obviously, AWS's EBIT operating margin is 30%. How does that weigh up if this is commoditized and people don't think about it; where is the margin really coming from? AWS?

No, you're probably right, that those parts are the biggest piece of it. Without infrastructure as a service, you're not going to get the higher-level applications, you're not going to get the SAGE makers. For the customers I deal with, when they're talking about moving to the cloud, what are the benefits and pros and cons? Which is better between Azure, AWS or GCP? When they conduct the RFI and RFP, they don't focus on the infrastructure, because to them, this differentiation is very small, unless you have a very specific use case, like if you need a redundancy in this country.

### Vertical specifics like PaaS and SaaS.

Yes; the things that they get more and more customers looking at is around a data layer in their AI and ML there and those things. That's the reason why companies like Snowflake and Databricks are having more and more discussions.

### Let's say in five, six years’ time, we have a Snowflake, best of breed SaaS player or PaaS player like Snowflake for every micro service, that's competing heavily. Where does that leave AWS?

I think the big question is, does Snowflake have the capital to build out the infrastructure and service layer in a datacenter? Do they want to compete in that area? I don't think so. I think the reason that is, like you said earlier, there's only four people or four major companies, Microsoft, AWS and Google and Alibaba. For these Asian markets that have enough capital to build out a datacenter and build out those networks and build out the pipes, it's $2 billion for a data center. I don't think they want to get into that space. I think all these hyperscalers are pretty safe. That infrastructure is not going to be touched.

Where they're going to feel threatened is going to be on the data side. Google, for example, is BigQuery and this big lake that we're going to be choosing later from data warehousing side and data lake side, that's going to be threatened, because that's where all that value comes in. For companies like Snowflake, right now they're leveraging these hyperscalers as a partner, and Databricks does the same thing. But if they started really taking market away from, let's say, Azure Synapse, or Azure SQL, Google BigQuery – and Amazon Dynamo – I think they're going to be acquiring them. I think that's probably the best way.

### That's my question. Let's just assume Snowflake doesn't build those things but, let's say, there's a similar player like Snowflake in databases, in all these different services on top. Therefore, there are all these other enterprises moving to the cloud and want to use the best in breed SaaS or PaaS player; they want to use Snowflake versus Redshift. What do you think that does to AWS's profitability?

I think it's going to shrink your profitability. Just like Oracle. When I came to Oracle, I saw Oracle has declined, because Larry Ellison thought that people would never get off Oracle databases, because it was so mission critical to their business, but look what happened. I think it will definitely shrink their profitability. Any time you take your market away from Redshift, or Dynamo, or Azure Synapse, or SQL or BigQuery, which is one of the most popular product lines in that space, it's definitely going to hurt their business.

### What's the hard thing for me to look at from the outside looking in is, obviously you see AWS 30% margin, but we don't know what's truly driving the profitability. Obviously, it's all interlinked. Let's say that infrastructure is going to be an oligopoly between two key players but like you said, it's commoditized, the value is potentially on top. How do you think about the profitability per service or per layer that the hyperscalers can offer?

If you really want to drill down to it, each one of those layers could have higher margin versus lower margin. Think of it in a traditional sense, where if you were HP or you were IBM, you're selling hardware. Hardware has very low margin business and then if you were selling an application that might have a higher margin business, and you're selling databases and everything, so the pricing structure is different. Pricing structure is different per service. Taking account of egress charges also are different, too. At the end of the day, if you really want to know what is the fastest selling product, you have to look at that. Obviously, the customer's always going to get multi-cloud; I don't know a single customer that just has one. Just like back in the day when it was on-premise, people didn't just learn everything on Linux or Unix, or Windows. There was always a hybrid environment. I think Gartner and Forrester might say 80% of people are going to be running multi-cloud tenancy.

### How do you see the difficulty of migrating between clouds changing over the next five years?

I think they're going to try to impose migration type of tax where they charge you heavily on egress. Even though companies like to say that they want to prevent you from vendor lock-in, I think that is a go-to market strategy to make it very sticky, as much as possible and I think that egress tax is going to get you. It's one of those things that when you sign a contract, you know what it is, but you don't think about it.

Another thing that customers like to do – or enterprises like Microsoft – is they like to play around with the licensing models. Microsoft is very good at imposing a Microsoft Terra if you run your SQL environment on AWS. AWS like to counter, well, you could get BYOL licenses, and then Microsoft might change their terms and say, yes, but if you run it on AWS, you get charged extra, but if you run on Azure, there's no additional costs. There's always going to be those licensing schemes that they can play around with. And if you're running a larger environment when you have 1000 instances of SQL Server or 1000 instances of these different workloads, that could add up. You’ve just got to keep in mind the licensing costs and then also the migration tax or the egress charges.

### Let's say it's 2030, for example and, for some reason, it's really easy to now migrate workloads between the infrastructure layer, what could be the reason that that would happen?

From a technical technology perspective, migrating from one cloud to the other, that's not complicated. It could be, if you're running a huge ERP financial system with a whole bunch of modules and pieces. But generally speaking, there's plenty of third-party tools and third-party SRs that can do that; it's relatively easy. What I was referring to, is that stickiness is more from the cost, like the egress charges and the licensing. I think everybody has tools in place to make it easy to migrate off of your competitor to your own platform. But I think you just have to really understand the licensing implications and the egress charges.

### It takes time and costs the business like you said, just in effort and attention to migrate.

Yes, so you’ve got to ask yourself, if the cost of migration might take $600,000, is it worth it for 10% gain? There are going to be these departmental apps that say, we just run 100 times better on platform A, on Azure versus AWS. And Azure might say, we released this cool feature. IoT is a great example. Azure said, we do a very good job of IoT. If you're in the manufacturing space with millions of sensors, and if you already have an Azure Data Warehouse, then why don't you put that over there? I think customers are looking at trying to consolidate on the data side, trying to build a data warehouse and data lakes, and trying to consolidate that. Not a departmental and use case basis.

### How can Kubernetes change the stickiness of IS layer?

I think everyone was using Kubernetes. I think that's just putting everything in a container. Docker started all this. It fundamentally changes the way you write applications to microservices and microkernels versus the old monolithic applications. I think if you wrote everything in a Kubernetes framework, that would definitely make a lot easier to put things over. Are you familiar with Anthos? Anthos is a great example of taking Kubernetes to make it easy to migrate from AWS, Azure to GCP. Because Thomas Kurian’s strategy has always been, we realized that the customer is going to have multiple cloud vendors, so let's make it easy. Since Kubernetes is the heart of what we do at Google, they're probably the one that is promoting Kubernetes the most, let's put that as the Anthos. And I think that was a really good strategy for them.

### That makes it easy for customers to move workloads between Azure and AWS on the IS layer?

Yes; the application was designed as microservices. It was a monolithic application, with on-premise, that Kubernetes has no value because they were never containerized in the beginning.

### How do you see these energy companies and big legacy on prem businesses approaching shifting over?

All new applications that are being built are going to be on microservices, they're going to be containerized. That is going to be the trend going forward. They are trying to retire the technical debt of these legacy applications, the three-tiered application model. The whole app development has been more cloud native now.

### If it becomes easier to migrate, how do you see the pricing of computing storage changing over the next five years?

I think it's going to be a race to zero as companies scale and have the ability to build new datacenters. Just in simple economics, the more you have, then you can scale down. You see that all the time when one cloud provider reduces theirs by 20% and the other one does the same. It's going to get cheaper and cheaper and cheaper. Again, heavily commoditized, it's going to be table stakes. Then they will start charging for the AI and ML piece, because that's where the real property is. Because if you look at the number of instances they charge for an auto ML, that could be 100 times more expensive than simple network and storage.

### That means if you're invested in AWS, you have to be sure on the ability of Amazon, for example, to capture those instances or the AI/ML, micro services on top of their infrastructure in the long run?

Yes, it's all about data; it's all about AI. And some of those, middle layer pieces. Think fast.

### How do you think Amazon has an advantage in that, in winning that share in the PaaS layer in the long run?

I think Amazon does a great job because they are the largest user of themselves. A lot of people already know that Amazon has a very advanced set of data, just from the billions of transactions and millions of customers that it has, and then the recommendations and the recommendation engines they use. They're pretty known to be the AI leader in that space. But I can tell you that Google has the brand to be AI/ML leader, and here's why. When I was selling Google to the customers, people knew Google, it's not on the Google search. At the end of the day, these companies are data companies. And there's nobody who has more data than Google does.

Every time you do a Google search, every time you open up Gmail, every time you use Google Maps, there's over nine applications that have over a billion users worldwide. And that is petabytes and petabytes data that they're going to run a base and analytics on. Since the majority of Google's revenue – I think it was like 80% – still comes from the ad business like YouTube and ads, they can leverage that to the cloud side. A customer will come to me and say, I'm on AWS and Azure Shop, do I really need a third player? I would say, yes, you do because you're trying to transform your company, trying to get more insights into the data that you have in your refineries, or what you're doing around your utility space, or what you're doing around your banking space. Sure, AWS and Azure has it. But we have things that are light years ahead and much simpler to use. We make it so that you don't have to be a hardcore Python. Our programs make it so that you don't have to be a data scientist, you could be just an analyst.

### You go in selling the data and BigQuery effectively. Was that your hook when you're selling?

We don't we don't mention products. But basically, we're selling that we have the most advanced analytics, AI, and data.

### How do you compare BigQuery to the other offerings?

> Everybody was trying to get into Data Warehouse. You have Data Warehouse, Redshift, and you have Synapse or SQL, Azure SQL. It was hard, because Redshift probably has the largest base; they've been around the longest. What we looked for around BigQuery was a high amount of transactions. NASDAQ is a good example, where you have a whole bunch of real time transactions coming in. Another one could be sensor data that could be coming in. When you look at these different types of data warehouse, you have to look at the four Vs. The volume of the data, the veracity of the data, the velocity or speed and you also look at the value of the data. Do you need millisecond response? Is it emitted response? Customers can decide, and then you say, if you really want to run data, then the tools are important, the analytic tools are important. We had a hard time competing with Microsoft, because the world leader at that time was Microsoft BI, because everybody was familiar with those tools. Then you have Tableau but Microsoft BI is by far the most entrenched and most user friendly because it stemmed from Power BI, Excel and Power BI.

Accounting departments knew how to use it. Everybody in finance knew how to use it. Pretty much every department knew how to use Power BI. We had to take that conversation that bit further and say, should we take an analyst, data business analyst, statistician and make that person a data scientist and teach him some programming? This is what Google did a lot with their data science teams. So we evolved from business and we did a lot of these peer-to-peer sessions.

I would take a customer like this super major, Global Fortune 2 oil company, or a retail organization, and brought them into Google and show them how Google did it. That was a really effective way to establish that trust. It was a lot easier for me to sell into retail, because retail was already a large Google shop. If you look at all the major retailers in the world, they don't want to do business with Amazon; it's a competitor. Since they're already spending billions of dollars with Google on the ads business, it was easy to leverage that sponsorship at executive level to get that business in. That was our hook to get into those accounts, the leverage of retail. In the first part of my experience at Google, I was selling into manufacturing, energy and utility. The second half, I was selling into retail and I got a lot more traction by leveraging the retail analytics and retail data and putting that into a Google Data Warehouse into BigQuery.

### How did Snowflake come in and compete?

That's a good question because Snowflake can say, we could do everything BigQuery does. But also, we could do it on AWS, we could do it on Azure. And we could also do it on Google. And we're saying, Dang, we were supposed to partner with Snowflake. Now, they made a corporate decision to say Snowflake is no longer a true partner; we need to compete with them. Because remember, our secret weapon was BigQuery. That was the one that we're really pitching, just Azure was from the data side. Snowflake was gaining huge amount of traction and they were getting a lot of bought leadership coming in, taking market share away. I've heard of people losing deals to Snowflake, because they're all about being open. Let's go back, we can deal with it. We can, it doesn't matter if you're on AWS or Azure; we can work with everybody. Yes, Snowflake's becoming a competitor that we no longer want to partner with them at Google and that was an interesting shift.

### When you were going in at Google, selling these services, you have BigQuery as your secret weapon. You get them to buy Big Query, effectively, and they will have to buy GCPs, kind of like infrastructure and compute. Can you just walk through the sales process and how you run it?

Customers know they don't get actually data and analytics; you need the underlying infrastructure components. But like I said earlier, I didn't have to prove that TCP infrastructure was good enough because they just took it for granted. When I do an RFI and RFP, as long as they said, do you have a data requirement? Yes. Did it meet the GDRP compliance requirements, because we operate businesses in Europe? Does it also have fault tolerances?

### That's like a tick-boxing exercise, effectively?

It is in our department, yes. The true business value is telling me about how we can process these data insights. How do we take that data from hindsight to forecasting with predictive analytics? How do we get to that, really, that using AI and ML to predict forecasts? If you're an energy company, you want a better model to predict the price of energy. So you use these Monte Carlo simulations and a lot of cycles. You want to be able to have the most advanced AI and ML engines to predict that model. But you don't want to have to develop a team of 20 data scientists to put that model together. You want to just get two or three people from departments and put it together like that and that was our pitch to get them on board, those early wins.

### What have GCP got now then, if Snowflake's come and dampened the BigQuery position? What else have they got up their sleeve to drive growth?

We would like to leverage the complete platform, at Google, just like Microsoft. We're not just a data layer; we are the complete flow platform. We also do IoT, we also do app development and some other things. As people are moving into Data Warehouse, they want to take all the data and now they said, Data Warehouse is good, you can run BI and analytics tools, you can get a good idea of what your forecast looks like, good idea what your sales performance looks like. But if your CEO says, tell me about my sales in the next three to five years and how are we going to run our supply chain during post-Covid? Help me build those models, now you're really talking about the data science side. People are looking at data lakes now, so then this company called Data Bricks started coming out and it said, we have the best in class data lake. They used to have a data warehouse to run all the PI Analytics reports. They would have to migrate that data into a data lake, to run the data science models.

### What's the difference, technically, between a lake and a data warehouse?

A data warehouse is where you take mostly structured data, like SQL data, and you run analytics reports using Tableau or using Power BI. This is more rear-looking; how's my sales? How's my sales in a particular region? How's my production in a particular state? But if you want a future looking, if you want to forecast, you have to run AI models and now you have to use unstructured data. Let's take unstructured data from real time feeds, a lot of more variables, so it's not about porosity volume. The four Vs of data come in here. Then you run data science, building these data models, and then we should be able to borrow. You put it back, then you can port that model back over to the data lake. There's been a lot of these Data Warehouse and data lake migrations back and forth and it's hugely inefficient. I think if a company could can get that right, they can build a data warehouse.

### Don't Warehouses offer that?

They announced something called the Snowflake Data Cloud. I'd say that was announced a couple of months ago during their annual summit. Databricks now have Delta Lake, which is a unified data lake platform. Then interestingly, if you look at Google, Google just announced their big lake; instead of BigQuery, they call it BigLake. It's called a Unified Data Lake.

### The competition is basically shifting from structured data to more data science and unstructured data. And then from the warehouse to the lake?

Yes, so they called it BigLakes, combining best of both worlds. Microsoft has something called Synapse. That's got to be the next wave. It's so fast how these things are evolving.

### This is my question. When I look at AWS and I'm thinking, this technology evolves so quickly, you have Snowflake come out of nowhere effectively. How would you look at trying to understand the durability of AWS and their profitability in the next 10 years, if you look at all the innovation on top of the IS layer?

It's hard to stop AWS's momentum though. The reason is, for customers to truly leverage the data lake and the AI and MLs, they still have to move majority of the workloads to the infrastructure service. Gartner or Forrester or McKinsey all say 5% to 10% of data/applications have moved? You still have this huge addressable market space of 80%, so all that stuff has to be moved up and firstly, they're going to move up. They're going to have to move the infrastructure to the service. They're going to start consuming that.

### Is that an advantage though? Does Redshift really have an advantage over being native to EC2?

Absolutely. Every one of those things is going to be very proprietary. And you're never running Redshift on Azure. You never run Bukhari. It doesn't run on EC2. That's why they want Snowflake. That's why they want Databricks.

### Surely, the SaaS companies are going to try and follow in the footsteps of Snowflake and be this multi-cloud best of breed SaaS offering, which kind of neutralizes Redshift and BigQuery across the other services? How can AWS and Azure keep up with that and ensure they don't get out-competed on the PaaS front?

> I think they are the things they have to leverage on their ecosystem. When I was with AWS or Microsoft, I said, we have so many other things that you're really hooked into; interoperability is key. It really goes to the fundamental question, what is best for you? Best of breed, but then you're going to have to spend a lot of time trying to interoperate and make sure it is compatible. Or you might have best of breed, and some just good enough, but then when it interoperates as a whole, that itself is a best of breed. I always told customers, my advice is, don't look at best of breed of everything. Because when you cobble best of breed for everything, if you have very bad interoperability compatibility, then the system is going to fail. Just like building a Formula One car, you could have the best turbochargers, the best valves, the best exhaust, best tires, but if it didn't operate together, that's what it is.

### It's how it works together. You mentioned how the IS layer is commoditized. So how much does the chip matter? Like Graviton, for example, in AWS? How much does that matter?

I think the Gravitons, and what Google is doing with the TensorFlow models and developing those chips, it really shows. My personal thing is, we are like the Nvidia, if you're a gamer. If you want best, the most advanced, we have got those chips for you. I think it's a great marketing strategy. I think it's a great way to show that Graviton is best for what Google's doing with their TensorFlow models and the Titan chips and what Nvidia is doing with their vast AI on their chips. It shows that they're putting a lot of R&D money in investments, and we're taking that seriously. I remember for a lot of gamers, paying for a $10,000 top line in video versus $2,000. For you and I, that millisecond frame difference doesn't really matter but for gamers it does. End of the day, how many customers really need that much horsepower? Maybe NASA, maybe if you're running a complex Wall Street application or something, but I would say 90% of them probably don't need those Graviton and some of those advanced chips. But it shows that Amazon is really serious about this, and they're a class leader.

### All of the value, like you said, comes on top of the PaaS layer?

I think so.

### Let's say I'm running AWS, I've got EC2, basic infrastructure layer and I use Redshift as well, in my business, and I want to switch to Snowflake. Can you just explain, or just describe roughly how difficult you think that is, or would be?

I think, technology wise, not too difficult. There's plenty of tools by third parties and Google have their own tools and Azure have their own tools Again, you just have to be wary of those costs. They're going to charge you a migration tax. What is the egress is going to be now? Egress is going to be very expensive. And then the licensing model, so just be careful of that.

### How expensive are we talking about?

If there was a price sheet, you could look at what the egress charges are, but it could add up because some of these data warehouses are petabytes in size. If you had a customer on Redshift for five years, and they stored all the customer data, for example, that could be petabytes of size and volume. How long is it going to take to move that over? Pretty fast but then the cost is going to be pretty expensive. What I've seen is more and more people are developing applications on Snowflake like that. I haven't seen a big migration of a cloud, to be honest with you. From AWS, I see more departmental apps, but not a core function like the SAP financial app that was used to run on AWS; now it's all on Azure. I don't see that too much.

### Because of the costs and time. How does Oracle position themselves in all of this?

Did you see the new announcements? I could tell some interesting stories. I left because of Thomas Kurian actually, to join him at Google, because I had a chance to work with him as an executive sponsor on one of the accounts. Thomas Kurian had always said we need to open our platform for interoperability in a hybrid world. I think Larry Ellison, with his hubris and with his ego said, no, we can develop our own infrastructure service called OCI. Remember Oracle, that infrastructure? Larry Ellison came from the mantra, if you build it, they will come. He made that famous speech that Amazon would never get off Oracle. He pretty much dared them, you will never get off. And what did they do? They developed Redshift and got off of Oracle, within 18 months or something. Thomas was Head of Development, pretty much Larry Ellison's right-hand man. He was in charge of all product engineering. So when he went over to Google, his openness and interoperability, he's the one that really launched Anthos, about multiple clouds.

I think in order for Oracle to survive, they needed that partnership. They needed that partnership with Microsoft. Because, at the end of the day, he realizes that people are not going to spend money on another infrastructure service in OCI because they already have AWS, Azure and now Google is gaining traction. You don't need a fourth player and OCI was never gaining traction. When I was at Oracle, trying to gain traction, nobody wanted that. They still have some of the best databases. Not only with the Oracle databases, on the SQL side, but they had MySQL, they had all these different types of databases. I think they did a pretty good job with autonomous database, creating a lot of these AI and ML on the autonomous database side. But they realized that their customer is going to be using AWS and Azure. I think his ego is going to probably prevent him from making a partnership with Google and AWS, but I think that will be a better strategy being partnered with those two. Same thing as Snowflake's doing, same thing Data Bricks is doing; partnering with these other customers for survivability.

### What are your first views of the Microsoft partnership? What does that mean for Oracle?

I think it favors Oracle a lot more, because now they can put their database in everything, in all the Microsoft customers. They don't realize every one of Oracle's customers is a Microsoft customer. I don't see Microsoft viewing Oracle as a threat because I think they said, we still have enough other, we have our own databases, we have our things.

### Why are they not a threat through? Because they can't build the infrastructure?

Yes, they can't build infrastructure. But also, I think that Microsoft feels like their databases are still better and that the Azure databases are still better than anything Oracle has. Oracle is one of those legacy customers; they're developing applications today. You mentioned Kubernetes earlier, these microkernel services, they're not putting it on an Oracle Database. They're not building an Oracle database, they're going to build it on an AWS database, there's like five or six of them. They're going to build it on Azure type of database because it's already cloud native, it's already got all the frameworks in place; people are used to developing that language. Also, the generations of people that are developers now, they're in their 20s and 30s; they're not the 50 to 60 year olds that used to develop a code for the Oracle site when it was a three-tier application. That actually has a huge play, people that are born of a younger generation; they were born an internet generation, they were born in a cloud native generation so this is a lot more familiar and easier for them.

### If you're building something in Kubernetes, you're not going to stick it on Oracle?

No, you would never do that.

### So what can Oracle do then?

If I was Oracle, I would focus my business on the SaaS side. If you look at Oracle's growth, data is important because there's still a lot of data but my growth of the business is going to be on SaaS because they still have NetSuite. They still have HCM, the ERP applications. Now they're going to be competing with Workday, they're going to be competing with Salesforce CRMs of the world. They're going to be competing with the true SaaS players, but that's where the growth is. I think the days of Oracle databases is like the days of IBM and DB2 and Teradata and Mainframe. You've already got to remember when DB2 was kind of like the mainstay of the enterprise. Teradata is kind of the mainstay of enterprise. And all those monolithic databases are slowly fading away into these cloud databases. Oracle is the same way.

### In five years’ time, what do you think will be the market share of the major cloud hyper scalers?

I five years or so, it will still be AWS, Azure and then Google. I think that's going to be the same. I think the gap might get closer, but I don't think AWS is ever going to be taken away. Maybe 20 years.

### But why?

Because they're growing and they have such a large base. Think about if you're growing 33% on a large base, but if you're growing 50% to 60% from a small base, you still have a long way to go. It's all numbers.

### What about the 30% EBIT margin for AWS? What do you think that looks like in five years?

I think they said the higher-level services might go higher. You're the finance guy.