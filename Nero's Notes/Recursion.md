# Recursion
Recursion is an approach to problem solving where the solution depends partially on solutions to smaller instances of related problems. It is often appropriate when the  input is expressed using recursive rules, such as a computer grammar. More generally, searching, enumeration, divide-and-conquer, and decomposing a complex problem into a set of similar smaller instances are all scenarios where recursion may be suitable.

A recursive function consists of base cases and calls to the same function with different arguments. Two key ingredients to a successful use of recursion are identifying the base cases, which are to be solved directly, and ensuring progress, that is the recursion converges to the solution.

A divide-and-conquer algorithm works by repeatedly decomposing a problem into two or more smaller independent sub-problems of the same kind, until it gets to instances that are simple enough to be solved directly. The solutions to the sub-problems are then combined to give a solution to the original problem. Merge sort and quicksort are classical examples of divide-and-conquer.

Divide-and-conquer is not synonymous with recursion. In divide-and-conquer, the problem is divided into two or more independent smaller problems that are of the same type as the original problem. Recursion is more general - there may be a single sub-problem, e.g binary search, the sub-problems may not be independent, e.g dynamic programming, and they may not be of the same type as the original, e.g., regular expression matching. In addition, sometimes to improve runtime, and occasionally to reduce space complexity, a divide-and-conquer algorithm is implemented using iteration instead of recursion.

### Recursion Boot Camp

The Euclidean algorithm for calculating the Greatest Common Divisor (GCD) of two numbers is a classic example of recursion. The central idea is that if x > y, the GCD of x is the GCD of  x and y-x. For example, GCD(156,36) = GCD(120,36) because 120 = 156-36. By extension, this implies that the GCD of x and y is the GCD of x and y mod x, i.e GCD(156,36) = GCD(156 mod 36 = 12, 36) = GCD(12,36 mod 12 = 0)= 12.

```java
public static long GCD(long x, long y){
	return y ==0? x : GCD(y, x%y);
}
```

Since with each recursive step one of the argument is at least halved, it means that the time complexity is O(log (max (x,y))). Put another way, the time complexity is O(n), where n is the number of bits needed to represent the inputs. The space complexity is also O(n), which is the maximum depth of the function call stack. (It is easy to replace the recursion with a loop, thereby reducing the space complexity to O(1)).

Now we describe a problem that can be elegantly solved using a recursive divide-and-conquer algorithm. A triomino is formed by joining three unit-sized square in a L-shape. A mutilated chessboard (henceforth 8x8 board) is made up of 64 unit sized squares arranged in a 8x8 square, minus the top-left square. Suppose you are asked to design an algorithm that computes a placement of 21 triominoes that covers the 8x8 board. Since the 8x8 contains 63 squares, and we have 21 triominoes, a valid placement cannot have overlapping triominoes or triominoes that extend out the 8 x 8 board.

Divide-and-conquer is a good strategy for this problem. Instead of the 8 x 8 board, le'ts consider a n x n board. A 2 x 2 board can be covered with one triomino since it is of the same exact shape. You may hypothetize that a triomino placement for an n x n board with the top-left square missing can be used to compute a placement for a (n+1) x (n+1) board. However, you will quickly see that this line of reasoning does not lead you anywhere.

Another hypothesis is that if a placement exists for an n x n board, then one also exists for a 2n x 2n board. Now we can apply divide-and-conquer. Take four n x n boards and arrange them to form a 2n x 2n square in such a way that three of the boards have their missing square set towards the center and one board hat its missing square outward to coincide with the missing corner of a 2n x 2n board. The gap in the center can be covered with a triomino and, by hypothesis, we can cover the four n x n boards with triominoes as well. Hence, a placement exists for any n that is a power of 2. In particular, a placement exists  for the 2^3 x 2^3 board; the recursion used in the proof directly yields the placement.

### Top tips for recursion

- Recursion is especially suitable when the input is expressed using recursive rules such as a computer grammar.
- Recursion is a good choice for search, enumeration, and divide-and-conquer.
- Use recursion as alternative to deeply nested iteration loops. For example, recursion is much better when you have an undefined number of levels, such as the IP address problem generalized to k sub-strings.
- If you are asked to remove recursion from a program, consider mimicking call stack with the stack data structure.
- Recursion can be easily removed from a tail-recursive program by using a while loop - no stack is needed (optimizing compilers do this).
- If a recursive function may end up being called with the same arguments more than once, cache the results - this is the idea behind Dynamic Programming.