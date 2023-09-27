## Arrays class

The **Arrays** class in **java.util package** is a part of the **Java Collection Framework**. This class provides static methods to dynamically create and access **Java arrays**. It consists of only static methods and the methods of Object class. The methods of this class can be used by the class name itself.

The class hierarchy is as follows: 

~~~java

java.lang.Object

↳ java.util.Arrays

~~~

why do we need java Arrays class ?

---

- Sort an Arrays.
- Search in an Arrays.
- And many more.

Here Arrays class provides several static methods that can be used to perform these tasks directly without the use of loops, hence forth making our code super short and optimized.

**Syntax:** Class declaration  

~~~java

public class Arrays

extends Object

~~~

**Methods in Java Arrays Class** 

---

The Arrays class of the [java.util package] contains several static methods that can be used to fill, sort, search, etc in arrays. Now let us discuss the methods of this class which are shown below in a tabular format as follows:

|**Methods** |**Action Performed**|
| :-: | :-: |
|asList()|Returns a fixed-size list backed by the specified Arrays|
|binarySearch()|Searches for the specified element in the array with the help of the Binary Search Algorithm|
|binarySearch(array, fromIndex, toIndex, key, Comparator)|Searches a range of the specified array for the specified object using the Binary Search Algorithm|
|compare(array 1, array 2)|Compares two arrays passed as parameters lexicographically.|
|[copyOf(originalArray, newLength)]|Copies the specified array, truncating or padding with the default value (if necessary) so the copy has the specified length.|
|[copyOfRange(originalArray, fromIndex, endIndex)]|Copies the specified range of the specified array into a new Arrays.|
|[deepEquals(Object\[\] a1, Object\[\] a2)]|Returns true if the two specified arrays are deeply equal to one another.|
|deepHashCode(Object[] a) |Returns a hash code based on the “deep contents” of the specified Arrays.|
|[deepToString(Object\[\] a)]|Returns a string representation of the “deep contents” of the specified Arrays.|
|[equals(array1, array2)]|Checks if both the arrays are equal or not.|
|[fill(originalArray, fillValue)]|Assigns this fill value to each index of this arrays.|
|hashCode(originalArray) |Returns an integer hashCode of this array instance.|
|mismatch(array1, array2) |Finds and returns the index of the first unmatched element between the two specified arrays.|
|parallelPrefix(originalArray, fromIndex, endIndex, functionalOperator)|Performs parallelPrefix for the given range of the array with the specified functional operator.|
|parallelPrefix(originalArray, operator)|Performs parallelPrefix for complete array with the specified functional operator. |
|parallelSetAll(originalArray, functionalGenerator)|Sets all the elements of this array in parallel, using the provided generator function. |
|[parallelSort(originalArray)]|Sorts the specified array using parallel sort.|
|setAll(originalArray, functionalGenerator)|Sets all the elements of the specified array using the generator function provided. |
|[sort(originalArray)]|Sorts the complete array in ascending order. |
|[sort(originalArray, fromIndex, endIndex)]|Sorts the specified range of array in ascending order.|
|[sort(T\[\] a, int fromIndex, int toIndex, Comparator< super T> c)]|Sorts the specified range of the specified array of objects according to the order induced by the specified comparator.|
|[sort(T\[\] a, Comparator< super T> c)]|Sorts the specified array of objects according to the order induced by the specified comparator.|
|spliterator(originalArray)|Returns a Spliterator covering all of the specified Arrays.|
|spliterator(originalArray, fromIndex, endIndex) |Returns a Spliterator of the type of the array covering the specified range of the specified arrays.|
|[stream(originalArray)] |Returns a sequential stream with the specified array as its source.|
|[toString(originalArray)] |It returns a string representation of the contents of this array. The string representation consists of a list of the array’s elements, enclosed in square brackets (“[]”). Adjacent elements are separated by the characters a comma followed by a space. Elements are converted to strings as by String.valueOf() function.|

