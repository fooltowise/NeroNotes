# How I think about Equity Investment Returns

As an investment practitioner, I have always been frustrated with usual valuation methodologies.

Some are too simplistic, like the comparative of multiples. A stock may be "cheap" when we look at its earnings multiple (or book value multiple) compared to other companies in the same industry. But it does not tell us anything if the whole industry is overpriced. Comparing multiples does not give us any insight about the future profitability of a company : its earnings multiple may be half of what other businesses trade at, but if over the next years its profitability deteriorate a low multiple will be more than justified.

At the other extreme, we have the Discounted Cash Flow valuation (DCF). Cherished by academic models, it requires that we forecast a company's future cash flows until judgment day, and discount them to arrive at a present fair value. Although one hundred percent correct in theory, the DCF suffers from many shortcomings. First, any student doing the exercise will figure out that most of the fair value lies in what happens in the far future.

In many cases, more than 70% of the company's value comes from the cash flows occurring after the next 10 years. How to accurately forecast this? That's a recipe for generating models that are very precise but entirely inaccurate. Second, which discounting rate should we use? The DCF formula is extremely sensitive to the discounting rate - changing the rate by 1% can easily increase or decrease a present value calculation by more than 50%. Furthermore, how do we compute this rate? I have always found odd when academic texts claim that the answer lies in the company's Weighted Average Cost of Capital (WACC). Shouldn't the discounting rate be proper to each investor - that is, his opportunity cost? Let's face it, nobody can analyse accurately all the companies on earth, let alone other asset classes. If my investment opportunities are different from yours, why should we use the same discounting rate?

It looks to me like the DCF flaws make it the perfect tool to protect analysts: tweak your inputs just enough, and you can justify any valuation for a stock price. As James Montier said,

> DCFs are like the Hubble Telescope. Move your settings by an inch and you end up studying a different galaxy.

Of course, several improvements have been made to the DCF approach. For instance, Michael Mauboussin recommends to use it to reverse-engineer a company's market expectations. Given a stock's current market price, what are the implicit market expectations about its future profits? Do these expectations make sense? Reverse-engineered DCF is a big improvement. But because most of the value lies in the long term, one can easily disagree with market estimates and yet not be sure about the investment opportunity. In a low interest rates environment, if I think that a company's long term growth will be 5% and the market think it will be 4%. This implies vastly different fair values, but it will not give me more confidence in my assumptions...

In _Accounting for Value_, Stephen Penman improves also on the DCF by using the Residual Earnings approach, which anchors on the balance sheet and near-term earnings. This methodology works well for companies with a lot of tangible assets (think utilities, manufacturers, ...) and commodity businesses. But for companies where most of the profitability comes from intangibles (software, branded products...), residual earnings suffer from the same shortcomings as the DCF: most of the value lies in the distant future. Back to square one.

Other approaches focusing on balance sheet analysis suffer from the same problem. The most iconic, Benjamin Graham's Net-Net valuation, worked extremely well in the 1930s-1960s. But in modern times, businesses don't rely as much on tangible assets as in the last century. And even for the few companies that do, it is not clear if investors would realize the company's net working capital in case of a liquidation - contrary to last century, a liquidation nowadays would surely trigger a lot of litigation, especially with labor. Sometimes however, say in the trough of the 2008 financial crisis, one can find again companies meeting the harsh valuation criteria of the Net-net methodology.

Although Graham's technique is not practical for our investing environment, one of its features is still relevant : that's the _Margin of Safety_. Given my assessment of a company, and knowing that market fluctuations are unpredictable in the short term, how much can I afford to be wrong to still realise an adequate investment return? By how much can the market move against me without jeopardising my investment thesis?

## Quality compounds the problem

Looking at companies benefiting from a long-term competitive advantage, the valuation only gets more difficult. These firms are usually able to compound their earnings at an attractive rate for a long period of time. They will produce huge cash flows in the distant future, but this is exactly the time horizon where the DCF and other approaches are the weakest. That's the cruel fault of the DCF - it is the fuzziest where you need it the most.

We obviously know that great companies are worth paying more. Let's look at the four situations below, ranked by decreasing order of attractiveness:

-   A) A business generating $100 of profits, and able to grow them at an attractive rate without any need for incremental capital; the company distributes most of its earnings to shareholders (either as dividend or share buybacks) and will be able to grow its earnings significantly next year without any reinvestment.
    
-   B) A business generating $100 of profits, and able to grow them an attractive rate. However, it needs incremental capital to grow profits. If most earnings are distributed to shareholders, they won't grow materially next year. A typical "Put more to get more" situation.
    
-   C) A business generating $100 of profits, but the firm needs to reinvest a significant part of its profits into the business to stay at the same level of profitability next year. Even if its financial statements show an accounting profit, most of it cannot be distributed, otherwise the business competitive situation will decline next year. It happens often when capital expenditures are dictated by what competitors are doing. Think airlines and textile industries.
    
-   D) A business generating $100 of profits, but profitability is stuck in a declining trend and will probably lead to bankruptcy.
    

It does not take a genius to figure out that even if all four businesses are generating $100 of profits, business A is worth a lot more than business B, which itself is worth a lot more than business C, which itself is worth more than business D.

But how much should I pay for business A? When we look at market prices, quality companies rarely look cheap. Very often, these businesses are trading at P/E ratios above 30, 40, or even higher. Granted, sometimes those multiples are warranted. But many times they are not, and this is the crux of the quality investor dilemma.

**How do I know when I should pay up for quality - that is, to be able to generate adequate returns? On the other hand, if I find a very fine business, how do I know that its quality is not already baked in the price - therefore likely to provide unattractive returns?**

How does the margin of safety mechanism translates to quality businesses?

## A Framework for Investment returns

There is a quote from Charlie Munger that I have often encountered in the past:

> **“Over the long term, it's hard for a stock to earn a much better return that the business which underlies it earns. If the business earns six percent on capital over forty years and you hold it for that forty years, you're not going to make much different than a six percent return - even if you originally buy it at a huge discount. Conversely, if a business earns eighteen percent on capital over twenty or thirty years, even if you pay an expensive looking price, you'll end up with one hell of a result.”**

Munger's approach intuitively made sense, but for a long time I could not really prove it; it just "felt" right. So I decided to dig more into it to figure out where equity investment returns come from. I'd like to thank Twitter user [Return On Capital](https://twitter.com/CapitalTalk2), from whom I have borrowed a big part of what follows. Sorry in advance if this essay gets quite Math-y. If you are allergetic to math formulas, feel free to jump directly to the conclusions.

If I purchase a share of Company A for a price P1 at time t1 and sell it later for a price P2 at time t2, my annual returns can be computed as

$$  
Annual \, Returns = (\frac{P_2}{P_1})^{\frac{1}{t_2 - t_1}} -1  
$$

  

For instance, if I buy Microsoft stock for $10 and sell it 10 years later for $20, my annual return is roughly 7%:

$$  
Annual \, Returns =(\frac{20}{10})^{\frac{1}{10}} -1 \approx 7 \%  
$$

  

For the sake of simplicity, let's assume that this company doesn't pay any dividend; we can check later that the approach is similar when we consider dividend returns. Let's also assume that there is no stock split or similar corporate action. That would only complicate the formula and the final result would not be altered whatsoever.

Prices can be expressed as multiples of earnings, that is,

$$  
P_1 = E_1 * M_1 , P_2 = E_2 * M_2  
$$

  

where E is an earnings measure (I personally like to use Free Cash Flows before growth capex, but feel free to use your favorite earning measure). M is the multiple on this earnings measure, such that P = M * E. In other words, it is how much the market currently values those earnings. If you choose GAAP Earnings for E, then M is simply the P/E ratio.

Our returns equation becomes:

$$  
Annual \, Returns = (\frac{E_2 * M_2}{E_1 * M_1})^{\frac{1}{t_2 - t_1}} -1  
$$

  

Let T be equal to t2 - t1 (i.e, T is our holding period). Now let's look at E2. Over the holding period T, E2 is nothing more than E1 growing at an average annual rate g.

$$  
E_2 = E_1* (1+g)^T  
$$

  

We can thus substitute for E2:

$$  
Annual \, Returns = (\frac{E_1 *(1 +g)^{T} * M_2} {E_1 * M_1})^{\frac{1}{T}} -1  
$$

  

We can simplify by E1, which leaves us with:

$$  
Annual \, Returns = (\frac{(1 +g)^{T} * M_2} {M_1})^{\frac{1}{T}} -1 = \frac{(1 + g)} { (\frac{M_1}{M_2})^{\frac{1}{T}} }-1  
$$

  

It does not look like much, but we have already come a long way!

**We have just shown that our returns depend only on four parameters:**

-   **The holding period**
    
-   **The average annual earning growth over this period (and not the current level of earnings)**
    
-   **The entry multiple and the exit multiple, and more particularly the ratio between both.**
    

**All investing strategies are a play on one or more of these variables. For example:**

-   Deep value investors care little about the business growth. They want to buy at a very low entry multiple, betting that this multiple will return to the mean after some time.
    
-   Activists investors want to influence the management of a mediocre company with room for improvement. After implementing new measures, profitability usually follows (improved g), and an improved profitability is rewarded with a higher multiple.
    
-   Speculators in meme stocks use mimetic desire and fear-of-missing out to bet that the exit multiple will be a lot higher than the entry multiple (irrespective of how the underlying business actually performs), _even if the entry multiple is already at eye-watering levels_. This is a perfect example of the Greater Fool Theory.
    
-   Investors in spin-offs and other special situations often rely on the institutional forced sell-off following the spin-off, leading to an artificially low entry multiple. Over the period following the spinoff the stock multiple tends to recalibrate to more normal levels, and the investor benefits from the multiple expansion.
    

-   What happens when the holding period becomes very long? That would be the case of buy-and-hold investors, either in passive index funds or quality companies. The term (M1/M2) ^(1/T) tends towards 1, and we are left with:
    

$$  
Annual \, Returns = \frac{(1 + g)} { (\frac{M_1}{M_2})^{\frac{1}{T}} }-1 \approx (1+ g) -1 \approx g  
$$

  

Over the very long-term, stock prices follow earnings growth per share. A passive index fund investor will get the average growth of the economy, while the quality investor will look for businesses whose competitive advantage allow them to reinvest profits at superior rates of returns for a very long period, which should lead to a tremendous earnings growth.

Of course this model has several limitations; in particular, it does not look at how earnings growth is generated:

-   If growth is financed by cash flows from operations (i.e the company does not need external financing), then the growth is simply the Return on Incremental Invested Capital times the portion of reinvested profits. If all profits are reinvested in the business, then the growth is equal to the Return on Capital; we are exactly in the case Charlie Munger is talking about.
    
-   If growth if financed by external capital, it often comes from two sources. The company can raise additional equity, in which case we need to check that even after dilution, earnings per share are still growing at an adequate rate. The company can also issue debt, for which it will have to pay interest. But the true cost of debt is often not the interest to pay on the debt. The true cost occurs when creditors refuse to refinance the company, leading right into bankruptcy. The cost of debt is often small, except when one most needs it. As a result, the more leveraged a company, the lower its market multiple tends to be, which reflects an increased risk of bankruptcy.
    

Let's come back to Charlie Munger, and use his two businesses: one generating 18% per year, and another growing at 6% per year. What happens to investment returns? The results are displayed in the two tables below.

###### Annual Returns - A business generating 18% per year :

Investment Time Horizon (Years)

**(M1/M2)**

**3**

**5**

**10**

**30**

0.3

76.27%

50.13%

33.10%

22.83%

0.5

48.67%

35.55%

26.47%

20.76%

0.7

32.90%

26.73%

22.28%

19.41%

0.8

27.11%

23.39%

20.66%

18.88%

1

18.00%

18.00%

18.00%

18.00%

1.5

3.08%

8.81%

13.31%

16.42%

2

-6.34%

2.72%

10.10%

15.30%

3

-18.18%

-5.28%

5.72%

13.76%

4

-25.66%

-10.57%

2.72%

12.67%

5

-30.99%

-14.48%

0.46%

11.84%

###### Annual Returns - A business generating 6% per year :

Investment Time Horizon (Years)

(M1/M2)

3

5

10

30

0.3

58.34%

34.86%

19.56%

10.34%

0.5

33.55%

21.76%

13.61%

8.48%

0.7

19.38%

13.84%

9.85%

7.27%

0.8

14.19%

10.84%

8.39%

6.79%

1

6.00%

6.00%

6.00%

6.00%

1.5

-7.40%

-2.26%

1.79%

4.58%

2

-15.87%

-7.72%

-1.10%

3.58%

3

-26.50%

-14.91%

-5.03%

2.19%

4

-33.22%

-19.67%

-7.72%

1.21%

5

-38.01%

-23.17%

-9.76%

0.46%

In both tables, the first column displays various scenarios for how the earnings multiples evolve over time. When M1/M2 is greater than 1, the stock will benefit from a multiple expansion over the holding period. On the contrary, when M1/M2 is smaller than 1, the stock will suffer from an multiple contraction (for example, if a market crash occurs).

The next four columns sum up the average annual investment returns that an investor in these companies would get if he would hold their stock for 3,5,10 and 30 years.

For instance, in the first table, we can read that if an investor holds the stock of the 18% business for 30 years, and in the mean time the market multiple halves (M1/M2 = 2), then he will enjoy annual returns of 15.30% per year over the next 30 years.

It becomes obvious that over a short-term horizon (inferior to three years), most of the returns come from the evolution of market sentiment. For instance, in the second table with the business generating 6% per year, the business' mediocre quality does not matter at all in the first column. If the market suddenly decides to triple the business multiple over the next three years (first line, first column), investors will enjoy incredible annual returns of 58.34% per year over those three years.

But when holding periods get longer, business quality takes over. Over thirty years, investors' returns will track closely the underlying business profitability. Even if earnings multiples triple, an investment in the 6% business will provide _only_ 10.34% per year.

**As our time horizon increases, our returns become completely dependent on the quality of the company.**

## Margin of Safety for Growing Companies

We can improve our model by taking into account investors' opportunity cost, i.e the returns available in their second best investment opportunity. An investor will only back a company if estimated annual returns are above his opportunity cost.

Let C be our Opportunity Cost. That means that we need to meet the following condition:

$$  
Annual \, Returns \geq C  
$$

  

That is,

$$  
\frac{(1 + g)} { (\frac{M_1}{M_2})^{\frac{1}{T}} }-1 \geq C  
$$

  

Or

$$  
\frac{(1 + g)} { (\frac{M_1}{M_2})^{\frac{1}{T}} } \geq 1+C  
$$

  

A bit of refactoring gives:

$$  
(\frac{M_1}{M_2})^{\frac{1}{T}} \leq \frac{1 + g} { 1+C}  
$$

  

Finally,

$$  
\frac{M_1}{M_2} \leq (\frac{1 + g} { 1+C})^{T}  
$$

  

Let's pause a little bit here. At this stage, what is under our control? If we have done our homework properly, we should have a firm grasp on:

-   Our assessment of the future probability of the company, and thus a good idea of its future growth g. If we cannot have a view on the future business prospects for the firm, we should gladly take a pass.
    
-   We control as well the time horizon over which we made the company's assessment, T
    
-   We obviously know our opportunity cost, C
    
-   We can choose to invest or not at the current multiple M1
    

The only thing we do not control is M2, that is, how the market will value future earnings when we will want to sell.

Saying that we will only invest in the company at a multiple M1 if the investment annual returns are above our opportunity cost C is the same as saying that the below inequality needs to hold:

$$  
\frac{M_1}{M_2} \leq (\frac{1 + g} { 1+C})^{T}  
$$

  

That is, the multiple contraction M1/M2 needs to be kept under a certain threshold, and this threshold only depends on g (the future growth), C (the opportunity cost) and T (the holding period).

Let's see how this translates in practice. Let's say that our opportunity cost is 10%.

In the below table, the first columns gives various values for g (the earnings CAGR). The four other columns show how much multiple contraction/expansion one can endure for four different holding periods (5,10,15,and 20 years) while still meeting our target of a 10% opportunity cost.

Multiple Contraction/Expansion

Investment Time Horizon (Years)

**Company Earnings CAGR**

**5**

**10**

**15**

**20**

0

61.05%

159.37%

317.72%

572.75%

2%

45.87%

112.78%

210.38%

352.74%

4%

32.37%

75.22%

131.95%

207.03%

6%

20.35%

44.83%

74.30%

109.77%

8%

9.61%

20.14%

31.68%

44.34%

10%

0.00%

0.00%

0.00%

0.00%

12%

-8.62%

-16.49%

-23.68%

-30.26%

15%

-19.93%

-35.89%

-48.66%

-58.89%

20%

-35.28%

-58.11%

-72.89%

-82.45%

25%

-47.23%

-72.15%

-85.30%

-92.24%

30%

-56.62%

-81.19%

-91.84%

-96.46%

This should read as: "**If the company grows its profits by 15% (line 7) each year over the next 15 years (column 4), one can buy at current multiples and still enjoy investment returns north of 10% per year over the next 15 years as long as the multiple does not contract by more than 48.66%**."

And here lies our margin of safety. Let's say I see a company trading at 30 times earnings, and I think that it will grow its earnings by at least 20% per year for the next 10 years. Then, if I buy today, I will still enjoy returns of at least 10% per year, as long as the earnings multiple in ten years will not have contracted by more than 58.11% (that is, if the earnings multiple in ten years is still above 12.56).

**I may not know what the market will look like in ten years, nor how the market sentiment about the company will evolve, but at least I know by how much the market can contract before I stop meeting my investment goals.** And this itself is powerful.

Now let's play a thought experiment and say that in ten years, the earnings multiple of our company is indeed below 12.56. This can be due to two different reasons:

-   Either my assessment of the company was right (it compounded its earnings at 20% per year over the last 10 years), and the market is in the middle of a crisis, in which case the company is offered on sale, which is likely to be temporary.
    
-   Or my assessment of the company was wrong, which will get me in trouble. Not only will the final earnings lower than expected, but the market is likely to reflect a lower profitability in the exit multiple. This is why it is fundamental to have a deep understanding of the business we are investing into. We only need to have a correct insight into a few select businesses, there is no need to know everything about all businesses on earth.
    

Now let's go back to our margin of safety:

-   The more the company is able to grow, the bigger the margin of safety in multiple contraction gets. For a fixed horizon of ten years, an annual growth of 12% provide a 16.49% margin of safety in the multiple contraction. With 20%, the margin of safety jumps to 58.11%.
    
-   If the company's underlying profit growth is less than our opportunity cost (in the above table, that is 10%), there is no margin of safety whatsoever related to the company's quality. To get the desired investment returns, the investor will need a positive market re-rating (that is, an earnings multiple expansion). This can happen if the entry price is low enough (that would be the approach used by deep value investors), but this won't happen with business development alone: the market will need a catalyst event to re-rate the company. Also, the longer the time horizon, the bigger the multiple expansion needs to be to meet our opportunity cost.
    
-   With quality companies able to grow their earnings above our opportunity cost, time is our ally. In the above table, with a company growing at 20% per year, the margin of safety on a 5-years horizon is 35.28%. It jumps to 72.89% over 15 years.
    

Now let's not fool ourselves. So far we have been acting as if we could assess accurately a business profitability over the next 5, 10, or even 15 years. First, I don't believe that is possible for many companies: cyclical industries, commodity businesses, companies with a lot of technological disruption, etc. However, every now and then we stumble upon a business with an entrenched competitive advantage, superior return on capital and growing earnings. Paradoxically, the better the competitive advantage, the easier it is to get a qualitative idea of how long it is going to last, and how much room there is for reinvestment.

The task of the investor is to find those rare businesses, and to be able to assess qualitatively to which extent the current competitive position will evolve: is management busy on growing the competitive advantage? How hard would it be for a well-funded competitor to eat our lunch? How long can this last? Once the competitive moat is assessed, we need to look at how big the opportunities for investment are: is the addressable market big, or getting bigger? Is the industry fragmented?

Those questions are never a one hundred percent yes and no, but answering them will give an idea about to which extent past profitability will go on, improve or worsen, and over which time horizon we are confident about our estimation. This is only after all this qualitative work, that we can look at the tables we have been devising above to consider our margin of safety.

This post has been very quantitative - how do investment returns for growing company work? But the conclusion is very qualitative. **Find companies that will still be there after a multi-decade period. Ensure that they can keep competition at bay and grow their profits at attractive rates for a very long time. The higher a company scores on these criteria, the higher your margin of safety. The higher the margin of safety, the more you will be able to endure market contractions and still meet your investment goals.**