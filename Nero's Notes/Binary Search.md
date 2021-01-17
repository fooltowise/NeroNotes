Given an arbitrary collection of *n* keys, the only way to determine if a search key is present is by examining each element. This has O(n) time complexity. Fundamentally, binary search is a natural elimination-based strategy for searching a sorted array. The idea to is eliminate half the keys from consideration by keeping the keys in sorted order. If the search key is not equal to the middle element of the array, one of the two sets of keys to the left and to the right of the middle element can be eliminated from further consideration.

Questions based on binary search are ideal from the interviewers' perspective: it is a basic technique that every reasonable candidate is supposed to know and it can be implemented in a few lines of code. On the other hand, binary search is much trickier to implement correctly than it appears - you should implement it as well as write corner case tests to ensure you understand it properly.

Many published implementations are incorrect in subtle and not-so-subtle ways - a study reported that it is correctly implemented in only five out of twenty textbooks. Jon Bentley, in his book *Programming Pearls*, reported that he assigned binary search in a course for professional programmers and found than 90% failed to code it correctly, despite having ample time.

Binary search can be written in many way - recursive, iterative, different idioms for conditionals, etc.  Here is an implementation adapted from Bentley's book, which includes an error:

``` java
public static int bsearch(int t, List<Integer> A){
	int L = 0, U = A.size() - 1;
	while (L <= U){
		int M = (L+U)/2;
		if(A.get(M) <  t){
			L  = M + 1;
		}
		else if (A.get(M) == t ){
			return M;
		}
		else U = M - 1;
	}
	return  -1;
}
```

The error is in the assignment M = (L+U)/2 in line 4, which can potentially lead to overflow. This overflow can be avoided by using **M = L + (U-L)/2;**

The time complexity of binary search is given by T(n) = T(n/2) + c, where c is a constant. This solves into T(n) = O(log n), which is far superior to O(n) approach needed when the keys are unsorted. A disadvantage of binary search is that it requires a sorted array and sorting an array take O(n log(n)) time. However, if there are many searches to perform, the time taken to sort is not an issue. 

### Important points:
- Binary search is an effective search tool. It is applicable to more than just searching in sorted arrays, i.e it can be used to search an interval of real numbers or integers.
- If your solution uses sorting, and the computation performed after sorting is faster than sorting, **look for solutions that do not perform a complete sort.**
- Consider time/space trade-offs, such as making multiple passes through the data.


[[Know your Searching Libraries]]




