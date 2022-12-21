# AWS: Running a Hyperscale Data Center

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### Could you take me back to your time at AWS?

I've been in the data center infrastructure market for 32 years. I was highly sought after because I've run global data center infrastructure organizations. Amazon recruited me over 8 years ago from a consulting gig that I was doing for a large, listed software business to run the entire West Coast; US-West-1, US-West-2, US-West-3, Los Angeles, São Paolo, Brazil, Montreal, Canada, and Dublin, OH. Even though Montreal and Dublin are not necessarily West, if you're not in northern Virginia, they consider it West.

That was my responsibility. I was responsible for safety, security, availability of people, and financials; this is Amazon language. Those were the five pillars, and within each of those pillars, we had a plethora of activities I was responsible for, like logistics. I had to handle logistics everywhere, from the facilities parts, to the break/fix, to brand new data center construction, and with people, managing an entire data center organization of over 600 people that manages all those hyperscale data centers/colos. And all the financials on the construction of new hyperscale data centers, retrofitting colo data centers, and the financials of expenses. I also knew how much revenue I was generating for AWS in the region. So I had a lot of financial responsibilities.

Ultimately, number one was always safety. I've been doing these consulting talks, and even though we consider safety number one, nobody really likes to talk about it. I had the strongest safety record in all of Amazon Web Services data centers globally. I'm very proud of that because data centers are a very dangerous place to work; some people take it for granted, and I'm passionate about safety. Especially when Covid came around, trying to run a data center with Covid is just a pain in the butt.

That pretty much talks about the high-level roles. In my day-to-day responsibilities, I met with all the directors from every region I mentioned, such as San Francisco, Oregon, Seattle, Dublin, Montreal, and São Paulo. I would meet with them daily and say, okay, how do the operations look? We went through the five pillars, how are your safety, your availability, and your security? What are the issues, and what projects do you have going?

I would be involved in a lot of strategic and capacity planning. Amazon is building hyperscale data centers left and right, even though the economy is down now. Even in the late 2010s, in the US-West region at least, we were constantly building five hyperscale data centers every 18 months. I had a lot of responsibility for delivering capacity, so I went to the businesses and worked with the AWS teams outside the data center, like the EC2 teams. I'd work with the artificial intelligence team to understand what capacity they needed, how many racks, where they would need them, and what kind of timelines they were on.

The biggest thing was driving efficiencies in the data center, whether from the facility side or the break/fix side; how can we get our technicians to fix broken infrastructure? The failure rate is enormous when you've literally a million servers across a region. For your backlogs, do you know whether it's a memory module or motherboards? We had to be on it to ensure we provided capacity. Sometimes services were so thin on capacity that if you were to lose three or four servers in a rack, that would severely impact the customer. We always drove customer obsession because capacity is the first thing a customer sees. Whether it's capacity from a CPU memory or storage perspective, capacity gets hit hard when you have hardware failures. I would constantly do fire drills to be sure the compute services were there.

### Could I hop in because it's super interesting, and I have so many questions. It’s just so abstract because it sounds like running fulfillment centers on the retail side the way you talk about it, but it’s much more abstract for someone who’s not from the industry. You said you had revenue responsibility, which I understand. Still, you also had all those services, EC2, like you were saying, some things that were higher up the stack, some database services. What is your revenue and their revenue? Not everything is yours. Could you explain how those teams and services interact and contribute to the total revenue we see as investors?

Let me first back up. I've got a revenue number that I use. The key is that my infrastructure supports revenue. For example, the AWS revenue was around $60 billion last year. In US-West, I supported the infrastructure to deliver about $23 billion of revenue in the data centers under my directorship. It's an enormous region. I had a third of the revenue. Northern Virginia had pretty much the other third, and then you had the rest of the world like we were discussing. You've got data centers in Paris, London, and Bahrain.

### So the rest of the world is so behind? Are many people in Europe also taking resources from the US regions?

Yes; the US regions are highly in demand because the cost is cheaper. You've got Oregon, for example; US-West-2 is the cheapest region in the world to get compute infrastructure. Because of that, if you compare it to somebody in Seattle or San Francisco, it could be double the amount in those larger regions. This is because we pass along the real estate, the people cost, and the insurance. The cost to operate in larger metro areas is much more enormous than when you run it out in a desert in the middle of nowhere in Oregon. That's why many folks in Europe or Asia use US computing resources. With an asterisk. We have government contracts that require the data not to leave the country's boundaries, and we are audited on that and so forth.

### So it's one-third, one-third, one-third. How would the split of the product side be? You mentioned EC2 before. How does that interact, and how does that fit into your planning?

A lot of the fundamentals, EC2, S3 Glacier products, Elastic Beanstalk, and some of the real common services are spread out at every data center. You'll always have your foundational services in every single region; that's a given. We would have specialty services like Snowmobile. This service brings a semi-truck up to your data center, sucks it out, then shoves it back into our data centers. That only occurs in Oregon and one data center in northern Virginia. Artificial intelligence was big out of our Seattle data center because it was close to headquarters. Many of our new AWS greenfield product offerings came out of the Seattle data center region. It seemed like the more advanced services that were fresh were in Seattle, and some of the more commodity ones were everywhere. There was some differentiation for the different services by region.

### How would capacity planning work? You said the EC2 team is coming and asking for capacity; how do these services interact? Would they have their own P&L, as you have your own P&L?

The good part of my job was that I was not necessarily responsible for a P&L. I was pretty much an expense. Even though I had revenue going through my data center, I didn't have control of it. If I could provide availability, that was how I was measured, and I wasn't measured necessarily by P&L.

### How could you ensure that you could provide availability?

At Amazon, in the hyperscale data centers especially, we had a highly available infrastructure with multiple outside power suppliers. How our power distribution is set up, you have A side, B side, and a catcher. If we were to lose one side, if we were to use a PDU, if we lost all power, our generators would kick in. So, we were 2N+1. As a matter of fact, in my time there, I never had an outage related to power. We did run into availability in which some servers were single-corded and didn't have multiple power supplies; in those cases, our SLAs were reduced. Our availability was based on a facility number and computing by the service. You could take all those services, EC2, S3, all those foundational services, and I could provide you a report on my availability broken down by service.

### The customer who signs up for AWS, his organization will pick a region.

Yes.

### But it will not pick the specific data center.

That is correct. The interesting thing is that if you are savvy enough, you can do it if you know your Amazon data center regions. For example, there are three availability zones in PDX, which is the Oregon data center. You can figure out what availability zones within that region you could be in. You had that kind of transparency, and I think if you wanted to, you could figure out if you wanted to be in PDX-1 or PDX-3, or PDX-6.

### Understood. You were saying there is hyperscale in these and colocation. Can you give me an overview of the type of data centers they had?

Our hyperscale data centers were about 30 megawatts, and we had about 700 racks per hyperscale data center. Each position was around 25 to 30 kVA or kilowatts, about 20,000 square meters each. That was the hyperscale data center; that's a high-level view.

We had regions like northern Virginia, Dublin, OH, and Oregon; those were our big hyperscale regions. However, we did have hyperscale data centers in other regions, but they weren't as prevalent. For example, in Oregon, there were 27 hyperscale data centers, and in northern Virginia, there were around 32. In Dublin, OH, there were 12, as it was a relatively new region. However, we did have colocation agreements in some regions because they had to be in the metro area, such as, for example, in Seattle. The entire Seattle region is colocation, and we had deals with Digital Realty, Equinix, and TierPoint. In San Francisco, we had only two hyperscale data centers under our build and own. Still, we also leveraged Equinix and Digital Realty Trust in that region. So we had a hybrid model with colocation and Amazon-built and run.

### Colocation means you rent capacity in someone else's data center, and the other one is that you control everything entirely.

That’s correct.

### And you still run it, or are the premises purchased and owned by Amazon?

No, we would rent. We would lease the space from an Equinix or a Digital Realty. There were a couple of models of leasing. In one, we let them run the facilities, like the air conditioning, the power distribution units, the generators, etc. Then in some cases, when we took over the whole place, they would lease us the entire facility, and we would manage all the facility infrastructure ourselves. We worked with a couple of different models in the colo market.

### For the hyperscale ones, would you rent or purchase the land?

We'd purchase. When we put a hyperscale data center down, we own the land, the building, and all the infrastructure; that's all ours.

### Can you run me through the economics of running a data center. How does it look operationally and financially?

The data center is built. Just as a data point, it costs about $1 billion to build out a hyperscale data center just to get it ready to start taking in your first rack.

### One billion.

One billion to open up one of those 20,000 square meter facilities.

### What about the other ones for colocation? I guess that will vary more.

It really varied, yes. It’s definitely not a billion. You’re on an opex model at that point; you’re paying for power and square footage of space. We would pay as little as $10,000 a month for some smaller ones or up to a quarter million. That’s a real variable. But when it comes to hyperscale data centers, we have it very tight.

### To have an idea, you said a third, a third, a third of revenues is going through that region. Could you say what revenue share comes from hyperscale and colocation facilities?

> Yes; 60% of our revenue was delivered through services in hyperscale data centers. The financial part of running is paying for people who are not necessarily the easiest to find and train. You've got a whole people cost. You're spending about $1 million in salary and benefits to run an entire region. You also have your facilities, probably your biggest cost, because that's where the power comes from. The more servers you put in, the more power you consume and the higher your cost. Having a full data center will cost a billion dollars a year because of your racks.

> Earlier, I mentioned you put about 700 racks in one of these hyperscale data centers. Each rack is $400,000 to $500,000. It is not cheap. When we have semis come up to roll out 12 racks to be installed, you're looking at $4.8 million worth of racks in one semi. That's an enormous cost, your compute. However, we depreciate that over five years. If you've got 700 racks and your average cost of each rack is about $400,000. That's a big cost. The next one is powering them. We look at each rack taking up about 35 megawatts. I'm trying to extrapolate my costs for each rack position here. It was probably about $500 a month per rack, $30 million per year. So $100,000 per megawatt is what we used, so $30 million a year in power for a fully loaded data center.

### How does that change when energy prices change? Do you lock in energy prices? Do you have hedges on for that?

We sure do. We have a lot of influence. When we go into a region, we will hedge our prices. For example, the Oregon data center is 100% hydro-powered. It comes from power plants that are up and down the Columbia River. We can lock in power rates, and that's not fossil fuel-based; that's what we like there. However, in many other regions, we don't have that luxury, it's fossil fuel-based, and you get higher energy costs. But the most is about two-year hedging that we do for that. We do that, but we also enter into some very aggressive decommissioning programs, implementing power-saving processes in technology, and we'll raise the temperature in the data centers. Believe it or not, raising the temperature in the data center by one degree will save us $1 million a year. We do a lot of different things to hedge increasing power costs.

### Wow. A quick follow-up question in the same line. Is cloud computing, running data centers like that, more energy efficient than on-premise infrastructure?

Absolutely, without a doubt. Say you're doing on-prem for your company, you're an Autodesk or a GM, and you've got your own data center. You don't use the full capacity of your infrastructure. By using cloud computing, you are divvying it up with multiple customers; therefore, you are utilizing it much more efficiently.

### That's what I always thought. Still, I was thinking about energy efficiency because that utilization is just higher. There are multiple parties from a central place; it's just more efficient.

Are you familiar with PUE?

### I’m not, go ahead.

> PUE is power utilization efficiency, and it's the number one metric data center operators have to report. That means that what percentage of the electrical load is attributable to computing versus other things that could be in there. You’ll see numbers that are less than one, and you rarely see them higher than 1.8; 1.8 is bad, and anything less than one is extraordinarily good. Most companies come in around 1.1, or 1.2, which means the ratio of compute power over the amount of power that’s provisioned. That’s a key metric that you’ll watch. You’ll find that the lower the PUE, the more efficient those data centers are, and they're probably the most successful ones.

### We were talking about the economics. You said the investment, the people costs, the energy cost, the compute cost, the racks, the servers, and the infrastructure. Those were the items. Then how much else do you plan financially? I guess now you have a data center. How much out do you plan the capacity?

From beginning of a data center release, you go through your phases or commissioning, and it's ready to start taking in rack one. It takes, on average, about two and a half years to reach the full capacity of a live data center. Then you get a really good steady run rate.

### Two and a half years from commissioning to being fully ramped and efficient?

Yes.

### How much time does it need from commissioning to the first workload?

No more than six months.

### How much in advance do you plan we're going to open locations X, Y, and Z?

That is planned a good three years in advance, so I could tell you in 2022 what will be built out in 2025. It's a three-year lookahead.

### What does a business plan look like for the additional investment?

> The business plan is to invest heavily in your larger regions. I keep bringing up northern Virginia, Dublin, OH, and eastern Oregon. The plan is to continue to build three hyperscale data centers per region every 18 months and not stop. We've bought enough land that it will handle it for 10 or 15 years' worth of growth.

### How is it tracked that that spend is officially done and that it ramps? Or is the question not asked because consumption is going through so much?

You took the words right out of my mouth. It's a linear consumption model. It's like that movie, you build it, they will come, that's how we ran it. We knew there would be demand, and we would even have racks backed up because we didn't have space for them, which drove my customers crazy. We always had demand for racks. Any time we opened up a new data center, I can guarantee semi trucks were coming into the loading dock every day, dropping off 12 brand new racks for that data center for about the next six months.

### We have these three clouds; let's take AWS for simplicity. When the figures were disclosed, they had a useful life for servers and network equipment of three years. Over the past two or three years, that has gone to four, then five, and now to six. Funnily enough, all of them are following, and Microsoft and Google are doing the same. Could you please explain why that is, what’s going on there, and what it means?

> There are a few reasons for that. This was always at the top of our conversations when managing the regions. One of the reasons you are set with aging infrastructure is that the service you're providing on a six-year-old server only runs on that server. The bottom line for a lot of what I’m going to talk about comes down to human resources. One, developers aren’t developing some of the legacy products into the new server architectures because they have to make code changes to run from, let's say, a 32-bit machine to a 64-bit machine.

The other reason is that the people who would migrate the applications and data from old racks and technology, like a six-year-old one, are the same people doing the developing, so it's prioritization. There is no priority at Amazon to migrate services from old racks to newer ones because a lot of work needs to be done when you do that. One, you have to be sure there is capacity for it and, two, you’ve got to make sure it's compatible. You can't just expect your code to work on a newer technology platform than it's been running on for the past six years. That's a big one right there.

However, there was a push to do a lot of server decommissioning. I've noticed that once these racks hit three years, you see higher failure rates with hardware, and at a certain point, you can't get parts from the manufacturers for these older racks. Once a rack gets to be about five years old, getting parts for it is extremely difficult. Red flags go up saying, okay, you didn't prioritize it earlier, and now it's a fire drill. The application teams have to reprioritize their software development activity, so they can work on porting the old code so it can work on the new code.

### Who are the main providers for the hardware? Are you getting the servers from HP or Intel?

> This is the special sauce; Amazon does not buy servers from anybody; we build our own. When we first started up in 2007-2008, we had a partnership with Dell and IBM, and we started on that model. But the way our growth went, they couldn't keep up with us, so we ended up building our own.

### Is that true for the others, like for Microsoft and Google Cloud? Do you know?

I have colleagues at Microsoft who are more of a hybrid. They build some of their own, but they're not exclusive like AWS. Google is more of a shop that goes and buys its own. They'll have partnerships with HP, Dell, and IBM. However, some of the things you run into like that are security issues. IBM had some serious security breaches, which raised many flags. That's another reason we didn't go with other providers for servers and did our own.

### What are the suppliers? What are the dependencies that you have? In my head, I thought you would get the servers, but you don't. What are the inputs that you need? Is there a supply risk somewhere?

> Yes, it’s at the component level. We would use NVIDIA for chips. We had big contracts with NVIDIA and Intel; we would get motherboards from Intel and ASUS. Then you’ve got different memory suppliers. A lot of them would be the standard memory suppliers. Fujitsu was one of our biggest, and Samsung was another big memory supplier we leveraged. But memory is very in flux, and this is key. If you look at memory, it is very volatile. Sometimes you get bad batches, and I’m talking about tens of thousands of memory sticks with high failure rates, which is a big problem. We talk a lot about CPUs and data center CPU. I think the issue is with data center memory. That would keep me up at night, the high failure rates, because that would drastically affect capacity.

### Why is Amazon not doing that itself, chips and memory?

I think we understand that we leave that to the big boys; it's not in our core competency. We won't make silicon; we won’t make the memory. We’re going to continue to buy that.

### The Graviton chip, how would that impact your responsibility and role, and what is AWS trying to do there?

You're the third person that's asked me about Graviton in the last two months, which I find very interesting. We hadn't embraced the Graviton technology when I left there in 2021. I would say that if we have it now, AWS runs Graviton; however, it's for our EC2 instances, and we're finding that it's a big performance leap over what we had before. Our Graviton is slowly increasing. I imagine we've got six-year-old racks in there right now, so it will probably be a good couple of years before it saturates our data centers, but we are making a push into it. We're late adopters of the Graviton, but it's fully embraced now. It's going into a bunch of servers; I mentioned EC2, and it goes into Aurora, ElastiCache, Lambda, Fargate, and so on. It’s going into a lot of the services currently. Graviton is a big player going forward for us.

### What does AWS do with Graviton? Is it their own chip?

Yes. That's something we design and customize to our services because we embed a lot of our code within the chips to make them more efficient. A lot of it helps gaming.

### So you would get the silicon from the suppliers, but you would custom-design it with Arm?

That’s right.

### Who would build it together?

That would be Intel.

### That is interesting. You said before, if I understand correctly, those applications or services have been designed and deployed on servers that are, let's say, five or six years old, and the migration to newer technology is trying to get pushed out. That's one of the reasons that useful life has been pushed out because you realize you can run these things longer on the old technology. Is that correct?

Yes, that's correct. One of the problems we face is that racks we put in six years ago probably only use 15 kilowatts per position. We've got racks these days that handle 35 kilowatts, over double. It's so inefficient that we look for opportunities to decommission the racks that are taking up space and consuming less power than a higher-density rack.

### Even when they're not fully written down, you would do that?

Yes, that’s right.

### And you would sell those to a third party?

No, the security around a decommissioned rack is off the charts. We literally shred and destroy the rack.

### Wow; you would take a write-off charge to be able to get more out per square meter.

Yes, that’s right.

### You said there are many reasons for that. I understood the first reason. I guess the second reason is evident from what you just said: newer things that come into it are more productive, they’re faster, have more storage, and they can run through more compute. Are there other reasons why that useful life has been expanded. I was wondering whether there is some software improvement behind it, too.

There is reliability. If you looked at racks built from 2010 to 2015, you wouldn't get the life out of them because they just weren't as reliable. We're making racks a lot more reliable with standard components. Parts are becoming more interchangeable with racks; for example, a fan or a memory module will be the same across different types of racks. We're getting to where you are not as specific on your replacement parts. For example, a motherboard will be compatible against three different rack types instead of one, or memory modules will be the same for 80%. It comes down to the component level.

### That’s not an accounting play. When I looked at AWS four or five years ago, I thought three years was very aggressive accounting. Aggressive in the sense that it’s depressing current profits because I did not expect them to buy their servers in this infrastructure just for three years. So I thought the cost would be lower than what is being recorded, which has proved to be correct. My question is, now, how will that look? Is that also an accounting play because that way, you depress profits and hide how profitable you are? Is that something you've come across?

No, you have to take in accounting, but that is not the driver. Everything is based on services, and the one thing about Amazon that always impressed me was the quality of service and customer obsession. Whatever makes the customer happy, whether it's high availability or higher performance, is what we strive for.

### Your customers were the services.

Yes, that’s right. And their customers were the external folks. I was rarely approached by finance to say, we’ve got to do a high decommissioning project to get rid of these racks. That would rarely happen.

### What would that useful life be five years from now?

> I managed eight-year-old racks in one of the regional PDX regions. It was very touchy. It was trying to run it at a steady state, and we'd have a special parts area. I can't imagine that we would let anything go past eight. You're taking way too many availability risks. We would raise an alert to the application group; once it gets to five years, you start to raise red flags. It would have to be such a custom app that had to run on a certain technical rack platform to stay past that, and there’s not much of that out there. I don’t see it ever going over eight, and I don't see it much going over six.

### That’s interesting because it’s there now.

Yes.

### It’s interesting because the way you talk and where you’re coming from reminds me of the old separation of hardware and software, which you almost forget when you talk with people today because they don't have to do that type of work anymore.

Yes.

### That's the magic you provide behind the scenes; I think that's also what Amazon has always been saying. How much of the improvements we see on the hardware side are actually software driven?

We would come out with new features. I'm also a certified architect with the services. I would see with Amazon that our services were constantly evolving and being rewritten. We listen to the customer for features and performance, and I would say that our applications and services evolve so much faster than the hardware. The applications will leverage the hardware more efficiently as time goes by, with new releases and so forth.

### In the public filings, we can see that square footage has increased over the years. This is in line with what we’ve discussed, about 26% per annum over the past seven years. Revenue per square foot, you've been able to get more out of each square foot of revenues. Can you explain why that is?

When you try correlating square footage to revenue, it is not necessarily all computing. For example, in a data center, 60% of that square footage is to compute square footage and 40% to your facilities, like your HVAC units, your power distribution, and your generators.

### So the computer part, the 60%, comprises storage, applications, everything that is basically on top?

Yes. You have a lot of space allocated in that square footage number that's associated with facilities. Even if you take that out and say, I'm going to try to increase my revenue proportional to my square footage of compute space, that might be more. In terms of increasing capacity from a compute perspective, we were always under the guidance to never go over an 80% utilization because you have spikes; you have to always leave headroom. You will have wasted compute capacity because of those requirements to have an overhead purpose. That will play into not being in lockstep with your square footage growth because you'll always leave a little bit out there for overhead.

### That makes sense, but how could you get more revenue out of each square foot over time?

It’s because of the technology. We used to run 15-kilowatt racks, and now we're running 30 to 40-kilowatt racks, which has a ton more computing. Your IOPS are higher; your processing is higher. Just by Moore's Law, you'll get more computing out of the new technology. It's going to eat more power; it's definitely going to eat more power.

### The increasing profitability we've seen over the past years at AWS, I suppose a big function is also a function of Moore's Law. The cost side can be managed more efficiently, and you can just get more out of it. What are the other drivers if you’re familiar with that?

The costs of components in volume go down. Virtualization technology helps us get more efficient by leveraging our service across multiple racks, for example, with software that would make us more efficient. Stuff like that.

### If we go to the last question, when you look at capex per square foot, that has been volatile. You cannot read if capital expenditures have gone up or down per square foot. Do you have some data points or some insights on that?

Yes, with capex, I can totally understand how that can be a variable. The way racks are engineered or architected; they're not all the same.

### What goes into capex? It's everything you purchase, including land and all the components for you to build the infrastructure.

Yes, and you also have to include facilities in capex. PDUs, generators, and HVAC units are expensive, which is a big play in capex.

### This goes into the server part for which we have discussed useful life, right?

Yes.

### The land, I guess, has an infinite useful life once you own it. And the facilities, how long do they last?

A facility lasts a good 20 years.

### So that goes into capex. And how can you understand that it’s variable?

From a compute side, you'll get a lot of variability because you build racks for the services. You could have some racks that are heavy memory or heavy CPU, which will be more expensive, but sometimes you don’t need racks that are that huge. People go out and get EC2 instances that are M2 mediums or smalls; you don't need that high power, so there will be a lot of variability in that. You’ll see more variability in the rack types. The average rack is about $400,000. However, I've seen racks come in that are about $800,000, and I've seen them as low as $100,000.

### But does capex tend to go down? Is it something that’s more inflationary or deflationary?

It’s interesting. You’ll get more from a rack at the same price from an IOPS perspective.

### I guess facilities and land have become more expensive.

Yes, that’s one thing that is a given; your facilities costs rarely go down from data center to data center. That’s always increasing.