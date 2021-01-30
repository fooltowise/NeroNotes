Sorting - rearranging a collection of items into increasing or decreasing order - is a common problem in computing. Sorting is used to pre-process the collection to make searching faster (as we saw with binary search through an array), as well as identify items that are similar (e.g. students are sorted on test scores).

Naive sorting algorithms run in O(n^2) time. A number of sorting algorithms run in O(n log n) time - heapsort, merge sort, and quicksort are examples. Each has its advantages and disadvantages : for instance, heapsort is in-place but not stable; merge sort is stable but not in-place; quicksort runs O(n^2) in worst case. (An in-place sort is one which uses O(1) space; a stable sort is one where entries which are equal appear in their original order).

A well implemented quicksort is usually the best choice for sorting. We briefly outline alternatives that are better in specific circumstances.

For short arrays, e.g., 10 or fewer elements, insertion sort is easier to code and faster than asymptotically superior sorting algorithms. If every element is known to be at most k places from its final location, a min-heap can be used to get a O(n log k) algorithm. If there are a small number of distinct keys, e.g. integers in the range [0 ... 255], counting sort, which records for each element, the number of elements less than it, works well. This count can be kept in an array (if the largest number is comparable in value to the size of the set being sorted) or a BST, where the keys are the numbers and the values are their frequencies. If there are many duplicate keys we can add the keys to a BST, with linked lists for elements which have the same key; the sorted result can be derived from an in-order traversal of the BST.

Most sorting algorithms are not stable. Merge sort, carefully implemented, can be made stable. Another solution is to add the index as an integer rank to the keys to break ties.

Most sorting routines are based on a compare function. However, it is also possible to use numerical attributes directly, e.g. in radix sort.

The heap data structure is discussed in detail [[Heaps | here]]. Briefly, a max-heap (min-heap) stores keys drawn from an ordered set. It supports O(log n) inserts and O(1) time lookup for the maximum (minimum) element; the maximum (minimum) key can be deleted in O( log n) time. 

### Sorting boot camp

It's important to know how to use effectively the sort functionality provided by your language's library. Let's say we are given a student class that implements a compare method that compares students by name. Then by default, the array sort library routine will sort by name. To sort an array of students by GPA, we have to explicitly specify the compare function to the sort routine.

```java
public static class Student implements Comparable<Student> {
	public String name;
	public double gradePointAverage;
	
	@Override
	public int compareTo(Student that){
	     return name.compareTo(that.name);
	}
	
	Student(String name, double gpa){
		this.name = name;
		this.gradePointAverage = gpa;
	}	
}

public static void sortByName(List<Student> students){
	return Collections.sort(students);
}

public static void sortByGpa(List<Student> students){
	return Collections.sort((a,b) -> Double.compare(a.gradePointAverage, b.gradePointAverage));
}

```

The time complexity of any reasonable sorting complexity is O(n log n) for an array with n entries. Most library functions are based on quicksort, which has O(1) space complexity.

[[Know your  sorting libraries]]


### Top tips for sorting
- Sorting problems come in two flavors: (1) use sorting to make subsequent steps in an algorithm simpler, and (2) design a custom sorting routine. For the former, it's fine to use a library sort function, possibly with a custom comparator. For the latter, use a data structure like a BST, heap, or array indexed by values.
- Certain problems become easier to understand, as well as solve, when the input is sorted. The most natural reason to sort is if the inputs have a natural ordering, and sorting can be used as a preprocessing step to speed up searching.
- For specialized input, e.g. a very small range of values, or a small number of values, it's possible to sort in O(n) time rather than O(n log n) time.
- It's often the case that sorting can be implemented in less space than required by a brute force approach.
- Sometimes it is not obvious what to sort on, e.g. should a collection of intervals be sorted on starting points or end points?



