The basic array type in Java is fixed-size. You should know the Java Arrays utilities very intimately; these simplify working with the basic array type. The ArrayList type implements a dynamically resized array, and is a good replacement for the basic Java array; it's more flexible, and has more API methods. 

- Know the syntax for allocating and initializing an array, i.e  new int[]{1,2,3}
- Understand how to instantiate a 2D array - new Integer[3][]creates an array which will hold three rows, each of these must be explicitly assigned.
- Don't forget the length of an array is given by the length field, unlike Collections, which uses the size()  method, and String, which uses the length() method.
- The Arrays class consists of a set of static utility methods. All of them are important:
- asList()
- binarySearch(A, 641)
- copyOf(A)
- copyOfRange(A, 1,5)
- equals(A,B)
- fill(A,42)
- find(A, 28)
- sort(A)
- sort(A, cmp)
- toString()

- Understand the variants of these methods, i.e how to create a copy of a subarray.
- Understand what "deep" means when checking equality of arrays and hashing them.




