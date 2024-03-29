# Suites Arithmetico-Geometriques 


Elles sont définies par:

$$\forall n \in \mathbf{N}, u_{n+1} = a \ u_n + b$$

On pose
$$ \mu = \frac{b}{1-a}$$

Ainsi, on a :

$$\forall n \in \mathbf{N}, u_n = a ^n (u_0 - \mu )+ \mu$$


### Application to personal finances:

Lets's define the following variables:
$$C_0 = initial \ capital$$

$$r = annual\ returns (CAGR)$$

$$S = annual \ savings $$
Then in any given year n, the total capital is given by:

$$C_n = (1+r)^n (C_0 + \frac{S}{r})-\frac{S}{r}$$


Usually we also have a target capital T, as well as a time horizon N to reach this target capital:

$$C_N = T=  (1+r)^N (C_0 + \frac{S}{r})-\frac{S}{r}$$


Depending on the issue at hand, we can then choose to solve for either N or r:
$$N = \frac{ln(   \frac {T+ \frac{S}{r}}{C_0 + \frac{S}{r}})}{ln(1+r)}$$
