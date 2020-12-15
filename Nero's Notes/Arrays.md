The simplest data structure is the array, which is a contiguous block of memory. It is usually used to represent sequences. Given an array A, A[i] denotes the (i+ l)th object stored in the array. Retrieving and updating ,A[i] takes 0(1) time. Insertion into a full array can be handled by resizing, i.e., allocating a new array with additional memory and copying over the entries from the original array. This increases the worst-case time of insertion, but if the new array has, for example, a constant factor larger than the original array, the average time for insertion is constant since resizing is infrequent. Deleting an element from an array entails moving all successive elements one over to the left to fill the vacated space. For example, if the array is (2,3,5,7,9,11,13,17), then deleting the element at index 4 results in the array (2,3,5,7,11,13,17,0). (We do not care about the last value.) The time complexity to delete the element at index i from an array of length n is 0(n - i).



### Remember

- Array problems often have simple brute force solutions that use O(n) space, but subtler solutions that use the array itself to reduce space complexity to O(1).
- Filling an array from the front is slow, so see if it's possible to **write values from the back**
- Instead of deleting an entry (which requires moving all entries to its right), consider overwriting it. 
- When dealing with integers encoded by an array consider **processing the digits from the back of the array**. Alternately, reverse the array so the **least-significant digit is the first entry**.
- Be comfortable writing code that operate with subarrays.
- Think about the **double pointers technique**!
- It's incredibly easy to make off-by-1 errors when operating on arrays.
- Don't worry about preserving the integrity of the array (sortedness, keeping equal entries together, etc.) until it is time to return.
- An array can serve as a good data structure when you know the distribution of the elements in advance. For example, a Boolean array of length W is a good choice for representing a subset of [0,1,....,W-1]. When using a Boolean array to represent a subset of [1,2,3,...,n], allocate an array of size n+1 to simplify indexing.
- Sometimes it's easier to simulate the specification, than to analytically solve for the result. For example, rather than writing a formula for the i-th entry in the spiral order for an n X n matrix, just compute the output from the beginning.

- Make sure to [[Remember your array Java libraries]]


