# Strings

Strings are ubiquitous in programming today - scripting, web development, and bioinformatics all make extensive use of strings. You should know how strings are represented in memory, and understand basic operations on strings such as comparison, copying, joining, splitting, matching, etc.


Similar to [[Arrays]], string problems often have simple brute-force solutions that use O(n) space solution, but subtler solutions that use the string itself to reduce space complexity to O(1).

Understand the implications of a string type which is **immutable**, e.g the need to allocate a new string when concatenating immutable strings. Know alternatives to immutable strings, i.e an array of characters or a StringBuilder in Java. 

Updating a mutable string from the front is slow, so see if it is possible to write values from the back.

### Know your Java string libraries

When manipulating java strings, you need to know both the String class and the StringBuilder class. The latter is needed because Java strings are immutable, so to make string constructions efficient, it's necessary to have a mutable string class.
- The key methods on strings are:
	- charAt(1)
	- compareTo("foo")
	- concat("bar")   -> returns a new string - does not update the invoking string
	- contains("aba")
	- endsWith("YZ")
	- indexOf("needle")
	- indexOf("needle", 12)
	- indexOf('A')
	- indexOf('B', offset)
	- lastIndexOf("needle")
	- length()
	- replace('a', 'A')
	- replace("a", "A")
	- "foo::bar::abc".split("::")
	- startsWith(prefix)
	- startsWith("www", "http://".length())
	- substring(1), 
	- substring(1,5), 
	- toCharArray()
	- toLowerCase(),
	- trim()

The substring() method is particularly important, and also easy to get wrong, since it has two variants: one takes a start index, and returns a suffix (easily confused with the prefix) and the other takes a start and an end index (the returned substring includes the character at start **but not the character at end**).

- The key methods in StringBuilder are:
	- append()
	- charAt()
	- delete()
	- deleteCharAt()
	- insert()
	- replace()
	- toString()
