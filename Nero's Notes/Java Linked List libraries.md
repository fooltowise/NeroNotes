# Java linked list libraries

We now review the standard linked list library, with the reminder that many interview problems that are directly concerned with lists require you to write your own list class.

Ordered sequences, including dynamically resized arrays and doubly linked lists, implement the *List* interface.  The key methods for the List interface are:
- add('A')
- add(2,3.14)
- addAll(C)
- addAll(0, C)
- clear()
- contains(2.71)
- get(12)
- indexOf(289)
- isEmpty()
- iterator()
- listIterator()
- remove(1)
- removeAll(C)
- retainAll(C)
- set(3, 42)
- sublist(1,5)
- toArray()
Be very confortable with iterators - you should be able to code a class that implements  the iterator if asked to do so.

### Java List implementations

Here are some key things to keep in mind when operating on Java lists.
- The two most commonly used implementations of the List interface are ArrayList(implemented as a dynamically resized array) and LinkedList (implemented as a doubly linked list). Some operations are much slower on ArrayList (i.e add(0,x) takes O(n) on an ArrayList, but O(1) time on a LinkedList. )
- Both add(e) and remove(idx) are optional. In particular, they are not supported by the object returned by Arrays.asList()



### The Java Collections class
The Java Collections class consists exclusively of static methods that operate on or return collections. Some useful methods are 
- Collections.addAll(C, 1,2,4)
- Collections.binarySearch(list, 42)
- Collections.fill(list, 'f')
- Collections.swap(C,0,1)
- Collections.min(C)
- Collections.min(C, cmp)
- Collections.max(c)
- Collections.max(c, cmp)
- Collections.reverse(list)
- Collections.rotate(list,12)
- Collections.sort(list)
- Collections.sort(list, cmp)

These are, by and large, simple functions, but will save you time, and result in cleaner code.