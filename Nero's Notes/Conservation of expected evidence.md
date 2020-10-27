The way the probability framework is built allows to figure out nice consequences on the relationships between Hypotheses and Evidences. Let H be an hypothesis and E an evidence.

We have P(H) = P(H|E)*P(E) + P(H|~E) * P(~E)

As P(E)+ P(~E)=1, it means that P(H) * [P(E) + P(~E)] = P(H|E)*P(E) + P(H|~E) * P(~E)

And so :

**0 = P(E) * [P(H|E) - P(H)]    +    P(~E)* [P(H|~E) - P(H)]**

The quantity P(H|E) - P(H) is a measure of how much the evidence E confirms H. If this quantity is positive, then seeing the evidence E should make us more confident that H is true, and vice versa.
The same is true for P(H|~E) - P(H) : if this quantity is positive, observing ~E should make it more probable that H is true.

However, since P(E) and P(~E) are both positive, it means that P(H|E) - P(H)  and P(H|~E) - P(H) are always of different sign. If seeing E make the hypothesis H more probable, then observing ~E should make H less probable. The more I think that observing E is a strong evidence for H, the more I should think that observing ~E makes H less probable.

This principle is called the *Conservation of Expected Evidence*.

In a similar manner, if P(E) grows, then P(~E) becomes smaller. But because of the equality above, it also means that P(H|E) - P(H)  and P(H|~E) - P(H) adjust in such a manner that observing E is less of a strong evidence for H as before, and observing ~E becomes a stronger refutation of H than before.

Example: at T0, 

- P(E)= P(~E) = 0.5
- P(H|E) - P(H) = 0.2 and P(H|~E) - P(H) = -0.2

If at T1, P(E) = 0.75 (and thus P(~E) = 0.25) ,

- this is a 50% raise of P(E), and a diminution of 50% of P(~E)
- thus P(H|E) - P(H) should be diminished by 50% to 0.1 => E is less of a proof to H
- and P(H|~E) - P(H) should be raised by 50% to -0.3 => ~E is more of a refutation to H

*Therefore,* for every expectation of evidence, there is an equal and opposite expectation of counter-evidence.



See [[Evidence and Beliefs]]
