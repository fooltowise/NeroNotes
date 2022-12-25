# Amazon Web Services: EC2 Graviton Strategy

by #InPractise 

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### Can you explain to us non-techy people what Graviton is in layman's terms?

Graviton is a processor that AWS has designed that powers EC2 virtual machines. It's a processor that is built on top of the ARM64 architecture, which is different than the standard X86 architecture you see in AMD and Intel processors. This just means that the instructions that are used to compile your code are slightly different and the resulting binary that your code is compiled into, is only readable by ARM64 machines and couldn't run on an X86 machine. It's an alternate set of instructions and this processor architecture has some unique advantages over X86. Some of the advantages that you see, like in the Graviton processor, the reason that customers are so excited about them is because, they're extremely energy efficient, very low power consumption for the speed that you get. The Graviton processors have up to 64 cores and each VCPU that you see inside of the instance, is a dedicated core, not a hyperthread, like you see in Intel or AMD.

That's relevant, because it's really useful for the scale out, the cloud native workloads that many customers are running on AWS. You can think of it as a processor and an instance; it's built for the cloud native applications that everyone wants to run. It allows customers to run them very efficiently and at a low cost. Those energy savings that I mentioned, that power efficiency is one of the factors that allows AWS to price these at 20% discount compared to Intel or AMD instances. You can see why there's been a lot of interest around those; it's a great cost savings mechanism.

### What is the main reason to adopt Graviton?

It's actually price to performance benefit. Price performance means that for a given spend, am I getting better performance? In a fair amount of cases, Graviton is just objectively outright more performant than Intel, or AMD and a lot of that comes down to the fact there's just more cores available for a given instance size. Even if I only get 5% or 10% better performance, and I'm paying 20% less per instance, that tends to be pretty compelling; that's a good value prop.

The downside for customers, historically, has been that ARM64 is architecture which isn't everywhere yet. It's really only starting to become commonplace. As developers get more comfortable with it, as M1 MacBooks, or M2 MacBooks start to proliferate, and everyone's running and building software on our machines locally, they'll get more comfortable with ARM in production. As other cloud providers start to adopt ARM, it also makes it much easier to think about investing in that. Right now, the struggle is, do I want to run ARM on just AWS? If I have another cloud provider or data center that's X86, then I'm building for two different architectures, and that means I've got different CI pipelines. My developers have to consider the implications of libraries for two different architectures and it can make troubleshooting more complex.

### Is there a major difference in architecture?

It really depends on how modern your application is. Generally speaking, if you're using really up to date frameworks and libraries, you'll have an easier time building for ARM64, but as you start to get to some of these older frameworks, it might not even compile for ARM64 or it might not be performing on 64 and you have to figure out why it's not performing as well. For example, Java8 supports ARM64 but the resulting performance you get running Java8 application on Graviton is just not very good. You really need to be on JDK 11 and 13 to get the performance advantages of ARM64. You can start to see how, if you've got old applications, there's this modernization effort I have to go through first to actually do the migration and have it be beneficial to me.

### How important is Graviton for AWS versus the other players?

Graviton is AWS’s in-house processor. The CPU cores are designed by Arm, so Arm will design these architecture-based cores license them out to other companies for their own use. Amazon design the processor, called Graviton, around Arm.

They’ve really designed the entire server platform around that Arm IP and that Graviton processor, to run the workloads they see customer running in the cloud so that is definitely unique. Azure and GCP all have Intel and AMD instances, but they do not have a Graviton. They can start to build Arm64 processors and I think we see them heading in that direction, but AWS has been doing it now for two or three generations. They had their first Graviton processor when it did not seem like it was that widely adopted and the use cases for it were pretty narrow. Graviton 2 was more general purpose and you started to see a lot more adoption, with folks being very vocal about their move to it and getting that price performance.

They recently announced Graviton 3, the seventh generation of EC2 instances, based around that processor. They claim it continued the price performance benefits so I think it is yet another example of being the first mover in a space and having some advantages due to that and having something unique to offer until everyone else catches up.

### But it is only for a while until you have technology evolve and Azure and GCP start spending money and focusing on it and will close the gap eventually.

I think it is to be seen how quickly they can execute on that. It is clear that Apple has been able to execute on that fairly quickly with the M1 line of Arm-based processors. I wonder how much a five-year lead in that space really means over the long run; I think it is to be determined. There is certainly some very specific expertise with building a server specific Arm processor, building the whole chassis around and it making sure the rest of the attributes of that instance you are offering are built well and can allow your customers to run the workplace they need to, very performantly on your cloud. It is a long process and AWS is three generations in to it so I wonder how quickly folks can catch up.

### Let's say it takes two, three years for customers to get to the more recent libraries and architecture. What if Microsoft and Google have caught up by then, on Graviton?

On one hand, you might be more willing just to make the investment into ARM64, because you feel like it's the new industry standard and I think that that's going to happen. Just with the efficiency and cost gains, it makes a ton of sense as a cloud provider and as a cloud native app developer. I'd say within three to five years, most new applications will be ARM64 native. But there's an interesting play for AWS here, and for a lot of customers to benefit from Graviton. You'll notice that Graviton is kind of the default for a lot of the managed services out there. RDS and Elastic Cache are two examples of, historically, they'd probably put you as the default on an M5; now it's going to be an M6G; it's going to be a Graviton instance. As the consumer of an RDS database, I have no idea that it's Graviton behind the scenes. It's just cheaper for me and it's a little bit more performant.

Through some of these managed services, there is a nice way to get this value add and not really have to do anything. If I was an AWS customer right now, and thinking about Graviton, I would absolutely be migrating everything that's managed; all of my RDS fleet to Graviton, like yesterday. It would save me money, and it's going to be more performant and there's really no burden on my part. There are some caveats. You have to be on a new enough version of MySQL, for example. If I'm on a really old version of MySQL, that RDS is still supporting, maybe it doesn't support Graviton yet, but if I'm on a relatively recent version, I would just port it over right away and call it a day.

### Is it more profitable for Amazon to run Graviton instances versus older instances?

I don't know if it's more profitable; I know that it's way more efficient. There's a there's an interesting talk, which is about how much less cooling it takes in the data center, how much less power consumption it drives. Amazon has a lot of green initiative aspirations, especially in data centers, because they're such huge power hogs. I think that this is a major, major point.

### It saves them in overheads if they do their own cooling and they do their own power generation.

Exactly. It's these operational expenses. I don't know about the actual margins and the chips themselves. But I do know in terms of operating expenses, it's definitely cheaper to run them and I think that's where a lot of those cost savings come from. I think Peter DeSantis spoke about this at re:Invent last year, where he talks about the sustainability goals and how Graviton's a part of that. Interestingly enough, the cost savings and carbon footprint aspect has been a big driver of Graviton as well, and companies that are very conscientious about that would purposely adopt it for that reason, because they can reduce their carbon footprint by 20%.

### What was the original reason for Amazon to do Graviton?

Well, I think kind of more control over your own destiny is probably a big part of it. I don't remember the original genesis, but they acquired a company called Annapurna Labs, at some point, who was originally helping them build just ASICs for networking hardware and components inside of the server chassis. But they also had the ability to fab their own chips. They licensed cores from ARM and built processors around them. I think that just gave them the ability to start iterating more quickly and building processors that were specific to what customers needed.

Look at the ramp, the generational cycle, that Intel was on between fifth gen and sixth gen instances. The M5 to the M6i, was something on the order of four or five years, and AWS pushed a second Graviton out within 18 months after the first one. You can start to see how you can start to get some really interesting advantages if you can iterate on your processor, by looking at the workloads that your customers have, build a new processor in response and actually get it out the door in 18 months. You could be several cycles ahead of the traditional incumbents in that space within a few years.

### Why don't Microsoft and Google do this?

Microsoft is doing it. They do have an ARM64 instance, based on Ampere which seems to be quite performant. The difference there, though, is I think that chip is pre-provided to them.

### They didn't build it themselves, that's my understanding.

Yes, exactly. Maybe they don't quite have the expertise yet, or they're developing it. But I think the advantage of building your own chip is that you can be very specific about what you want to include and what you don't and which workloads you want to specialize in. It doesn't have to be the most general-purpose processor like AMD or Intel have to provide you. It has to be good at everything. I think it's just one more tool in the tool chest really, for them to offer because Graviton's not good at everything and it never will be. I don't think it will be the general purpose, every workload forever should go on Graviton type thing. You still see Intel being better at single core performance, for example. There's a place for all the different instances. But I do think, like I was describing earlier, Graviton really excels when you can have multi-threaded applications, when you can take advantage of all the cores on the processor.

### What would be an example of that?

Scale out web servers, for example, like HA Proxy is something that works very well. If you're running a lot of containers, for example, where you can spread them across many cores, it's very cost efficient and performant to do that. But there are certain things, maybe some rendering workloads – I'm forgetting exactly – but fluid dynamic modelling and stuff where it tends to perform better on Intel, because it's very serialized and uses only one core primarily or just a couple of cores, not a core for core basis and Intel tends to be faster than Graviton. AWS has some interesting kind of assessments of that, where you can actually do this on Graviton more cheaply, even though it takes slightly longer, because it's 20% cheaper. What's your priority? Getting it done as fast as possible, or saving some money on it?

### What's the endgame here? If they own the full stack, where they can design the chip, design the server, they can build the micro service on top, the customer workloads, what is the endgame you're going to have? You could have hundreds of different mini Gravitons that serve different customer groups, effectively.

> I think that's exactly right. You can eventually build very hyper specific processors based on your observations of your customer patterns. And that's probably where they're headed. I have a tale from Amazon Apocrypha, the lore of the company. Eventually, Amazon started building their own top of rack switches, and building the ASICs inside of these because they were outgrowing the capabilities of what Cisco could provide them. One of the things that was interesting is, back when they were using Cisco gear – Juniper at the time – they would basically say, we have this issue, can you help us replicate it? The problem was, the vendor couldn't replicate the scale that AWS was operating at. They really needed to start building their own stuff that was hyper specialized for what they needed to do, at the scale they needed to operate at and allowed them to debug the full stack in a way that they couldn't previously. It just gives them the, as you mentioned, ability to own the whole stack. It's very interesting that they can be very, very mission focused on a specific workload or a specific customer type, even down to the hardware level, which is really unique.

### Like you said, they could offer a very specific chip for almost an end customer vertical, because they have the scale where no one else can actually offer.

Exactly right.

### It's funny because this all these stories of Amazon it was basically just solving their own problems was is almost like how AWS started. It's like ingrained in their culture. I'm so amazed at how it seems like it just permeates every part of their business where they just have this philosophy of, you can't do it? Okay. I'm going to do it.

It's very much in character, almost to their own detriment. In some cases, it's just like, as an employee there, they always have all these proprietary things, even down to the ticketing system, or what you use to do project management, it's always something in-house and proprietary, the whole developer tool chain. It's very unique to Amazon, and everyone has to ramp up on this stuff when they join and forget about it when they leave. Salesforce is there, right, but it's like, you're not using Jira. To get exposure to Jira afterwards, people are like, you don't know Jira? No, I'm using a weird Amazon spin-off of that for 10 years.

### Were there another major hurdles to the adoption of Graviton on your mind?

I think they were all technological. I think it was really just exposure to this as a technology and how to get your apps optimized for it. A lot of the work that the Graviton team was doing was going out there and finding bugs and common open-source libraries or performance issues and common open-source libraries and patching them, and submitting these fixes upstream. When you go to build your SSL library or web server or whatever, compile it for ARM64, it worked as well as you needed it to.

### How important is Graviton, in your mind, over the next 10 years?

I think it's really important. Just generally speaking, I think that maybe X86 is kind of running out of steam in terms of ways to optimize, become more efficient. It seems like ARM64 is a platform everyone's betting on. I think that Apple investing in it for their consumer hardware is a huge validation, I don't know if you have used an M1 MacBook. But to me, it's like a world-shaking advancement. It's passively cooled, infinite battery life. They're just so good, so much more performant. It's clear that ARM has a lot of advantages in this future where we care about efficiency, and we care about speed, and we care about power consumption, there's just only advantage. I think it's really important for AWS; I think it's really important for the future of the industry.

### There's no doubt that Microsoft and Google have to try and catch up on the price performance metric. But the question then maybe is how far will these companies take it in terms of designing vertical lens specific chips to really, really serve customers?

Yes, how integrated do they want everything to be? It's interesting as you see a lot of the Chinese tech companies that are doing what’s called "going heavy". They invest all the way down the stack. They control all these different suppliers and build a lot of stuff. You wouldn't have a US equivalent, where you would use a lot of vendors and premade stuff. Amazon has that, we're going to control everything that we can up and down the stack. I think it is really important for them even at the hardware level. A while ago, we were talking about the very specific workload for a specific vertical; I think that that's ultimately the direction they want to go. And that's a pretty big differentiator. I would expect Microsoft and Google to try to do the same thing eventually. Maybe Microsoft will find that the Ampere chip is sufficient. It's something off the shelf, and maybe it works well enough for them. But I'm curious if that remains competitive, doing something like that, versus really investing in your own chips, as workloads get more specialized, and you can tune processors for these workloads. I get that the sky's the limit for that. I'm pretty excited about that as a potential. But yes, if I was Azure GCP, I'd be also trying to figure out how I can do the same thing.

### I guess you've got to have the expertise.

I think that's the limit. You have to find a company who has chip fab experience and can actually do all this build for you.

### Who are all these guys that AWS have? Obviously, they bought a company, Annapurna?

That's who they bought. They were acquired and that talent is still at the company and I figured the first thing they built, I think it was ASICs. Maybe it was a networking dongle or something they built first, actually, now that I think about it. But then once you have that up and running, start hiring for that expertise as well. So you get ease and other folks who have hardware expertise.

### This was good. Thanks very much.