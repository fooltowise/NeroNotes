# The Mathematics of Returns

If we purchase a share of Company A for price P1 at t1 and sell it for P2 at t2, our annual return can be represented as 

$$
Annual Return = (\frac{P_2}{P_1})^{\frac{1}{t_2 - t_1}} -1 
$$
(i.e. you buy Apple stock for USD100 and sell it for USD200 5 years later, your annual return is ~15%, or $$(\frac{200}{100})^{\frac{1}{5}} -1$$


For the sake of simplicity, let us assume that Company A does not pay out dividends; however, including dividends would not change our conclusion.

 Prices can be expressed as multiples of earnings, that is, 
$$ 
 P_1 = E_1 * M_1   , P_2 = E_2 * M_2
$$
where E is an earnings measure (take EBIT, for example) and M is a multiple (EV/EBIT, for instance). Thus, our return equation becomes 
$$
Annual Return = (\frac{E_2 * M_2}{E_1 * M_1})^{\frac{1}{t_2 - t_1}} -1 
$$




However, E2 is nothing but E1 growing at an average growth rate, g, over the time period T = t2 -t1. We can thus express our return equation as 

$$
Annual Return = (\frac{E_1 *(1 +g)^{T} * M_2} {E_1 * M_1})^{\frac{1}{T}} -1 
$$

 The E1  cancels out and we are left with:
$$
Annual Return = (\frac{(1 +g)^{T} * M_2} {M_1})^{\frac{1}{T}} -1 
$$


We already see something remarkable: *your return does not depend on the current level of earnings.* In fact, it doesn’t depend on *any year’s earnings.* But we aren’t done. What is g? Well, companies produce earnings and these earnings can go two places: given to shareholders through dividends and share repurchases or reinvested into the company. Let us call the percentage of earnings the company reinvests in itself as the reinvestment rate. How much does the company earn on this investment? Well, this is where Return on Equity comes in. The growth rate can thus be represented as the reinvestment rate multiplied by the return on this investment (i.e. ROE). Our return equation then becomes:

$$
Annual Return = (\frac{(1 + reinvestment rate * ROE)^{T} * M_2} {M_1})^{\frac{1}{T}} -1 
$$

If we assume this company reinvests 100% of its profits (i.e. no dividends), reinvestment rate is 100%, and our return equation becomes:

$$
Annual Return = (\frac{(1 + ROE)^{T} * M_2} {M_1})^{\frac{1}{T}} -1 =

\frac{(1 + ROE)} {  (\frac{M_1}{M_2})^{\frac{1}{T}} }-1
$$



What happens when T becomes really large, that is, when your time horizon increases? For those who remember high school calculus, the term $$(\frac{M_1}{M_2})^{\frac{1}{T}}$$ gets closer and closer to one. Practically, for time horizons greater than 15 years, this term has little to no bearing on your return. The equation then becomes our Holy Grail:

$$
Annual Return = \frac{(1 + ROE)} {  (\frac{M_1}{M_2})^{\frac{1}{T}} }-1 = \frac{(1 + ROE)} {1} -1 = ROE
$$



![A screenshot of a cell phone  Description automatically generated](https://lh5.googleusercontent.com/BISNFPIwf8Ub5mTSYB_Dh25mnCahVxamyRJ95CX7f7ANKihwS01nvEDlPYhspKeKKF7wQ4sVybmqzUOFbJMH27EwPWPmVht3d-7s9Gqg79B4riCSePbT4tAeih3wJRLb-Lj9_4w)



*As your time horizon increases, your return becomes* **completely dependent** *on the company’s average return on equity capital.*

Two important caveats. Firstly, the ROE figure in this equation is not the company’s historical ROE nor its current ROE. It is the **average ROE for the next multi-decade period***.* That is, the average *future* return profile for this company. This number requires extreme foresight; fortunately, you don’t need the exact number to make successful investments. Secondly, for these returns to materialize, the company needs to survive for T years, and history teaches us this is no small feat.

For all practical purposes, to generate high returns, one must follow the two paradigms I introduced in this letter: 

(1) Find companies that can survive the next multi-decade period (see [[Competitive Advantage]])
(2) Ensure these companies can generate, on average, high returns on incremental invested capital **for a long period of time**. 

This is a much more difficult process than imputing growth drivers into an excel model, but I can assure you it is immeasurably more rewarding intellectually and, hopefully, financially.

