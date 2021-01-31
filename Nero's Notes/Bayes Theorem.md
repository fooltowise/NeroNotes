# Bayes Theorem

Given an Hypothesis H and an evidence E, Bayes Theorem says that:

$$P(H|E) = \frac{P(H)*P(E|H)}{P(E)} $$

This comes from the fact that conditional probability is defined as 
$$ P(H*E) = P(H) * P(E|H) = P(E) * P(H|E)$$


Actually, Bayes theorem is easier to use with the odds form of the rule:
$$Odds_{after} = Odds_{before} * LikelihoodFactor$$

or more precisely: 

$$ \frac{P(H|E)}{P(\neg H|E)} = \frac{P(H)}{P(\neg H)} * \frac{P(E|H)}{P(E|\neg H)}$$

because we recognize that by definition, odds are defined as 

$$Odds = \frac{P(H)}{P(\neg H)}$$

So to update our belief about an hypothesis in light of an evidence, we should ask:
1. What were the initial odds of the hypothesis being true?
2. How probable would be the evidence in a world where the hypothesis is true?
3. How probable would be the evidence in a world where the hypothesis is false?

The ratio of (2) and (3) is the likelihood factor. Multiplying the initial odds by the likelihood factor gives us the new odds of the hypothesis being true.


See [[Beliefs]], [[Evidence and Beliefs]]
