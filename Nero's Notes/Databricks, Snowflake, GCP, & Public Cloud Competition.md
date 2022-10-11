# Databricks, Snowflake, [[Google]] GCP, & Public Cloud Competition

by #InPractise 

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### I'll start with this high-level question. Of all the public software companies today, which one would you be the most optimistic about regarding their ability to grow and prosper for the next 10 years?

That’s a very loaded question. Databricks is not public, right. I think the next Oracle/SAP fight you've seen all along will be between Snowflake and Databricks, so for a public company, I would say Snowflake.

### You must have watched these companies very closely. Snowflake and Databricks is one I follow very closely. How do you think that competition plays out? There are a lot of other competitors in the ring, too, like the public clouds; BigQuery is a big one. It's a very complex competitive environment. How do you think that shakes out?

Just about the infrastructure level, there are only two. Once you look at BigQuery, etc., they don't offer data store, database, data lookup, analytics, pure analytics, then core infrastructure to enable some of those things. I know BigQuery exceptionally well. As a background, when I worked at Advent software in development, I did get into those. We went from a flat file system to building a data warehouse.

I didn't know anything about data warehousing. We started using a startup called Sagent. As a result, somebody on the board of Sagent became my design mentor and design partner for building the data warehouse. I must have been hiding under a rock; I knew nothing. His name was Ralph Kimball. I was like, Ralph who? I had no idea that I was dealing with the father of data warehousing. The Ralph Kimball stuff is what Snowflake is based on, and Bill Inmon's stuff is what Databricks is based on, so that's the two different architectures, if you will, for data warehousing.

I learned my jubs from the Ralph Kimball side of things and built out data warehouses very early on. I understand the set of very different levels in terms of how these things are architected. There are two architectures that have been following, those traditional frameworks, if you will, as they were set up. Databricks, with its lake house architecture, is more along Bill Inmon's thinking, whereas Snowflake architecture, not surprisingly, is Kimball. They both have enough marketing profits that they're going towards each other and confusing everyone. Most CIOs, I saw this inside Santander as well, don't understand anything.

One thing I learned about banks, whether I brought them in or not – I brought in quite a few of the players – but before that, we had one of everything. There are layers and sediments just above the infrastructure level at the data management level to provide the wide gamut of data warehousing and analytics architectures for all the data rewards and everything else to get built on top, let's say. You need the capability at heart, which is all your data mesh, and all of the pieces that come in as part of what you're seeing come from Snowflake or Databricks. To me, those are the two giants that will battle each other. That fight has already been set up, but Databricks has screwed up and not gone public. They've got a bit of work to do ahead of that. I think they should have gone public; they raised the $1.6 billion in that last round. I'm not sure why that was too big to build a bridge around, but I assume they just put their books in order on the finance side and that's why they didn't go.

### I think they missed the window of opportunity there, and now they'll probably be private for a very long time. You know BigQuery very, very well. I might be reading between the lines here, but it sounded like you don't think BigQuery is competitive against Databricks and Snowflake. Why do you think that is?

> Because Google is not getting entry into large enterprises yet. It's ugly, and we were one of the first ones to come in, then they brought in TK, next phase. So Amit Singh and the team didn't quite get enterprise well when they tried to do it. I came in under Amit Singh's regime, but then Diane came, and it started to move more towards enterprise. It's still a distant number three in enterprise. People are going to pick AWS and Azure first, and what happens then is you're not going to pick BigQuery simply because GCP is last. You can argue that BigQuery has nothing to do with GCP but yes, it has everything to do with it, it's going to run on GCP, but you can get just BigQuery if you're looking at it from their perspective. But nobody's going to do that. No CIO is going to go out and buy it for any company that does a billion or over in revenue. Mid-market might, but mid-market has many other problems to deal with than to deal with multiple vendors.

So the only one who would deal with a multi-cloud hybrid environment is the large enterprise. When it's the second, or when somebody gets acquired that's on GCP, that's where it stands a chance. Selling net new into an existing organization that's already trying to figure out how much of this should I get off on-premise to cloud, they're not going to trust a non-database vendor. Databricks might have a little bit of an issue there, but Databricks is coming across more as a Snowflake competitor, and I think they should never lose that position. If they look more like an old competitor, they're not in the big accounts. This is the harsh reality. You may have the best product. I used to run the GCP cloud for startups program; at SAP, I ran the HANA startup program.

I used to get people to move over. It was a very simple equation on AWS. Once you hit hockey stick, you could hit hockey stick for two reasons. You hit real hockey stick; your revenues went up, so your server costs went up because your usage went up as well. If you were one of the lucky ones, your revenues went up, but your costs didn't go up, then you would not come looking for us. But at two places, they would come looking for GCP. I'd never even run a campaign; I'd wait for them to come in and ask us. They'd come in looking for GCP because they hit hockey stick either because of revenue or the worst case: eyeballs. They didn't hit revenue; they just hit eyeballs, which means their server costs would go up drastically. They would come to us and see that we were doing this at better performance, and 58% of the cost, and most of them would be off of RedShift or BigQuery.

When it's a SaaS startup, or it's a fast-moving business, BigQuery is awesome. Bricks has already announced that they don't want to go after startups because it's like a Ponzi scheme, one buying from the other.

### Yes, that’s a great way to explain it. Between Databricks and Snowflake, then, looking at the two of them, do you have a feel for which architecture will be a more significant market long-term? Do you think Databricks is a more prominent company in 10 years, or do you think Snowflake is?

Both of them tried to hire me, both for different reasons. One wanted to bring me in as a CMO and one as a CEO. I want to state that so I have no bias. I like both of them. I will say I took my eye off of Snowflake after saying no. I just didn't know they'd become that big. I must have been hiding under a rock because I bumped into an architect of a large footwear company whom I know extremely well, a chief enterprise architect, and an SAP customer. I bumped into him and said hey, how are things going with HANA? He said we're not using it anymore; we replaced it with something more magical. I said what? Did you bring Oracle back? He said no, no, no, we put Snowflake in. It was the second time I heard Snowflake after saying no.

Then I looked back and realized that these guys had gone through the roof. I know Databricks from its inception, from the early days. I was one of the first guys to walk into their office in Berkley when they were 10 or 12 people to say here's a problem I have with HANA; I need a fix, and you guys are the fix. The CEO, Ion, almost threw me out, thinking I was one of the SAP guys who doesn't know what he's talking about because these people come through all the time. Luckily Arsalan was in their organization; I think he was VP of customer service or something. He had done pricing for HANA at some point or some consulting things. He took Ion aside and said I know this guy; I've heard his name. We got the deal done.

I think technically, both the teams of Snowflake and Databricks are solid. One comes out of old Oracle, and Oracle has been a workhorse; we already know that. They have got very, very strong fundamentals. The other comes out of AMPLab in Berkeley, and they are more purists. Purists who have learned that to be in the industry, to be in the enterprise, they have to tone down their purist thing, maybe, to make compromises. So if, as a technical person, I was looking at it purely on purist, academic interest, I would potentially lean toward Databricks. If I looked at it from a business perspective, I have a huge deal of respect for Ali. I knew him as the VP of engineering, so I knew him in the early days. I didn't know that he would be such a phenomenal CEO; he's just killing it.

> Sometime back, I think when at Google, they were a little stuck. I brought them back in at Google to sort of move the partnership with Google further along. That was in the early days when they didn't have as much Google attention. I helped catalyze that. But he came in, took the call, brought the people, and I saw him in action. Phenomenal respect. However, I don't think he's a Frank Slootman. Now putting things in perspective, I do believe Snowflake will run a tighter business. If it's an Oracle SAP comparison, I would say Snowflake might be the Oracle, and Databricks might be the SAP; they both have done well. I don't know if this answers your question; I'm just giving you a data point.

### It’s really helpful that you know the people involved and can look at it from that perspective. I noticed that as a technologist, you didn’t take a strong stand on the architecture itself. On whether coming off of a lake attached as three is better than coming from a data warehouse perspective and attacking the infrastructure, the data platform market, that way. I'm reading between the lines here, but is there not a big difference then between the two architectural approaches, long-term?

There is a big difference, but I'm impressed. 99% of the CIOs would not know what the heck you're saying. But seriously, the problem is people won't get that, and people don't understand that. Yes, there are CPOs and enterprise architects that are in organizations that can make these sorts of assessments, but how many enterprise architects have you actually talked to?

### Yes, there’s a handful of them out there.

A handful of good ones.

### Yes.

Most of them are effectively just ghosting, holding onto jobs and titles. It is kind of interesting to see. The good ones tend to be in vendor organizations, and they're going to do the not invented here; they're going to build their own. They're not going to go and pick up one of these. They're going to go to bare metal and build on top of that. Google partners with Databricks, but Google doesn’t use Databricks for anything. That's another way to look at it. Partnering for the customer market, but for anything they want to use, they're not going to use another. Google doesn't use any software. They just build everything on their own, anything and everything.

### I hear you loud and clear. Last question around the data infrastructure market. When I asked about at the beginning, which customers you were most optimistic about, you jumped to Databricks and Snowflake. I guess that’s a statement about the size of the market there. What do you think about that? Why are you so optimistic about this market?

Because there's a sea of change that has yet to happen. These guys have just scratched the surface. Can a third party, can another company grow to that? I don't think that's impossible; a disruption could come from someone else and maybe a small player we haven't seen yet. Look at all the workloads that have to move. I've worked very closely with customers all along, and I've always been customer-facing. But when you work in the customer organization, when you see the underside of that belly, which normally, people won't show you, even when they're on the other side, no matter what, they'll still keep that firewall. When you see how much change needs to be made and they will just scratch the surface.

> After all the changes we made at a large bank, I'm going to put a number out that we managed to get 5% of it off to the cloud. There's a whole lot of data and everything, and we had our own data lakes and lakes upon lakes and a bunch of different things, so consolidation has to happen even for people who've built all this stuff on-premise. I'm not sure what numbers Databricks and Snowflake are now projecting in the cloud market, but I would say if they're putting a B behind it, they're wrong. It probably needs more of a T behind it; it’s in the trillions.

### Wow.

I just think there’s so much change that has to happen in terms of all these legacy organizations that will eventually move over, and we are looking at a twenty-year journey. In 20 years, I would expect that, if we are lucky, they will be 50% done.

### Let me use this as a segue into the public cloud discussion. What inning do you think we're in for public cloud adoption, and what inning would you say we're in for modern data infrastructure adoption, like the Snowflakes of the world? If you were to compare the two of them, is one earlier than the other?

If you want to keep it purely cloud, Snowflake, Databricks, just pure cloud because they have done these deals in enterprises where they're doing hybrid on-premise versions of this for people who don't want to trust the data centers. As much as the marketing doesn't talk about it, those deals have been made. I'm going to ignore that because, to me, that's a variation they have to do to keep their quarter going and their deals going. But just as pure cloud, and I would say the cloud market comes before the data market right now the way it stands. The cloud market is more mature than the data market.

In the cloud market itself, Amazon made a bet with EC2 and then moved to other things. Azure followed relatively quickly, not with any greatness. I guess if you're a [[Microsoft]] stack, you do well. Having said that, we chose Azure as a large bank customer. I was probably the most surprised when I opened the envelope to see who won, and I was in charge of it; I was writing the damn check. I looked at it and said, oh, great. Then I bumped into Andy Jassy and he said, I just want to know why you picked Azure first as your primary; we picked them as the secondary. I said Andy if I tell you, you will break your head on this pillar; he was standing next to a pillar.

> I'm not going to get into why we chose it, but technically Google and AWS were neck and neck, but Azure was nowhere near, but they won it because of many other things they brought into the deal. How they could talk to legal, it's a long story, but our acquisition process sort of went down like that.

Coming back to the question, Google made a wrong bet many years ago, saying we have the cloud infrastructure, and only two companies will need it, Apple and Google. We're already providing this on a friendly basis to Apple; we don't need to make this a product. They let Amazon wreak havoc. [[Amazon]] took the same thing that Google was doing but decided to productize it. That was seven years before, so they had a seven-year leap before Google came in, so that's a seven-year gap between Amazon and Google. Azure came in somewhere in between the second and third years. So that's the cloud lineage. If I'm AWS, I’ve got a very mature ecosystem, I can find anything I need, and the thing that they do very well – at Google, they're still learning – is all the stuff that comes around the product: the packaging, ease of adoption, etc.

> Google is learning and fixing the problems it had before. Even now, with Google's product, you need a Googler to run it. Not many people can afford Googlers, neither from a skillset perspective nor a cost perspective. So basically, the kitchen sink comes out. Maybe there's a bit of bias creeping in here, but for one, I don't think there’s any product better than GCP. AWS is a very close second from a pure product perspective. But the minute you bring the packaging, deployment, ease of use, all of that stuff in, security – Google's great for security as well – there's no chance. Google stands no chance of winning at enterprise. AWS has got that figured out.

The one that does the best of all that other packaging and makes it look like they've got enterprise, and that's how they win, so the other two guys don't really know enterprise, is Azure. This is interesting because if you take a step back and go back to the MISO days, with Microsoft, IBM, SAP, and Oracle, Microsoft was the joke in enterprise. They'd say, oh, it's not working; just reboot it. It used to be that way, which you can never do in an enterprise situation, you know that. But in this new world, Microsoft is considered the company that gets enterprise. I don't know if this answers your question, but I talked about the cloud.

Now you come through the data lineage that’s sort of the Snowflake, the Databricks, and of course, now there are all these players, the old players are old stack, they're trying desperately to be new stack, but it's not happening. Informatica has the new PowerCenter and the cloud, etc. Their innovation is so they can continue milking their legacy and present the customer with something that makes them look a little more modern so they can continue to get the maintenance revenue more than anything else.

### Just to follow up on Google's struggles in enterprise here, my question is, why hasn’t Google figured this out by now? I feel like TK definitely knows the problems and the areas around packaging they need to work on. What makes this so hard to fix for Google?

So TK made two bets when he came in, actually three, which were very promising. He went after industry, and he went after ecosystems. So, to provide deals to partners, he took the industry play from Oracle; he took the ecosystem play from IBM, which is if I make a dollar, somebody else will make $10 or $7 or $12. They used to say that right, SIs and partners, that was a model for IBM. The third play he did, I thought, was brilliant, but I don't know how it has panned out – maybe some of it has not panned out – which is the multi-cloud hybrid: Anthos. He took Anthos and said, you know what? We are a distant number three. We will never get to where we want to if we try to take things head-on and be the only cloud player. So let's start setting the stage that, through acquisitions, through whatever you do, Mr. CIO, you're always going to have multiple clouds and a hybrid environment, and you need a trusted advisor for that hybrid environment. You don't have to have GCP, it's okay, but we can be your trusted advisor.

That was a way to bring GCP in, of course. Wherever GCP was, whether first, second, or third, that was a good message to the CIO that maybe I could use these guys, too, to manage everything. Once you're managing everything, then you can start steering things your way. That was a good way to get your foot in the door and establish yourself. So those were the three attempts. They organized and hired a bunch of stalwarts from each industry, Hans Talwar, for transportation and logistics; they brought David White in from Goldman Sachs and your alma mater. He's become CEO and president of some other company now, a well-known company, but I forget the name. They brought in Lori Mitchell-Keller from SAP to run all of the industries, so all these people would report to her. They brought in Rob Enslin from SAP, which I think was a brilliant move, to run enterprise sales.

It was also an interesting move for me to see because Rob and TK in some way always competed with each other, one from SAP, one from Oracle, and to see the two of them together and Rob work for TK. Things have not panned out, and I can guess why. Rob's left and gone to UiPath as their co-CEO. Rob brought Lori Mitchell-Keller in, so I guess this whole structure doesn't fit inside Google, the enterprise, and the middle manager. These are individual stars. To put a manager in between or on top of them probably didn't work between Rob and all of these people, so I think he's gone.

> That tells me that the industry did not work as well. Why? I don't know, but it seems to be across industries; it's not just one industry. Maybe there's not enough content, not enough references, not enough whatever that might be. Selling from one industry is basically a reference sale, but for reference selling, you have to build out references in the industry. This was the build time for them, and they obviously weren't able to build it, or Google wasn't able to keep them; I'm not sure what the answer is. I'm assuming a little bit of everything. The guy running Anthos has gone off to become the CPO at Reddit and is running at least quite a bit of the Anthos stuff. Anthos, to me, is a dark horse. It could be what keeps GCP in the picture, but I don't know how Anthos is to explain it right now. I don't know the details, I don't know the insides, and some of what I do know is all hearsay, so I don't want to get into it.

It seems to be off the three moves. It seems to be the only one that seems to have stuck the ecosystem play in terms of winning partners. Yes, Google has got some good partnerships with Databricks and some of the others, but on the whole, where are people applying? Where Google is winning against, let's say, an AWS or Azure in terms of partnerships is that AWS and Azure already have partners in that space. It has become a very crowded space. So these partners like SADA Systems, as an example, for implementation, etc., at Google. Miles is an ex-Googler, a Zoogler, and also came from AWS, is their CTO. I know Miles well. It's an example of somebody who's doing really well in the Google ecosystem, but they were lost in the AWS ecosystem because there are so many of them, so they're doubling down on Google. There are those niche specialists that are doing well, but as a whole, Google is not able to attract them because that body of work is not there as much as it is at the other two enterprises. Does that help?

### Yes, that makes sense.

Those were the three plays, and I do think the Anthos one might be the one that saves them.

### My follow-up question is about the level of price competition in the public cloud. I'm not sure if you were hands-on with pricing policy, but Google has always had this reputation of being a price destructor, if you will, against AWS and Azure. Could you talk about the thinking behind that and whether you would expect price competition to get better or worse over time in the public cloud?

> Pricing is always a race to zero; that's the problem. How do you put enough value to keep your price levels low because as you start adding innovation, you get more product for the same cost, or you get a lower price. That's the overarching thing first. Why would Google be the price destructor? It's kind of the lineage of Google, and its drawback became its strength: the lineage was largely consumer, and the pricing on consumer was zero or close to zero.

When enterprise came in, and since consumer was making so much money, cash cow, they could feel it. Even now, Google Cloud, in the numbers that are reported, maybe now GCP is making more. But when the initial three or four billion was being reported, more than three-quarters of that would be on Google Apps. GCP was making almost nothing when they started. But Google's lineage is small and medium businesses on the enterprise side. It started with Apps. They wanted to get the Apps customers as much as possible onto GCP, not so much the enterprise.

Now it has changed to SAP workloads, enterprise, etc., but the initial push was all around getting the SMBs. If you already have them for Apps, let's ensure we get them for cloud. And their needs are not that great for on cloud. They don't need to run GCP machines; they're just starting; that is why the price was very close, more than anything else. That's the lineage of where they started out. And then it slowly crept up as they started getting more and more enterprises. I would say in the early days, Google even gave away deals they could have priced a lot higher for the enterprises that came in, and the enterprises that came in were looking at Google from a different perspective, which means they could have priced higher and missed the boat. This means they were able to do some kind of partnership that they could announce.

Everybody wanted Google Magic. At SAP, we wanted Google Magic so we could announce it at our conferences. Tired old companies like the Google Magic because it makes them look young and innovative. That's from a price-performance perspective. I still think Google is more competitive than anyone else. I say price performance because if you just look at the pure price, Google looks low. But when you look at what they throw in in terms of goals and the performance that comes out of it, for that same performance, you're paying a lot more on Azure and AWS; you'd have to throw in a lot more. The pricing is on a different scale for Google. Google is much lower than most of the others. If you're looking at a startup set, they all might look the same, and Google might look a little lower, but what you get out of the little lower is a lot more than you might get on those other two startup kits from a performance perspective.

### This better price performance on Google hasn't changed the dynamic competitively. Is the read-through that pricing isn't particularly important for enterprises in public cloud?

It hasn't been for CIOs making the decisions. We've gotten to the point where the job changes every two or three years for CIOs. We hired a lot of CIOs at SAP. We ended up bringing in many of those who were at HANA because the job just rotates, so it became like a parking area for them before they got their next gig. They want to hold onto their job as long as possible. They don't want to get fired for any reason. AWS has earned the reputation that you don't get fired for picking AWS. It's the old idea of a reputation. So AWS gets picked by default. Azure gets picked on the stack. If you want to pick Google, you have to prove why you want to pick Google, almost. Does that answer your question?

### Yes, that makes a lot of sense. You mentioned a bit about the ecosystem and partner strategy for Google. I'd like your take on how the partner approaches differ among the public clouds, especially regarding ISVs instead of the SI channel. How does the approach of ISVs differ?

Let's talk about the ISVs. I was involved in setting some of that up in the early days. I learned this in my startup program at SAP: recruit, enable, and monetize. I set it up as recruiters; how do you bring them in. Enablers, how do you enable them, both technical and business enablement, for the products they will be integrating with the product partnership or whatever else it might be? Or on a sale, how do these things work together, for which you need technical people. For the monetizers, it's not how you monetize. Your monetization is secondary; assume it will happen. It's how they monetize. You have to pay attention to that, making them want to choose you. Monetize is a broad term, which means it could be a marketing deal, press release deal, a legal deal, any of these other things in addition to monetary like adding to the pricelist of co-sale, re-sale, all of those. So in that form, how Google differs, and I don't know how this has changed from when TK came in and took the industry approach.

It used to be that AWS and Microsoft had a strict deal system based on revenue. If you are projecting a certain amount of revenue and could prove it, you got put into different deals. It was just flat based on revenue. Oracle has an industry-based system. If Oracle is interested in an industry, they might go get more partners in that industry. In the early days, we did what we called colloquially at Google the short head, the fat middle, and the long tail. With the long tail, we wanted to get the other things. Maybe put differently, it was one-is-to-one on partnerships, which were important, large, strategic partnerships, either for revenue or as a design win.

When we say design win, it means that a customer is big enough that having a partnership with them is a good thing for Google, even if it's an announcement, a press release, or what we are doing with them. Those examples would be Apple, SAP, SAP workloads, and things like that. These are the big names for a more revenue perspective or a design win perspective. So that's the one-is-to-one, and we can get into how things were structured for that. Then comes the one-is-too-few; this is where I think Google deferred from everybody else. Then the one-is-too-many was there was a very simple design principle which is kind of what the large companies do, except they don't market it that way, they don't say it.

Like SAP, they're trying to be a partner in the ecosystem, you'll get one email from them in a year, maybe not automated, and you're lucky if you get that and you pay money for it. I'm like, that's crazy, and then even in the referral relationships, you hardly get anything like that. You pay SAP money if you actually sell the product. So in that same way, my design principle – I actually set up the long tail – was if I have to pick up the phone to call the partner, we have failed. The team that is helping is more like a customer support team that is triaging and moving things around, and we should automate the first part so a third of it you don't even see. The next third, you triage, and then that last third, you bring it down to as trim as possible, so then you can interact or email and chat. So it's not a phone conversation, so you can have a support team, that was on the long tail.

The mid-part is where I think the biggest differences were in how Google operated, and Databricks is a classic example. Databricks started in the long tail, moved up to the mid-part – you can graduate from one to the other – now they are, of course, in the one-is-to-one. Mid-part is based on segments, not industries, segments. Google would look at the market and say, in what segment am I interested in making partnerships? This whole data segment is one. The storage segment is another. In healthcare, some specific aspects of HIPAA compliance could be one. These were segments, not by industry, but maybe they have been in an industry but more specific, and then you go recruit partners for that segment, so 10 to 15 of them in a segment.

### A few quick clarifications, what does a co-sell relationship look like when you have a co-sell relationship with an ISV like Databricks? What’s involved in that from Google’s perspective?

In a co-sell, first of all, it's the commits that the partner is willing to make to get a level of co-sell relationship, etc. One is the assessment from Google's side as to is this something that will further a Google product. What Google product does it sell? In a co-sell relationship, what are our customers asking for? Are customers going to go get it anyway? Then they start crafting the relationship. What it means is there are pieces in there that go here's the attainment KPI, here's what you have to meet, if you meet X, then this is the percentage of revenue share change, based on Google being willing to take a smaller percentage on higher revenue attainment.

There is co-marketing that gets put into it from a co-sell relationship. Google has not as big an intel as CISCO but has some market development funds, MDF, that it puts into a co-sell, which also means training Google's enterprise sales force to be able to do that. Let's say you’re bringing a Databricks person in to make that sale into one of your deals. You’ll have that conversation for the first time, enough training for them to do a level one before you bring in the customers who have expressed an interest, and you bring the Databricks salesperson into the level two conversation, the next level conversation. It’s almost an old model on the sales side, so you don’t murky the thing right up front when you’re putting the proposal on the table to the customer. That’s always a customer option when the salesperson is selling it, and Google drives that in a co-sell relationship. Google is always the alpha.

If Databricks brings a deal in and they bring and they register the deal so there's a deal registry, then Google supports it, and it's a slightly different structure when they go to market on the economics.

### Basically, in a co-sell relationship, and this sounds like it would be the closest relationship between a partner and Google, assuming that Google brings a deal to a partner, there's revenue share, sometimes there's co-marketing, training funds, etc. To make sure I understand, what is the revenue share?

There’s revenue share of the partner product.

### Okay.

Usually not revenue share of the Google product unless it’s a net new partner that is registered by Databricks, who is saying I'm bringing the deal in.

### That's really interesting. I didn't know that the product revenue moved back and forth that easily. I assume it's actually a one-time payment; it's not an ongoing recurring stream rate.

It’s an ongoing recurring stream that’s calculated and paid one time on an annual basis.

### Okay, that makes sense now. I understand that.

Everything is subscription, so it's all calculated once.

### Understood. A final question on the partner stuff and the last two questions overall. Around the partner ecosystem here, among the three players, it seems like AWS used to really like competing with ISVs, Google and Microsoft less so. Have any of these relationships changed? AWS is famous for going after MongoDB, going after Elastic, and all the open source guys with their own product. Would you say that's become less aggressive over time? Has Google shifted? I'm curious if there have been any major changes and approaches to competing with ISVs over time.

AWS continues what they’re doing. You can see they’ve gotten into low-code/no-code. They're getting into Honeycomb, they're getting into other things they haven't been in before. There's a general sense that, actually, the SAP founder used to tell that to my startups, don't get too close to us; we could make a left turn and either take over to you intentionally or unintentionally. That's kind of where AWS is at. I think it's more intentional than unintentional.

Google tends to have a very different ethic when it comes to that. It's typically not competing. It may buy a partner, it may acquire one instead of trying to compete with it. You've seen it with Looker, you've seen it with some of the acquisitions Google is doing because the innovation is hard to get inside so maybe that's the difference. If you're talking about a segment that had 15 partners, if they buy one of the 15, that's no worry; for the other 14, there is now competition for Google. That’s where the competition comes from, not from building it and going after it themselves. The net result is still the same, though, if you look at it. The end outcome is still the same. For the other 14, they're still looking at, oh, shit, I've got a new competitor, I've given them everything. They know everything about me; they know how to compete. How you come about it is slightly different.

### That makes sense. Last quick question here, this has been great, by the way. Apigee and your relationship here: totally different thing. I'd be curious what your review is on Confluent and MuleSoft as Apigee potential competitors if you have a view on either of them.

Confluent is more event streaming than API. Are we talking about the same Confluent?

### Yes, Kafka has been known to be used in situations that mirror APIs. I'm guessing it's not a big use case for Kafka.

It's not, and Confluent, from what I know, is going after event streaming, event architecture, event condition action, more than API management. MuleSoft is more head-on. Their genesis is very different; MuleSoft started as an ESB, enterprise service bus. Apigee started as API in a box, called Sonoa Systems. They were trying to do what I had done with CISCO called AON, application-oriented networking from TIBCO. They tried to take that whole concept of CISCO and put it out in a box with Apigee. So Apigee is more purist API management, and MuleSoft has started more from a messaging bus and POP server architecture if you will.

MuleSoft has been bought out by TIBCO. So there are only two games in town right now. Of course, there's Kong and others, but Kong is more popular in Brazil and LATAM, and maybe Europe, but not as much in the US. I can't understand why because Kong is a pretty decent product. I would not put Confluent in that. Maybe I have to go look at it again because I have never seen Confluent in that light. I'm having lunch with the CMO in a week or two.

### It's an interesting use case for Kafka because instead of doing API management and upper layer in the app, it can do the data swaps at a lower level with just the infrastructure. I've heard of a few companies doing that, not a lot so far, but I hear you, it's a very different space.

You stumped me. I now need to go look at this. I was in all of Apigee's acquisitions, so I should know the space well. We’ll see. Hopefully, there is no bias there.

### It has been really fun talking to you. Thank you for speaking with me today, I learned a ton, and you know a ton about the space, so I hope you don't mind if in the future we get back in touch at some point.

Sounds wonderful. If I can help in any way, let me know.