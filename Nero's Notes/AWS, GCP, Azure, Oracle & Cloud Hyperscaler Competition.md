# AWS, GCP, Azure, Oracle & Cloud Hyperscaler Competition

by #InPractise 


Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### I run an investment firm that invests in publicly traded companies, and my strategy is to find the best growth companies I can understand, buy them cheap and hold on to them ideally forever. The strategy being informed by the observation that there are some special 99th percentile companies that you can make one decision to buy, then that's it, you just hang on and they do all the work for you. I'm trying to find a few of those.

### I do recognize and to some extent understand the distinction between infrastructure, platform and software as a service, so you can assume basic knowledge of that terminology. I'd love to start with a brief background on your responsibilities at Microsoft, Oracle, GCP and Salesforce, to the extent they're relevant to this conversation about the public cloud.

I was one of the few people who actually got to see the launch of Azure. It was called Red Dog in the early days and it was an extension of Windows Server into the internet. Then they made the corporate strategic decision to launch it as an infrastructure service. Back in those days, Microsoft's bread and butter was Windows Server and Office, but the key to drive that ecosystem was applications. Just like the iPhone, the apps make it cool. In order for them to get the apps developed, they needed developers. This was an era where people switched from Java to .NET, and it was ubiquitous across all environments and sectors. They realized it was tricky because these developers had their own services and Amazon was testing EC2 and it looked like they were gaining traction. Selling infrastructure is a lower-level stack, so why don't we do that instead. That's how they gained market share and caught up with AWS.

### What year did Microsoft go to IaaS?

2010 is when they start talking about it, but they switched to PaaS in 2013. In the early days when we were starting to launch Azure and competing with AWS, people feared the cloud because they thought they could do it better. I remember talking to many CIOs who asked me why they needed to spend money on the cloud when they had recently spent $2 billion on a new datacenter or upgraded their SAP. SAP is a mission critical application which runs core financials for many businesses. If they spent $50 million upgrading it, why would they need to invest in the cloud? People didn't realize the benefits, agility and security. The economies of scale these hyperscalers can do is so much better than a company.

My clients were Fortune 50 customers which included Exxon Mobil and Chevron in the energy space and large banks and retail. Whenever they make a change, it takes a long time. Today everyone is on the cloud in one shape or form. Having said that, we're still very early and I could tell the maturation of the cloud, having spent almost a decade at Microsoft and seeing how people started ramping up to the cloud. It all started with infrastructure, meaning basic compute, network and storage. Then I noticed them going to the data layer by putting their database onto the cloud.

Oracle who at that time was one of the largest database companies in the world, shifted onto the cloud. When I was at Oracle, I realized how late Larry Ellison's strategy was, because he is very arrogant. I think his hubris let him down thinking they will never get off Oracle. He even challenged AWS and said Amazon would never get off Oracle, but they did it within 18 months. They shifted their ecommerce database consisting of millions of customers with billions of SKUs, over to Redshift. Then they realized they needed to do something about it, but it was too late.

### Could you tell me about your responsibilities and prognostications for Oracle's future as a cloud provider?

I would not put Oracle in the same category as AWS, Microsoft or GCP, because it is more of a SaaS offering. It is in the same category as Workday, SAP and Salesforce. My role and responsibility was the go to market lead for Exxon Mobil. 50 people reported to me in upstream, mainstream and downstream components. I went there because they had a large Oracle footprint on the database side, but they were shifting over to SAP HANA. They were taking bits and pieces of what they call the department applications to AWS and Azure. Everything they were doing was cloud.

I remember we were battling with Workday and the core HCM, whereas it's so much easier to buy a SaaS. Before Oracle I did the same thing at Salesforce for a year, and sold Exxon Mobil their very first CRM. They were getting rid of PeopleSoft and other on-premise applications. I see that as a trend that these companies prefer to go to SaaS, because it's so much easier. If you're going to invest in a company, I would invest in a consumption business versus a user-based business. Are you familiar with the Rule of 78?

### No.

The Rule of 78 is very important for cloud consumption. This is the reason why companies like AWS, Azure and GCP can grow at a much faster scale than someone like Salesforce or Workday. When you have a user model, you're limited by the number of users. If you have a user model as big as Exxon Mobil was, they only had 20,000 users that actually used a SaaS application, you can't grow that. Walmart have 100,000 employees, but they are not going to double that in a year. You can with a consumption model because the number of applications being built can double or triple. If you want to look at companies who have faster growth in the cloud, you have to differentiate between the pure SaaS Salesforce and Workday, versus consumption which has IaaS and PaaS. That's why Azure, AWS and GCP have such a stronger value proposition. Take a look at that Rule of 78.

### You were about to talk about when you went to GCP then I derailed your thought; let's go back to that.

One of the things is Thomas Kurian.

### Did he recruit you?

Not directly, but I had a chance to work with him because he was the executive sponsor of Exxon Mobil. Thomas Kurian was Larry Ellison's right-hand man and he wanted to go ahead and adopt cloud in more of an open partnership. In other words, let's partner our key applications with AWS, Azure and GCP. Larry Ellison decided to build our own cloud infrastructure which they called OCI or Oracle Cloud Infrastructure, which didn't go very well. It's interesting because if you read a recent article, Larry and Satya had a partnership.

### They announced it last week.

Two weeks ago, but it was two years too late. When TK went to Google, what he did was phenomenal, and Google owes their success to his strategy and vision for Google Cloud. He realized that AWS and Azure, even though they were first and second place, were not as open as he wanted with other clouds, so he created this very open framework called Anthos. Are you familiar with Kerberos and Kubernetes?

### Yes, I am.

Kubernetes is the container system which allows you to containerize things similar to Docker. Think of Kubernetes for clouds, where you could take that and put it in a container and move the VMs from AWS to Azure or GCP, on prem or the cloud. That offered customers choice, and what they realized was these customers, especially large enterprises, were on multiple clouds. Offering that flexibility to move an application from one cloud to another was good, so Anthos became a key player.

Google's business model is about capturing data and turning it into a profitable ads business. 80% of Google revenue comes from the ad side like YouTube data. They already knew how to capture that data and use AI and ML. They took those learnings from the Google side and engineered them to the cloud. When I was at Google, our pitch was that we had best in class data analytics. BigQuery was our flagship we were trying to pitch, and we had the most advanced AI to wrap around those products. That was our differentiator.

Microsoft, being born of the traditional on-premise Windows Server environment, were best in class with what we call hybrid. We have applications and environments which are on-prem and in the cloud. They have all the tools to do that seamlessly. AWS had the first mover advantage and have 200 to 300 product offerings in different categories. On the database layer alone, there are seven. They are by far the most mature. If you look at Gartner's magic quadrant, AWS is still the leader but Microsoft is catching up. They're all considered industry leaders.

### It sounds like TK's strategy was multi-cloud and focused on data analytics; is that a two-pronged strategy and how did that land with customers?

The sales motions would have been, let's try put them in vertical industries like retail, manufacturing and industries. Let's focus on specific geographies and at first, we have to evangelize. Customers would say, I'm already an AWS or Azure shop, why do I need a third cloud? In the US people remember Ford and Chevy, Toyota and Honda or Coke and Pepsi, but no one remembers Coke, Pepsi and Dr. Pepper. We had to do whatever we would to be in the top two. The differentiator was you have this huge data you need to consolidate into a data warehouse and we had the best-in-class tools and the most intuitive interfaces, plus we can leverage data on your ads business, because many customers were spending millions with us on ads. Why don't we leverage that data to give you more of a 360 view of your customer and partners?

Walmart didn't want to be on AWS, but it was still very strong and it was proven. There was a lot of organic support around developers and IT loyalists, because they got certified on it and had been doing it for years. We spent a lot of time helping people get certified on GCP, and they evangelized to help grow that grassroots effort. We would talk to businesses about providing value. We also needed to ensure we partnered strongly with the ecosystem partners, ISVs and key applications. For a lot of these big businesses, SAP is still the most mission critical. If they said we run good on AWS, Azure or GCP, that adds strong credence to it. We had to ensure mission critical apps drive the thought and mind share of these executives, to endorse us.

### What will the market structure look like 10 years from now? Who is most likely to be number three? Is it GCP or someone else?

No, it's still going to be AWS, Azure and GCP.

### Will they dominate forever or is this going to fragment slightly over time?

I cannot see anyone taking market share because of the capital required to build out those data centers and infrastructure network. Apple could do it if they wanted to, but do they really want to get into that space?

### Is the Oracle Microsoft partnership announcement an admission of defeat?

They need Microsoft more than Microsoft needs them. The partnership wasn't for the SaaS applications; it was so they could run Oracle's autonomous databases on Azure. Microsoft have Azure, SQL and Synapse. Amazon has Dynamo and Redshift. There are many of these depending on the workload. If I'm a Microsoft customer, why do I want to set up an application on Oracle? The only time I will use Oracle is if I'm moving an Oracle application and I cannot transform that application into Microsoft apps.

> If you have an old legacy retail database with customer data from the 1970s and it's running on an old Oracle SQL database, then you have to move that over. It's easier to take that database and put it on Azure infrastructure, but that's going to be fading away because they will retire and move that database to a modern cloud database such as Snowflake, Databricks, Redshift, Synapse and Microsoft. As much as I enjoyed my time at Oracle, they have struggled to catch on. When you're behind in this cloud journey, these companies are going 100 miles an hour. You're just getting up to 50 miles an hour. You saw how AWS grew 30% over the last quarter?

### Yes, it's incredible.

That is on a large base, so even GCP has to grow 80% to 90% to catch them. They're so far ahead and the base is so much bigger. If GCP is growing at 40% to 50%, or 10% faster, it would probably still take them 10 years to catch up. They did five or six billion and AWS did 18 billion. It's crazy how much bigger they are per quarter. It will remain one, two and three. I don't think there will be another coming player, but you have to look at companies like Snowflake and Databricks, because customers are always focused on data.

### It seems like Databricks and Snowflake are changing the dynamics in the industry longer term. What do you think about the adoption of a cloud on top of the cloud? How will it affect the businesses of the three clouds we've been talking about?

The PaaS layer includes operating system, middleware, run time and data. Some people put data in the SaaS layer, but I put it in PaaS because when you are developing applications you will need data. From a company's margin profitability, those higher-level services have increased margins. When you charge a customer, you have to review the price sheets. There are public price sheets from all cloud vendors. If you run a data analytics or ML tool, they charge much higher. Core infrastructure of compute, storage and network is a race to zero, economy of scale and commoditized. The way that customer will make money is by charging the higher margin businesses.

### I would love to demystify where the revenue and gross profit dollars come from. I've heard the core compute storage networking is 75% of revenue and compute is the biggest piece. In terms of margins, storage is often sold at a loss, then comes compute, then the higher-level services are where a lot of the profit pool is. Could you share anything that would help me get more confident framing around those things?

It's hard to break down what is the proper margin on IaaS compute, as they don't break it down that way. You have to run a pricing calculator to see the model. Everybody has a pricing calculator and I'll share some links. When you go in, you put a VM in and you can see the cost for the infrastructure service is $500, but as soon as you add data and AI machine learning, it becomes $1,500 or three times more.

### Many people conceptualize that profits are made on the higher level, but since it's consumed in the way you just described, many people worry whether the cloud providers themselves will over the long term be providing those services, or whether they'll be competed away by independent software providers or others. If that happens, don't cloud vendors simply raise price on the underlying IaaS?

To get to the higher-level services, everybody needs the underlying IaaS. From that perspective, 60% of AWS revenue comes from EC2 and storage, because those are the fundamental building blocks, but those higher-level services would generate more margins. If I was AWS, Azure or GCP, I would introduce as many high-level services as possible because they're already going to be on our cloud. Then I will to try to make our cloud as sticky as possible so they stay on it, and we'll charge them a migration tax to make it very painful for them, should they decide to migrate.

### The egress fees?

Not only the egress fees, but the license mobility fees. Microsoft did a clever trick earlier; they said if you're going to run our SQL server application on AWS, you have to pay a penalty or tax. Large hyperscaler companies can manipulate the egress and licensing fees to make it sticky. From a technology perspective, it's just as easy to move from one cloud vendor to another. All you need is to establish an ETL transaction, which many companies offer, but the cost of licensing is very expensive.

### It feels so punitive for them to keep customers by charging them to leave? Is that sustainable?

I don't think it's a good business model but cloud is about driving down cost and raising efficiencies. Why do you want to move from one platform to another? It's the same as why people are still on mainframes after 50 years. When you book an airline ticket, you see those people clicking 20 keyboard strokes to change a seat, which is due to the Sabre system that's been around since the 1970s.

### Was there a feeling inside GCP, Oracle or Microsoft when you were there, that margins are constantly at risk and what do we do to keep people on and margins up, or did you have confidence in long term profitability and it was just growth?

I think it was growth, because the pie is getting bigger. We had enough room for these cloud vendors to come in. Gartner, Forrester and McKinsey can tell you how big the total addressable market is for cloud service. We're still in the very early days. If this was a baseball analogy, I would say second innings at best.

### Really?

Yes. Many Fortune 50 companies still have the majority of workloads on-premise. Once they get the attention of cloud natives like Uber and Netflix, the majority of Disney applications are still on-prem, so they're moving more digital and trying to be like Netflix. It's the same reason why we cannot retire mainframes. The Sabre ticketing system for travel is still based on 1970s technology, as is the core banking transaction which runs the ATM network. The reason it is so hard for those applications to be moved is because of 30 years of business logic coupled together. They have many different systems so you cannot simply uncouple one.

Any new applications will be more cloud native, microservices using Kubernetes, Dockers containers and serverless functions which can now be on cloud. The majority of that on-premise stuff is still early. Every keynote from AWS Reinvent, Thomas Kurian and others say the same thing, we're still in the very early stages. AI and ML get a lot of attention and are buzzwords, but most companies are still running basic analytics with dashboards and reports.

If somebody figured out I how to predict or run a model to see where oil would be in the next five years, they would be richer than we are, but no one has. Even with all the quants, capacitates, multi color simulations and advanced algorithms, no one can figure it out. There's tremendous opportunity for the cloud. More businesses are using cloud applications to replace core back-office applications.

Salesforce was one of the first ones to address CRM and took out PeopleSoft who were the on prem leader at the time Salesforce came in. They did a good job because they made it intuitive and easy. I remember the first time I went to Microsoft, we were a CBO shop, and it took 10 minutes to add one opportunity in, because there were 40 different screens and clicks. Salesforce is like, boom, boom, boom and you're done. Many companies use Workday today whereas before they used PeopleSoft or Oracle Human Capital. Workday is so much better. ServiceNow are doing IT service management which is much easier. In future, more applications will be moved over, but the core business applications like the finance of your bank, the stock trading application or the ATM or SWIFT network that moves money from A to B, all that still has a long way to go. We have to help ISVs move them to the cloud.

### How are Databricks and Snowflake shaking things up?

Both of them are good in that they don't care what cloud you are with. Nobody likes vendor lock in; people like choice. Are you familiar with the difference between a data warehouse and a data lake?

### I read the definition multiple times, then it slips out of my mind.

I was guilty of that too, using this word interchangeably. Think of data warehouse as taking all those silos of data, putting them into a central repository or data warehouse, then running dashboard analytics or BI tools like Tableau or Power BI. If you're an executive of Goldman Sachs and the CFO asks you how Asia Pacific is performing in the bond market, you can show that up. Companies are starting to do that now, so they try and receive benefits, but if your CFO at Goldman Sachs asks you to build a model to see what the impact of China taking over Hong Kong and Taiwan will be and how that would impact their industry in the Asia Pacific market, that would be a good analysis.

> You couldn't simply build that on a data warehouse; you have to add AI and machine learning, then employ data scientists and engineers. That you have to put into a data lake, which is a different technology architecture. Snowflake is good on the data warehouse side and Databricks on the data lake side. Companies would move data from the warehouse from A to B, run the model, then put it back. They do a lot of this moving back and forth. If you want to invest in a company, Fivetran are a data migration company who do a good job of those things. Whoever can figure out how to create a unified platform that is database, data warehouse and data lakes, would probably be the company that is going to be the next wave of data analytics. They might be like Oracle when Oracle first came out. Everybody was on Oracle as they were first to use relational SQL databases.

### Will Databricks or Snowflake be that company?

Databricks probably has the lead as their technology is much stronger. They are all research academics from Cal Berkeley. Snowflake is good on the data warehouse side and they also have very strong marketing. People started using Snowflake earlier than Databricks, but originally it was sold to different audiences. Databricks is more of that data science, looking at foresight versus hindsight. Snowflake caters to the data analyst on the business side, looking at sales performers by region, product and SKU.

Keep an eye out for what they're doing around Snowflake data cloud. There is talk that could be the fourth cloud, but those companies will definitely disrupt and take market share from Oracle. They're already losing market share to Redshift, Microsoft and GCP's BigQuery. Legacy applications which cannot be lifted and shifted over, have to be rewritten, and if they don't have time to rewrite them, they can simply move them over to Azure temporarily, and budget and road map that sooner or later they have to retire the application, rearchitect it and make it cloud, using microservices and Kubernetes.

### Can you help me understand the competition between a BigQuery or Redshift and Databricks and Snowflake; how would they go head-to-head?

It's about use cases and workloads. If you're running a spiky type workload that goes up and down a lot, Redshift is better, whereas if you're running more real time like IoT or streaming, BigQuery is better. People think it's a cloud database and everything should be the same, but not necessarily, due to underlying architecture and the way clusters and VMs are set up, as well as licensing, which plays a big part. Some charge when it's idle while others only charge when it goes up and down.

### I forget what the description of a BigQuery appropriate workload was?

I will find a slide which compares the different types of workloads and share that with you at the end of this call. If you're running a NASDAQ transaction that has to be real time versus every 20 to 30 minutes, it has different architecture. Why spend more on millisecond transactions when you don't need to?

### I keep thinking of your comment about if an enterprise already has AWS and Azure, why do they need a third. Were there any case studies you were involved with or observed while at GCP where a customer said they need three, and GCP became a significant part of their spend?

We went after companies who had the most business on the Google side as a way to get into the executive table.

### Were they advertising a lot?

Yes, and those are traditionally CPG retailers like Proctor & Gamble, or Target, [[Home Depot]] and [[Nike]]. They were already spending a lot of money with Google who had a lot of data, most notably of their customers. Google uses analytics to deliver custom ads with either YouTube or Google recommendations, similar to what Amazon does with their recommendations of other customers bought this.

If you look at Amazon earnings, the ad business grew exponentially, but they want to get into Google's game. We took that same play book and said, how do we take that data, put it into your hands so you are the owners of it so you can create a 360 view of your customer. To do that, you have to put it into a cloud data warehouse which is best in class, and BigQuery is a good example of that. Google is good at running their AI for recommendations.

When they bought that neural networking AI company from Europe, DeepMind, and when they beat that Go world champion, it was phenomenal. The possibilities of having more moves than atoms in the universe is unbelievable. When people saw that neural network, they know you are a leader in that space. Google was the first to do that quantum and has the smartest engineers. Applying Google's Auto ML makes it easier, because people don't have Python programmers or data scientists. During Covid, it would have been nice if they knew people were going to look for bicycles and gym equipment because they were stuck at home. They started doing these models post Covid, so maybe I should start shrinking my Peloton inventory because people are going back to the gym.

### I guess Peloton didn't do that.

They definitely did not do that; they missed the ball.

### They should have.

That information is freely available on Google Trends where you can see what's popular by geo or region. We overlay data from NIH for Covid, and from weather, demographics and socioeconomics, so you can build a very powerful tool. The problem was that it was still in a data warehouse architecture. The difference between data warehouse and data lake is technical, but to build those models requires data wrangling; you had to move data from one side to another. Google realized Snowflake was looking at doing this and Databricks was already doing it well, so they created their own data lake house called Google BigLake, which was announced a month ago.

### What are the capabilities or muscles Google need to develop for the next leg of growth that they don't currently have?

They have all the fundamental pieces for growth. It's always about getting those hundred million to billion dollar customers. The Federal Government is a huge area. That JEDI contract was $10 billion and saw a lot of litigation and controversy. There's trillions of dollars’ worth of addressable market space in the cloud. My big concern is that GCP is still losing money. Thomas Kurian is one of the rock stars in Silicon Valley. People love him, he's established and he has the credentials, but at what time would the board say, maybe we shouldn't invest as much in GCP? Amazon would not be Amazon without AWS, which generates 90% of their income. Google isn't there yet but once it becomes profitable, people will relax. They are under a lot of pressure to make it profitable, which I can see because they almost paused hiring in the GCP space.

### Was that the feeling inside GCP that we're on a race against the board's rope to spend money or is that what you would worry about?

I think we had five years.

### Inside, it's pretty well known we have five years to reach profitability?

No, to be number two. That was our goal, to be number two.

### The goal was to be number two in five years?

Our goal was to be number two so we had to overtake Azure. Everybody has at least Windows and/or Microsoft Office and Teams now, and Satya leveraged the heck out of that. They said, if you're a Microsoft customer, it's easy to add Azure. During the early days we would add Azure credits to the EEA and people would ask what the hell is this $20,000 worth of Azure? We would say, don't worry about it; we just took $20,000 off your SQL Server licensing and gave you $20,000 monthly credit. That's how we planted that seed, and now they're using it and consuming it. The consumption model continues to grow because they are number one in enterprise. Google is not an enterprise vendor yet; the majority of their income is from ads.

### Is it well understood within GCP that the only definition of success is being number two and there's a handful of years to get there, otherwise it's over?

That was the sense of urgency the leadership created for us. Thomas took over in 2019, so if by 2024 we're not number two, is he going to be fired and GCP shut down? Probably not.

### So it's not as strong as I stated it?

Yes, but we were all about KPIs, metrics and targets. We had to be number two because nobody cares about number three. That was the internal mantra. As far as profitability, ask Elon Musk how long you told Tesla to turn a profit? He almost went bankrupt many times, but at least with Google, they have enough capital with their Alphabet and the rest of the ad business to keep them afloat.

### What could derail the industry, not any particular provider, but what could make this a lot less growth or less profitable than you currently expect?

I think it's the other way round. Covid forced companies to accelerate their digital transformation and move onto the cloud much faster. Any time there are geopolitical or macroeconomic pressures, it forces companies to reinvent themselves. They cannot continue with on-premise legacy application development. They have to become more agile and respond to supply chain issues.

Look at NVIDIA and chip shortages. Innovation will get faster. Companies will buy Snowflake, the valuations are too rich now, but they need to acquire them because they don't have enough R&D cycles. Fivetran is a leader in this data ingestion moving from A to B, so don't be surprised if those type of companies get acquired. Google is already doing that with security around Chronicle, and so is AWS and Microsoft. These big companies have deep pockets to acquire smaller startups.

### This was fantastic. It was nice to meet you and I hope we can stay in touch and talk in the future; your new position is exciting so maybe one day we could talk about that.