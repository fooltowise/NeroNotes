# Greedy Algorithms and Invariants

## Greedy Algorithms

A greedy algorithm is an algorithm that computes a solution in steps; at each step the algorithm makes a decision that is locally optimum, and it never changes that decision.

A greedy algorithm does not necessarily produce the optimum solution. As example, consider making change for 48 pence in the old British currency where the coins came in 30, 24, 12, 6, 3 and 1 pence denominations. Suppose our goal is to make change using the smallest number of coins. the natural greedy algorithm iteratively the largest denomination coin that is less than or equal to the amount of change that remains to be made. If we try this for 48 pence, we get three coins - 30 +12 + 6. However, the optimum answer would be two coins - 24 + 24.

In its most general form, the coin changing problem is NP - hard, but for some coinages, the greedy algorithm is optimum - e.g, if the denominations are of the form (1,r, r^2, r^3). (An ad hoc argument can be applied to show that the greedy algorithm is also optimum for US coinage.) The general problem can be solved in pseudo-polynomial time using DP in a manner similar to the knapsack problem.

Sometimes, there are multiple greedy algorithms for a given problem, and only some of them are optimum. For example, consider 2n cities on a line, half of which are white, and the other half are black. Suppose we need to pair white with black cities in a one-to-one fashion so that the total length of the road sections required to connect paired cities is minimized. Multiple pairs of cities may share a single section of road, e.e, if we have the pairing (0,4) and (1,2) then the section of road between cities 0 and 4 can be used by cities 1 and 2.

The most straightforward greedy algorithm for this problem is to scan through the white cities, and, for each white city, pair it with the closest unpaired black city.

This algorithm leads to suboptimum results. Consider the case where white cities are at 0 and 3, and black cities are at 2 and 5. If the white city at 3 is processed first, it will be paired with the black city at 2, forcing the cities at 0 and five to pair up, leading to a road length of 5. In contrast, the pairing of (0,2) and (3,5) leads to a road length of 4.

A slightly more sophisticated greedy algorithm does lead to optimum results: Iterate through all the cities in left to right order, pairing each city with the nearest unpaired city of opposite color. Note that the pairing for the first city must be optimum, since if it were to be paired with any other city we could always change its pairing to be with the nearest black city without adding any road. The observation can be used in an inductive proof of overall optimality.

## Greedy Algorithms Boot Camp

For US currency, wherein coins take values 1,5,10,25,50,100, the greedy algorithm for making change results in the minimum number of coins. Here is an implementation of this algorithm. Note that once it selects the number of coins of a particular value, it never changes the selection. This is a hallmark of a greedy algorithm.

```java
public static int changeMaking(int cents){
	final int[] COINS = {100, 50, 25, 10, 5, 1};
	int numCoins = 0;
	for(int i = 0; i< COINS.length; i++){
		numCoins += cents/COINS[i];
		cents %= COINS[i];
	}
	return numCoins;
}
```

We perform 6 iterations, and each of these iterations does a constant amount of computation, so the time complexity is O(1).

### Top Tips for Greedy Algorithms

- A greedy algorithm is often the right choice for an optimization problem where there's a natural set of choices to select from.
- It's often easier  to conceptualize a greedy algorithm recursively, and then implement it using iteration for higher performance.
- Even if the greedy approach does not yield an optimum solution, it can give insights into the optimum algorithm, or serve as an heuristic.
- Sometimes the correct greedy algorithm is not obvious.