# Adyen, Stripe, Checkout, & Payment Acquirers

Disclaimer: This interview is for informational purposes only and should not be relied upon as a basis for investment decisions. In Practise is an independent publisher and all opinions expressed by guests are solely their own opinions and do not reflect the opinion of In Practise.

### What are the main hurdles to overcome to be on the Visa and Mastercard networks? How sophisticated do you need to be to get there?

There's of course multiple business models in the industry. I assume by being connected to the networks you mean you need to actually become an acquirer and a principal member of the card schemes.

### Yes, exactly.

From one perspective, this basically means a technical connection so you need to connect into the networks and that's one investment that needs to be made. You can work with processing companies who build those connections or you can do it yourself. The complicated thing is here that these networks also have different platforms, especially in LATAM or in APAC. These networks have different functionalities and capabilities than maybe the European acquiring processing platforms. It’s quite a deep investment from a technical perspective.

That's only one aspect. I think the second component is the aspect of becoming a principal member to the scheme share; you need to be a licensed acquiring business and that's a process that can take multiple years in order to obtain licenses in the regions or regulatory countries where you want to be. For example, in Europe pre-Brexit, it was quite easy but now post Brexit you need to have a separate license for the UK and you need to have a license for the EU territory which you can typically passport across the region. That's quite unique. If you move into LATAM, you need to have licenses in those local markets in order to be able to process domestically or regionally, so that requires you to actually become principal members in those territories.

That's where many payment service providers actually choose a different route and so they work with third party acquirers who have local presence and local licenses and, in many cases, they also need to become fully regulated financial authorities, entities. That means you need to be not only regulated and approved by the card networks, but you also need to obtain your financial institutional licenses in those countries and that requires you to get approval from the local regulators as well.

Then last but not least, there's the aspect of sponsorship. In many cases, acquirers still need a sponsor bank covering up for the underlying risk and that's mainly associated with credit risk. You typically need the sponsor bank, who’s providing you with the BIN, and that sponsor bank also carries the risk a bit and that's subject to the negotiations between the acquirer and the sponsor bank.

But for example, if you take Adyen as an example or even Stripe in the US, they were technically already connected in the early days to the card networks but they didn't have their own BIN and they didn't have their own acquiring license. Stripe still uses BBVA or even First Data as a sponsor bank with their BIN and a part of their business is maybe over their own BINs. It’s quite a lengthy process. It's a complicated process.

### I didn’t realize Stripe still uses other banks. They have their own BIN but they use other banks as well, is that right?

I think it’s changing. Last year, Stripe probably moved away a lot of volume from their BIN with First Data, partly through their own BIN and partly to BBVA. I think especially in more maybe high-risk segments, that's where they probably use other BINs. In some businesses, they prefer their own BIN, especially as the Stripe model has been different from day one. Stripe were not necessarily an own acquiring business but they had a payment facilitator business model where they onboarded customers under sub-merchant ID with the supporting sponsor bank, in this case with BBVA and First Data.

But the master merchants, Stripe, that's also how they did it in Europe. They worked with Celator in the earlier days, but nowadays they have their own acquiring business and their own acquiring license. In most cases, they act as the super merchant basically under one merchant ID and then all the smaller underlying customers of Stripe are basically sub-merchants and they don't have their own merchant ID. That's the payment facilitator model which allows them to onboard customers basically instantly but that's only possible within non-high risk segments.

### You need to be able to trust that the merchant is not going to bail out on you in a way. You’re carrying the name of the merchant as the super-merchant, I guess?

Exactly.

### If we can talk about the networks and acquiring in general, Adyen has developed its own acquiring capabilities in many different geographies and this seems to be in marked contrast with many other players, even some big players. My understand is that it gives Adyen an advantage in terms of authorization rates. Is that right and, in that case, why is this model so superior compared to others who basically rely on third parties to do some of their acquiring in some geographies?

> I think, first and foremost, Adyen are mainly focused on large enterprise customers, so typically merchants who have multiple entities across the world and they want to optimize their authorization rates but also their payment costs. By having a global network of licenses and local acquiring capabilities, it allows their enterprise customers to process domestically in some markets, so maybe a Netflix could process with Adyen in Mexico domestically, which increases the authorization rate. In many countries, the issuing banks issue cards that are typically not set up for international or cross border payments.

Take Brazil as an example. If, for example, a European merchant is selling into Brazilian consumers and that card is not enabled for international processing, then there will be a decline, so your authorization rates will go down. There's also a cost implication, so in some cases processing cross border and internationally or intercontinentally will increase the interchange, so the card networks, they impose cross border fees subject to where the consumer is based, the inquiry is based and the merchant is based.

Especially for international businesses who want to optimize their costs but also the authorization rates, working with a provider like Adyen is probably a smart way of doing so. Although there's many companies who process cross border while working with an acquirer that has a European license, but they still process payments and accept payments in the US. It's possible but it can result into higher fees and lower authorization rates.

### Since you mentioned Brazil, that was one of my questions because Adyen has local acquiring in Brazil but I understand that even though they have local acquiring the authorization rates are unlikely to be very high because you still need to go via the local banks. I did not understand technically how it works, but apparently as a merchant, you’re better served by going with the local acquirer rather than with Adyen.

With Adyen in Brazil they don't have their own acquiring license. They can accept payments from Brazilian citizens but they probably acquire to their license maybe in Europe or maybe even in the US and that's where the consumer bank, the issuing bank, probably declines many of those transactions.

The other aspect is that if, for example, you have the opportunity to have a local acquiring license in Brazil, there's companies like dLocal and other companies who offer that capability. In most cases as a merchant, you would still need to be able to contract in that market locally as well because national regulators and national banks, they all put restrictive measurements in place about currency leave in the country so they require you to contract locally.

If you’re international business like Netflix and you don't have an entity in Brazil, the only way you can do it is process internationally and contract with an international acquirer. That will lead to lower conversion rates and authorization rates. That said, there's new companies like dLocal, my current employer Rapid, but also other employers, who have new business models where they allow you to contract internationally and process domestically. But again, I believe they don't do this yet in Brazil. In Mexico, for example, Adyen has their own local license so they can contract locally and process locally.

### If you are Netflix and you have worldwide contracts with Adyen, what happens when you are processing payments from a Brazilian subscriber?

If Netflix don't have an entity in Brazil, they will probably need to contract with Adyen in US or Adyen in Europe and then it's processed like an international cross-border payment. The issuing bank, so the Brazilian bank of the consumer, will probably decline those transactions in about 70% or 80% of the cases because most of the cards issued in Brazil are not set up for international processing, so the banks will decline those transactions. The authorization or conversion rates will be extremely low.

For Netflix, the only way to solve that would be contracting with a local acquirer in Brazil and maybe use their local entity, if they have a local entity; I'm not sure Netflix have a local entity.

### Adyen is targeting the Brazilian market, what does that mean? It’s targeting Brazilian merchants who want to expand outside of Brazil? Is that what it means?

Yes, that's probably what it means, especially for Brazilian merchants selling into international markets, yes.

### On that subject, they have announced a deal to process payments for Amazon in Japan which seemed quite meaningful because I assume that Amazon has lots of capabilities everywhere in the world. How significant do you think it is for Adyen and, from your experience, is there a possibility to expand into other geographies for Amazon?

Of course. Amazon is well known for having a very sophisticated payment platform internally as well. They typically contract with multiple PSPs and acquirers so they also work with Worldpay, Adyen and Stripe in some markets. I think Adyen has their own local license in Japan already for quite some time, so especially for Amazon to enter into the Brazilian market or process payments in the Japanese markets, Adyen is definitely a strong partner.

The benefit for them will be they can leverage their technical integration with Adyen in multiple jurisdictions and regions, so it only requires them to sign with the local Japanese entity of Adyen and the local acquiring business of Adyen, but from a technical point of view they don't need to do anything different. The Adyen platform is a global platform and it's more about which entities and which licenses do you want to use and that gives freedom to global players like Amazon to work with Adyen maybe in Japan locally, work with Adyen in Europe locally or in the US.

### What you’re saying is that Amazon is probably already a customer of Adyen in other geographies?

I’m not 100% sure but I would say so, yes. Typically, Amazon works with 10, 15 acquirers globally and I'm pretty sure that Adyen is one of their main providers already.

### You keep seeing the news flow of newly formed companies on the acquiring side because the market and growth is so big. How realistic is it for those newcomers to enter this market? It seems that you already have quite a number of large players and the newer generations like the Adyens are basically cannibalizing the legacy players. What is the dynamic in this market? What is the potential for disruption from a new entrant?

I think especially the legacy or the incumbent players like Worldpay, these coverages have typically a global infrastructure with local capabilities and licenses but from a technical point of view they are pretty outdated. It's typically a spaghetti complexity of payment systems where maybe traditional ecommerce merchants could work with them, but modern merchants in the gig economy or in a marketplace economy, they require enhanced capabilities with more functionality where those modern payment platforms like Stripe and Adyen can support those complex business cases.

I would say, especially in the last 10 years, the discussion between payment companies and merchants has changed from a financial discussion to a technical discussion so it's really becoming a developer discussion about ease of integration, the supporting complex business models and automating manual processes.

That's typically where companies like Stripe and Adyen do much better than the legacy players. In my opinion, today's growth is really in the SMB market, also driven by the pandemic situation, of course. Many businesses have been forced to go online for the first time and they start selling cross border more easily, also through platforms and marketplaces. So basically, 65%, 70% of global ecommerce is already taking place through platforms or marketplaces and smaller businesses start selling their services or goods to those marketplaces. Those modern payment platforms, they facilitate businesses selling on marketplaces but they've also facilitated those platforms and marketplaces themselves with collection capabilities but also disbursement capabilities and keeping the funds in escrow.

Especially from what I'm seeing here in Europe, there's a lot of focus nowadays on the SMB space, small businesses who need help not only to accept payments but also to expand into international markets more easily. A lot of businesses these days are digital services and subscription-based businesses. Companies like Stripe, they support those companies with not only payments but also with software solutions to help them issue invoices or manage the subscriptions, manage the subscriber base and packages and bundle different subscriptions into one payment.

That's not necessarily a payment product but these are value added services that help small businesses to expand more easily and I think that's where, especially the legacy players, the older payment platforms, are kind of losing market share. They're not playing in the new high growth economy.

### Is there room for new entrants or you feel the market is already torn by the existing new generation players?

There’s probably still enough room. Especially from an B2B or B2C ecommerce perspective today, ecommerce total processing volume is about 20% of the global economy so there's still 80% of growth opportunity. Emerging markets like Middle East, Africa, huge opportunities in APAC and LATAM, so I think there's still a lot of growth opportunities where smaller or new players have an opportunity to be successful, but maybe within a very specific approach in specific markets or in these segments. Companies like EBANX or dLocal, they have tailored on the emerging markets like LATAM and APAC and are also more in the Middle East. The global players perhaps have more focus on the huge ecommerce markets so yes, there's enough opportunity but, at the same stage, you'll also see further consolidation.

### Is Network International a prominent acquirer in the Middle East or is it more a niche player? How are they viewed?

I don't know them very well but, from what I've heard so far, they're a very established business in the Middle East and, for international businesses who want to move into the Middle East and process domestically and regionally, probably one of the first companies to consider. They're also partnering with third party gateways and even payment service providers so they also distribute their network capabilities in the region through the likes of Adyen or Worldpay.

Many of those countries, they face difficulties in obtaining licenses because it really requires a deep investment in opening up entities, opening bank accounts, becoming regulated. Network International are, on the one hand, directly selling in the region to local merchants, but through partnerships with more maybe global or international payment service providers they also sell indirectly, but it's definitely a very established business in the Middle East from what I know.

### How did a company like Checkout become so prominent so quickly in a market where the barriers to entry seem very high in terms of as we discussed getting on the networks, acquiring, getting credibility with the merchants? How would you explain this?

Checkout.com, they have been around also under different names so they have been building their business already for many, many years and, similar to most payment companies, they started their journey in higher risk segments in gambling and gaming. I think what they did pretty well is step into maybe the gap there was between the legacy players and the only modern payment platform focusing on enterprise clients, being Adyen. As international enterprise customers who are cross border and international or global, you had maybe the likes of Worldpay, Paymentech and a few others; or you had Adyen and Adyen was of course the dominant player with beautiful technology, a global reach, not only acquiring but also local payment methods.

They supported marketplaces and platforms as well but there was no real contender to Adyen and I think Checkout really stepped into that space with a similar go to market approach. They were very enterprise focused, very much selling their global reach with local acquiring capabilities, so they have a strong presence now in Europe, they are still partnering with bin sponsors in the US, I believe. They have local capabilities in the Middle East, beautiful technology, beautiful APIs, good documentation, a very aggressive sales organization.

Also in a time where Stripe were mainly focusing on SMB and micro merchants, they were actually stepping with a similar technology stack as Stripe into the enterprise business. I think they have been extremely successful not focusing on small business, only enterprise; aggressive approach, a lot of quality and experience within the company as well.

### Was there a big difference with Adyen in terms of pricing?

> I would say Checkout is commonly known as more aggressive because they want to grow volume. They are still a bit smaller but they were very aggressive in winning large deals and sometimes at zero margin or even negative margin. Finally, in payments, it's about winning a customer and then growing it over the lifetime value over contract, so typically Checkout was well known for being aggressive. I've been competing with them during my Stripe time in some deals but where it was maybe a walkway moment for Stripe, Checkout.com dropped their pants and was able to contract that very aggressively. That’s common behavior when there's a contender in the market who really wants to win the market share.

### In general, you get the feeling that Adyen does not play this game? They’re focusing on premium and getting value for the customer even though the pricing is high?

They probably sell more at premium value, although of course within a proposition for a merchant, there are so many components and one aspect is the acquiring itself. Acquiring is becoming more and more commoditized and it's becoming more and more under pressure. It's more about the value-added services for protection solutions or how they help customers to increase their conversion authorization rates. That's probably what is more important for merchants because finally negotiating on a few basis points is less impactful than maybe 10% higher conversion rates. That's how Adyen can probably maintain their profitability and also sell a premium model which is quite similar to what Stripe are doing as well.

Stripe has a similar approach where they really sell at premium value but within an overall proposition, there's so many components. Sometimes they drop their pricing on a particular product in return for maybe more profit on a different aspect of the proposition.

### I understand that, as you mentioned, Stripe has been a bit more focused on the mid-market and trying to grow enterprise whereas Adyen has been historically focused on enterprise going to the mid-market. But it seems that, at least from the Adyen side, their way to approach SMBs and mid-market is via the marketplaces and the platform businesses. If you're a small business, you don't need the sophistication of an Adyen platform, maybe not initially. How do you see Stripe’s likelihood of success in enterprise? Are there still big clients that they can win or it will be more reliant on finding new winners that will emerge in the next five to 10 years?

It's a combination of both. Stripe has a core philosophy of how they go to markets. They will always look at new startups and small businesses where they feel these will be the next Google or Facebook. Within Stripe, it's quite unique, there's a separate organization that really builds relationships with venture capitalists and investors ensuring that in every country where Stripe is going to market, about 30% of all new startups as an internal KPI need to work with Stripe. That's their long-term vision because they believe that okay, finally one of those start-ups will become the next Facebook. There's a lot of churn and, of course, a lot of those small startups will go out of business.

But that's a separate function within Stripe. It is driving a lot of leads and new opportunities for their sales teams. Stripe initially focused with a pure SMB and micro merchant approach mainly online, with an online account opening. Only in the last maybe four or five years they really started building out a global enterprise sales organization which requires a bit more. It's about pre-sales, it's taking a more consultative approach. These are complex and lengthy sales processes where you need to have technical integration teams working with those merchants, you need to have strong account management and support functions.

A few years ago, that didn't really exist within the world of Stripe, so most of their support was through call centers, even through external vendors who were doing it on behalf of Stripe. Nowadays, they really have a dedicated organization working with large enterprise customers and these sales teams are based in all countries. I was responsible for the Northern European market. I had people in Amsterdam, in Stockholm, I had people in Dublin overseeing my key markets with dedicated support functions, dedicated sales account management functions, pre-sales functions.

I think the only challenge we faced was more a cultural thing. Sales was not really a mentality within Stripe and we didn't have an organization for it. Now that it's in place they can really compete successfully against Adyen and against Checkout and also against the legacy players. During my time in Northern Europe, I won a couple of large deals that we also won during my time at Worldpay, so Stripe is successfully winning large enterprise customers from legacy players, but also from Adyen.

### Adyen have a very low churn rate, so it seems that they don't lose that many clients to the competition and it seems that for the competition to grow, they have to get clients that are still in the tendering process. Is that what you mean when you say that you've won clients from Adyen or is it literally the clients that have switched from Adyen to Stripe?

We have won clients that switched from Adyen to Stripe. At some stage, these companies start spreading their risk and they have a multi-supplier strategy and then they start working with Adyen and Stripe, so Adyen can maybe work better with them in Europe. In the US, Stripe was maybe still the better player.

I think it's not only about churn but it's also about the share of wallet you have as a payments company. Of course, every payment company is claiming to work with Amazon or with Netflix or with Spotify but in many cases, they only process a portion of the volume, so the question is, how can you increase your share of the wallet? The most important thing is winning completely new customers but especially working with a company like Netflix, if you are helping Netflix to expand into new territories that are strong revenue growth drivers, that could also be a very successful strategy to grow your market share versus your competitors.

Churn rates of Adyen are generally low, especially in enterprise. These are complex processes so companies don't move easily from one to another provider. Typically, these contracts are three to five years long. These are deep technical integrations touching upon the commerce platforms, the accounting systems and reporting. It's a painful process of switching providers so that's why typically churn rates are relatively low. In the SMB or micro merchant space churn rates are much higher.

### Over time, can you envisage just like in ERP systems, a large enterprise might have one payment provider or one payment provider that accounts for 80% of their payments and just a backup or is it simply not possible to think like that?

I think especially for global merchants, they probably need to work with multiple providers anyway. Although all those global providers say they are the best or they have global reach, nobody has true global reach or have the best performance in multiple markets. Typically, global and enterprise customers have to work with multiple providers and that's why maybe payment orchestration is also becoming very popular, not only in the SMB but also in the enterprise segment.

Even at Stripe we had our limitations. Even Adyen has their limitations. For example, I spoke with a similar company like Uber a few weeks ago and they have a very strong questions in LATAM and in Europe. In Mexico, they can work with Adyen, but in Brazil they had to work with another provider. They now have built maybe a multi-supplier strategy with three, four acquirers but finally integrating another acquirer and another one again is very intense. That’s where payment orchestration plays a role.

### Would you say that payment orchestration is a threat to companies like Adyen or more like a facilitator?

I think a few years ago most companies thought this would be a threat. That said, these payment orchestration companies also have the opportunity to drive more business to acquirers. From a sales perspective, it can drive a lot of leads so companies like Springly or Primer or Apex, the public can bring new customers to acquirers and PSPs.

My concern is that the central business level, the business layer, is moving away from the acquirer or PSP to the payment orchestration platform and that's where it's getting a bit risky for a company like Adyen because companies like Adyen or even Stripe, they want to sell value added services, so premium services on top of the pure payment processing, such as fraud management, 3D secure tokenization and other tools. That's moving to the payment orchestration level and I think that's becoming a bit risky for companies like Adyen.

Who’s in the driving seat? I think finally payments in general are becoming more and more commoditized. It's about integrations with technology stack, with ERP, CRM, ecommerce platforms and the underlying payment rails becoming more and more commoditized. The payment orchestration layer itself may become more important for a merchant than the underlying payment rails itself and that's where companies like Adyen may be a bit at risk if they lose the control of their relationships with their clients.

### I don’t know if you have followed their capital markets day? Maybe that’s why they’re diversifying away from payment processing into other financial services and you’ve seen there was more sophisticated fraud capabilities and also on the issuing side. Maybe that’s one way for those companies to stay relevant and not to be disintermediated.

Renewed product issuing has been around for many, many years but it was typically led by banks and with old systems, especially for platforms and marketplaces. For example, take the likes of Uber who represent hundreds of thousands of drivers globally who need to be paid and, in many cases, those drivers don't have bank accounts. The ability to issue a virtual card through Adyen or through Stripe to an Uber driver who can cash his salary maybe instantly and can start spending money, that's a beautiful use case.

Instead of having to work with local banks who typically issue those cards by working with a technology player like Adyen or Stripe, an Uber can work with one issuer globally to support their drivers globally. Issuing is one example, but there's many, many other value-added services. If you look for example at the Stripe website, you see there are many payment products, but also many products that are not necessarily related to payments. I think Adyen is probably going in a similar way with treasury products, banking capabilities allowing platforms and international businesses to process payouts and disbursements as if they are global business by having local accounts through Adyen.

### Having followed the company and see how they think long term, I find it quite exciting what they are trying to achieve with those new initiatives on POS and omnichannel and you’re starting to see the results now.

I think the omnichannel was almost invented by Adyen. When I was at Worldpay, I competed intensively with Adyen, especially with ecommerce retail merchant but also with retail merchants, that had both a physical and online presence and Adyen had basically an unrivalled solution there to bring the online and offline channels together through one single platform. That's becoming the standard by now I would say, although many merchants still have traditional retail and a separate commercial environment. Initially, it started by consolidating payment providers and now it's really about integrating platforms and driving new customer experiences through omnichannel shopping experiences, but Adyen played a very important role there. Companies like Adidas or Nike, they have been long partners of Adyen for online and online payments.

### If you’re a customer who’s spending in-store and online, what would Nike or Adidas do to you that’s different?

If I buy something online with Nike and I don't like it but I want to return it because I happen to be in the city, I want to return it to the Nike store. By having my card details on file and by knowing me as a customer of Nike both on the ecommerce side and the online side, they could give me a refund in the store immediately. If these are completely separate platforms you can't do that. For example, by bringing payment data together they can also drive more loyalty and last June I went into a Hugo Boss store and they already have my payment details on file because I'm an online customer as well. They said, listen, do you want me to charge your credit card again? I didn't even have to touch my phone or my card.

### Okay, amazing. There’s still a lot of exciting opportunities for them to address.

Yes. It's also about data because it consolidates data. They can probably have more granular data on consumer behavior on where they spend the money, with which payment types and it's driving new consumer experiences as well. Of course, from a consolidation point of view, it drives more purchasing power from a merchant as well so they can contract with one acquirer and probably get more aggressive pricing by bundling their payment volume.

### Since you've worked with Adyen’s competitors, when you were facing Adyen on a new client, what according to you was the main difference? Was it, as you mentioned, in omnichannel, a technical capability that the other party did not have, or is it a lot of groundwork done ahead of the tender being submitted? What would you say is really the key differentiator for Adyen versus other players?

> I think the main differentiator is their omnichannel capability. In enterprise, there's not too many competitors there, so Stripe is not able to do it, Checkout are not able to do it, Worldpay are maybe in some local markets like in the UK or in the US but, for example, not across the European region. Adyen is quite unique in that sense for enterprise customers.

> In the marketplace platform segment, they're closing the gap so Stripe was the first move for that industry, but that's where basically Stripe and Adyen are the only true contenders. Traditional payment service providers, like Worldpay or Chase, do not really play a role in that segment, working with the likes of Uber or with the likes of Amazon, as an example, where they can really build a solution using the regulatory environment of Stripe and Adyen to keep funds in an escrow account to facilitate the collection, but also the disbursement, the split payments.

That's a very complicated solution and there’s not too many providers doing that today on a global level. I think that's where they're quite unique. In POS itself, they have a very strong POS capability in multiple markets where they don't provide maybe the hardware themselves, so they still need to partner with hardware partners. I think that's where they're quite unique as well.

Definitely a strong contender. Where they are maybe less, let's say, set up for success is still in the SMB segment and the micro merchant business where platforms like Mollie or Stripe or PayPal with Braintree, they have a true online engagement model for customers to sign up and start processing within a matter of hours or day. With Adyen, it's still a very much an enterprise onboarding process where you go through a KYC and a KYB process that's done manually.

### It seems on that segment they’re throwing their energy on the marketplaces and the platforms who themselves are serving SMBs rather than doing it in a very aggressive way.

I think that's a very interesting approach because, finally, some companies like Stripe and PayPal have been going after the SMB directly. But research that I read last year from Amazon is saying that most SMBs sell at four different platforms so you can probably better partner with those platforms and help those platforms to successfully onboard SMBs as sellers on those platforms, than go directly to millions of small businesses, so it’s an interesting strategy. Are you mainly looking at Adyen?

### Let me know if you think that there are others to look at. In Europe, it’s a very narrow field of listed companies. It’s basically Adyen and Worldline.

Worldline, definitely Worldpay which is now part of FIS. Of course, there are smaller equivalents now, like Mollie; I'm not sure if you're familiar with them.

### I’ve heard the name but I’ve never really looked. I only focus on European listed companies.

Mollie is Dutch, as well.

### Is it listed?

Not listed, they're still private, but they had an evaluation of about four billion and the new CEO is a former CEO of ecommerce of Worldpay, so they're really going head-to-head with Stripe but also moving more into the enterprise sequence. I think they call themselves the European equivalent of Stripe. I think if there's one to watch, it’s probably Nuvei, I'm not sure if you're familiar with them.

### Is it the one that was set up by Adyen employees?

No. It’s a Canadian stock listed company but they acquired a company in Europe called SafeCharge. SafeCharge was mainly a high-risk profile acquirer for gambling and then gaming. They acquired a lot of talent from Worldpay and also from Adyen and they're really moving into the enterprise segment and they have global acquiring licenses as well. It's probably one of the contenders for Adyen as well these days.

### Do you think they can make a dent or is Adyen so far ahead that they’re left trying to recruit newer customers?

They typically try to target the smaller Adyen customers because that's where Adyen is not spending a lot of time and money. Adyen is very well known for their aggressive salesforce as well. They have a very experienced sales team so they win a lot of customers, but once they move into managing those accounts, they're not giving a lot of love and attention to sometimes mid-size businesses or smaller enterprises and that's typically where the likes of Worldpay and maybe Nuvei try to target smaller Adyen customers.

### On Apple’s entry into payments, what are the implications for Adyen and more generally the payments ecosystem?

Depends on what you mean. Are you referring to tap-to-pay?

### They had an announcement in March/April saying they were going to either do their own acquiring but certainly offer credit terms to some of their customers. I was wondering if it means that they will be displacing their outside acquirers?

I'm not sure if they're really moving into acquiring. I think they have a strong network with the issuers for Apple Pay which you can use as a consumer. Most recently, they opened up their NFC capabilities allowing small businesses and micro merchants to start accepting card payments on an Apple phone, which is a huge opportunity for Apple.

### For Adyen as well, it seems, because they were enabling tap-to-pay for a few merchants already.

Exactly. It’s probably an opportunity for Adyen as well because they can still be the underlying acquirer. Long term, for Apple, but also for Google and for other giants that can potentially move into the payment space, it disintermediates them of the financial industry. That said, I think that's a long journey. These financial institutions have built an infrastructure and it took them decades to do so, so I think they still need to partner but, in some ways, they will probably compete as well. Apple is also rumored to move into buy now, pay later propositions that could potentially also be a threat to the card industry.

On the other hand, buy now, pay later is also an opportunity for the credit card industry because finally consumers paying with buy now pay later still need to pay their debt and, in many cases, they do that over credit card rails. Even the likes of Klarna for example, partner with Adyen and with Stripe and with Checkout.com for the acquiring business and even Klarna are now issuing credit cards or issuing virtual cards and that's another opportunity where even Adyen can help them with. On one hand, it’s a threat, on the other hand it's also a massive opportunity.

### One thing that really surprised me in the beginning of the year, everybody was worried about and is still worried about the economy, but you saw ecommerce volumes normalizing a little bit and when Adyen published their results, their growth was still very impressive. How do you explain this? Is it just them being able to keep adding new clients and focus on the very highest growing clients? That was something that surprised me and it led me to wonder how sustainable their growth rates are.

It's probably also depending upon the industry target. Especially with the recession coming up, you will see pressure on high valued transaction businesses like traditional retail or maybe in the airline business, where people spend more time on digital and consuming music and watching Netflix, which is subscription and digital, where transaction sizes are relatively small but the volumes are high.

I think Adyen has a great spread across their books so they have traditional ecommerce retail and they have on airlines but they also have many other verticals where, during the recession, actually there will be growth.

Five years ago, the average transaction value was around €30 across ecommerce globally and it was always contradictory with the economy, so in case of a recession, ecommerce was growing because most of ecommerce was digital; video gaming and Netflix and the like. I think that's still the case with Adyen as well, so probably they will suffer like during the pandemic they suffered in retail, but they have been growing their business in other verticals.