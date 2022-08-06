# Dynamic Programming

DP is a general technique for solving optimization, search, and counting problems that can be decomposed into sub-problems. You should consider DP whenever you have to make choices to arrive at the solution, when the solution relates to sub-problems.

Like divide-and-conquer, DP solves the problem by combining the solutions of multiple smaller problems, but what makes DP different is that the same sub-problem may re-occur. Therefore, a key to making DP efficient is caching the results of intermediate computations. Problems whose solutions use DP are a popular choice for hard interview questions.

To illustrate the idea underlying DP, consider the problem of computing Fibonacci numbers. The first two Fibonacci numbers are 0 and 1. Successive numbers are the sums of the two previous numbers. The first few Fibonacci numbers are 0,1,1,2,3,5,8,13,21,... The Fibonacci numbers arise in many diverse applications - biology, data structure analysis, and parallel computing are some examples.

Mathematically, the nth Fibonacci number F(n) is given by the equation F(n)= F(n-1)+F(n-2), with F(0) = 0 and F(1)=1. A function to compute F(n) that recursively invokes itself has a time complexity that is exponential in n. This is because the recursive function computes some F(i)s repeatedly. 

Caching intermediate results makes the time complexity for computing the nth Fibonacci number linear in n, albeit at the expense of O(n) storage.

```java
private static Map<Integer, Integer> cache = new HashMap<>();

public static Integer Fibonacci (int n){
	if(n<=1) return n;
	cache.putIfAbsent(n, Fibonacci(n-1) + Fibonacci(n-2));
	return cache.get(n);
}
```

Minimizing cache space is a recurring theme in DP. Now we show a program that computes F(n) in O(n) time and O(1) space. Conceptually, in contrast to the above program, this program iteratively fills the cache in a bottom-up fashion, which allows it to reuse cache storage to reduce the space complexity of the cache.


```java
public static Integer Fibonacci(int n){
   if(n<=1) return n;
   int current0 = 0, current1 = 1;
   for(int i = 2; i<=n ; i++){
           int temp = current1;
		   current1 = current1 + current0;
		   current0 = temp;
   }
   return current1;
}
```


The key to solving a DP problem efficiently is finding a way to break the problem into sub-problems such that 
- the original problem can be solved relatively easily once solutions to the sub-problems are available, and
- these sub-problem solutions are cached.

Usually, but not always, the sub-problems are easy to identify.

Here is a more sophisticated application of DP. Consider the following problem: find the maximum sum over all subarrays of a given array of integers. As a concrete example, the maximum subarray in the array {904, 40, 523, 12, -335, -385, -124, 481, 31} starts at index 0 and ends at index 3.

The brute force algorithm, which computes each subarray sum, has O(n^3) time complexity - there are n(n+1)/2 subarrays, and each sub-array sum takes O(n) time to compute. The brute force algorithm can be improved to O(n^2), at the cost of O(n) additional storage, by first computing S[k] = Sum(A[0,k]) for all k. The sum for A[i,j] is then S[j] - S[i-1], where S[-1] is taken to be 0.

Here is a natural divide-and-conquer algorithm. Take m = floor(n/2) to be the middle index of A. Solve the problem for the subarrays L = A[0,m] and R = A[m+1, n-1]. The maximum subarray be one of the following:
- The maximum subarray from L. For example, if A = <2, 3, -1, 1, -3, 0, 1> and m = 3, then the maximum subarray is A[0,1]
- The maximum subarray from R. For example, if A=<-2, 3, -2, -1, 3, -2, 5> and m = 3, then the maximum subarray is A[4,6]
- The maximum subarray which begins in L and ends in R. This subarray is the maximum subarray that ends at index m concatenated with the maximum subarray that begins at m+1. For example, if A= <-2,3,1,-1,3,2,-1> and m = 3, then the maximum subarray ending at index m is A[1,3] and the maximum subarray starting at index m+1 is A[4,5] - for this example the overall maximum subarray is A[1,5].

The time complexity analysis is similar to that of quicksort, and the time complexity is O(n log n). Because of off-by-one errors, it takes some time to get the program just right.

Now we will solve this program by using DP. Suppose we know the maximum subarray ending at i(inclusive), for all i < j - call these maximum subarray sum B[i]. Then there are only two possibilities for the maximum subarray that ends at j (inclusive):
- It is just the element A[j], or
- It includes earlier entries, in which case it is B[j-1] + A[j]

Therefore B[i] = max(A[i], B[i-1]+A[i]). Since the maximum subarray ends at some index, the answer is the maximum entry in B (or 0 if entries are negative).

As an example, if A = <-2, 3, 1, -7, 3, 2, -1>, then B = <-2, 3, 4, -3, 3, 5, 4> and the maximum subarray sum is 5, corresponding to A[4,5].

```java
public static int findMaximumSubarray(List<Integer> A){
     int maxSeen = 0, maxEnd = 0;
	 for(Integer a : A){
	     maxEnd = Math.max(a, a + maxEnd);
		 maxSeen = Math.max(maxSeen, maxEnd);
	 }
	 return maxSeen;
}


```

The time spent by index is constant, leading to a O(1) time. In our implementation, we recycle space, which leads to a O(1) space complexity.


## Dynamic Programming Boot camp

The programs presented in the introduction for computing the Fibonacci numbers and the maximum subarray sum are good illustrations of DP.

## Top tips for Dynamic Programming

- Consider using DP whenever you have to make choices to arrive at the solution. Specifically, DP is applicable when you can construct a solution to the given instance from solutions to sub-instances of smaller problems of the same kind.
- In addition to optimization problems, DP is also applicable to counting and decision problems - any problem where you can express a solution recursively in terms of the same computation on smaller instances.
- Although DP conceptually DP involves recursion, often for efficiency the cache is built "bottom up", i.e iteratively.
- When DP is implemented recursively the cache is typically a dynamic data structure such as a hash table or a BST; when it is implemented iteratively the cache is usually a one- or multi-dimensional array.
- To save space, cache space may be recycled once it is known that a set of entries will not be looked up again
- Sometimes, recursion may outperform a bottom-up DP solution, e.g, when the solution is found early or subproblems can be pruned through bounding.
- A common mistake in solving DP problems is trying to think of the recursive case by splitting the problem into two equal halves, a la quicksort, i.e, solve the subproblems for subarrays A[0, n/2] and A[n/2+1, n] and combine the results. However, in most cases, these two subproblems are not sufficient to solve the original problem.
- DP is based on combining optimum solutions to subproblems to yield an optimum solution to the original problem. However, for some problems DP will not work, e.g, the longest path problem. The problem is to find the longest path between a given pair of vertices which does not repeat any vertex. In the graph on vertices a,b,c,d and edges (a,b), (b,c),(c,d),(d,a), the longest path from a to d is (a,b,c,d). However some subpaths in this longest path are not longest paths themselves, e.g, the longest path from c to d is (c,b,a,d) not (c,d). In contrast, every subpath of a shortest path is  a shortest path itself.




