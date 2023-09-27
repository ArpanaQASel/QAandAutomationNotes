##  Arrays Class methods Implementation

Example 1: asList() Method 
~~~java
// Java Program to Demonstrate Arrays Class
// Via asList() method
  
// Importing Arrays utility class
// from java.util package 
import java.util.Arrays;
  
// Main class 
class GFG {
    
    // Main driver method 
    public static void main(String[] args)
    {
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To convert the elements as List
        System.out.println("Integer Array as List: "
                           + Arrays.asList(intArr));
    }
}
~~~
Output
~~~
Integer Array as List: [[I@2f4d3709]
~~~

**Example 2: binarySearch() Method**

This methods search for the specified element in the array with the help of the binary search algorithm.
~~~java
// Java Program to Demonstrate Arrays Class
// Via binarySearch() method
  
// Importing Arrays utility class
// from java.util package
import java.util.Arrays;
  
// Main class
public class GFG {
  
    // Main driver method
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        Arrays.sort(intArr);
  
        int intKey = 22;
  
        // Print the key and corresponding index
        System.out.println(
            intKey + " found at index = "
            + Arrays.binarySearch(intArr, intKey));
    }
}
~~~
Output
~~~
22 found at index = 3
~~~

**Example 3: binarySearch(array, fromIndex, toIndex, key, Comparator) Method**

This method searches a range of the specified array for the specified object using the binary search algorithm.

~~~java
// Java program to demonstrate
// Arrays.binarySearch() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        Arrays.sort(intArr);
  
        int intKey = 22;
  
        System.out.println(
            intKey
            + " found at index = "
            + Arrays
                  .binarySearch(intArr, 1, 3, intKey));
    }
}
~~~
Output
~~~
22 found at index = -4
~~~


**Example 4: compare(array 1, array 2) Method**

~~~java
// Java program to demonstrate
// Arrays.compare() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // Get the second Array
        int intArr1[] = { 10, 15, 22 };
  
        // To compare both arrays
        System.out.println("Integer Arrays on comparison: "
                           + Arrays.compare(intArr, intArr1));
    }
}
~~~
Output
~~~
Integer Arrays on comparison: 1
~~~

**Example 5: compareUnsigned(array 1, array 2) Method**

~~~java
// Java program to demonstrate
// Arrays.compareUnsigned() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Arrays
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // Get the second Arrays
        int intArr1[] = { 10, 15, 22 };
  
        // To compare both arrays
        System.out.println("Integer Arrays on comparison: "
                           + Arrays.compareUnsigned(intArr, intArr1));
    }
}

~~~
Output
~~~
Integer Arrays on comparison: 1
~~~

**Example 6: copyOf(originalArray, newLength) Method** 

~~~java
// Java program to demonstrate
// Arrays.copyOf() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To print the elements in one line
        System.out.println("Integer Array: "
                           + Arrays.toString(intArr));
  
        System.out.println("\nNew Arrays by copyOf:\n");
  
        System.out.println("Integer Array: "
                           + Arrays.toString(
                                 Arrays.copyOf(intArr, 10)));
    }
}
~~~
Output
~~~
Integer Array: [10, 20, 15, 22, 35]

New Arrays by copyOf:

Integer Array: [10, 20, 15, 22, 35, 0, 0, 0, 0, 0]
~~~

**Example 7: copyOfRange(originalArray, fromIndex, endIndex) Method** 

~~~java
// Java program to demonstrate
// Arrays.copyOfRange() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To print the elements in one line
        System.out.println("Integer Array: "
                           + Arrays.toString(intArr));
  
        System.out.println("\nNew Arrays by copyOfRange:\n");
  
        // To copy the array into an array of new length
        System.out.println("Integer Array: "
                           + Arrays.toString(
                                 Arrays.copyOfRange(intArr, 1, 3)));
    }
}
~~~
Output
~~~
Integer Array: [10, 20, 15, 22, 35]

New Arrays by copyOfRange:

Integer Array: [20, 15]
~~~

**Example 8: deepEquals(Object[] a1, Object[] a2) Method** 

~~~java
// Java program to demonstrate
// Arrays.deepEquals() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Arrays
        int intArr[][] = { { 10, 20, 15, 22, 35 } };
  
        // Get the second Arrays
        int intArr1[][] = { { 10, 15, 22 } };
  
        // To compare both arrays
        System.out.println("Integer Arrays on comparison: "
                           + Arrays.deepEquals(intArr, intArr1));
    }
}

~~~
Output
~~~
Integer Arrays on comparison: false
~~~

**Example 9: deepHashCode(Object[] a) Method **

~~~java
// Java program to demonstrate
// Arrays.deepHashCode() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[][] = { { 10, 20, 15, 22, 35 } };
  
        // To get the dep hashCode of the arrays
        System.out.println("Integer Array: "
                           + Arrays.deepHashCode(intArr));
    }
}
~~~
Output

~~~
Integer Array: 38475344
~~~

**Example 10: deepToString(Object[] a) Method** 

~~~java
// Java program to demonstrate
// Arrays.deepToString() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[][] = { { 10, 20, 15, 22, 35 } };
  
        // To get the deep String of the arrays
        System.out.println("Integer Array: "
                           + Arrays.deepToString(intArr));
    }
}
~~~
Output
~~~
Integer Array: [[10, 20, 15, 22, 35]]
~~~

**Example 11: equals(array1, array2) Method** 

~~~java
// Java program to demonstrate
// Arrays.equals() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Arrays
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // Get the second Arrays
        int intArr1[] = { 10, 15, 22 };
  
        // To compare both arrays
        System.out.println("Integer Arrays on comparison: "
                           + Arrays.equals(intArr, intArr1));
    }
}
~~~
Output
~~~
Integer Arrays on comparison: false
~~~

**Example 12: fill(originalArray, fillValue) Method**

~~~java
// Java program to demonstrate
// Arrays.fill() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Arrays
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        int intKey = 22;
  
        Arrays.fill(intArr, intKey);
  
        // To fill the arrays
        System.out.println("Integer Array on filling: "
                           + Arrays.toString(intArr));
    }
}
~~~
Output
~~~
Integer Array on filling: [22, 22, 22, 22, 22]
~~~

**Example 13: hashCode(originalArray) Method** 

~~~java
// Java program to demonstrate
// Arrays.hashCode() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To get the hashCode of the arrays
        System.out.println("Integer Array: "
                           + Arrays.hashCode(intArr));
    }
}
~~~
Output
~~~
Integer Array: 38475313
~~~
**Example 14: mismatch(array1, array2) Method**

~~~java
// Java program to demonstrate
// Arrays.mismatch() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Arrays
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // Get the second Arrays
        int intArr1[] = { 10, 15, 22 };
  
        // To compare both arrays
        System.out.println("The element mismatched at index: "
                           + Arrays.mismatch(intArr, intArr1));
    }
}
~~~
Output
~~~
The element mismatched at index: 1
~~~

**Example 15: parallelSort(originalArray) Method**

~~~java
// Java program to demonstrate
// Arrays.parallelSort() method
  
// Importing Arrays class from
// java.util package 
import java.util.Arrays;
  
// Main class
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To sort the array using parallelSort
        Arrays.parallelSort(intArr);
  
        System.out.println("Integer Array: "
                           + Arrays.toString(intArr));
    }
}
~~~
Output
~~~
Integer Array: [10, 15, 20, 22, 35]
~~~

**Example 16: sort(originalArray) Method**

~~~java
// Java program to demonstrate
// Arrays.sort() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To sort the array using normal sort-
        Arrays.sort(intArr);
  
        System.out.println("Integer Array: "
                           + Arrays.toString(intArr));
    }
}
~~~
Output
~~~
Integer Array: [10, 15, 20, 22, 35]
~~~

**Example 17: sort(originalArray, fromIndex, endIndex) Method** 

~~~java
// Java program to demonstrate
// Arrays.sort() method
  
import java.util.Arrays;
  
public class Main {
    public static void main(String[] args)
    {
  
        // Get the Array
        int intArr[] = { 10, 20, 15, 22, 35 };
  
        // To sort the array using normal sort
        Arrays.sort(intArr, 1, 3);
  
        System.out.println("Integer Array: "
                           + Arrays.toString(intArr));
    }
}

~~~
Output
~~~

Integer Array: [10, 15, 20, 22, 35]
~~~

**Example 18: sort(T[] a, int fromIndex, int toIndex, Comparator< super T> c) Method** 

~~~java
// Java program to demonstrate working of Comparator
// interface
import java.util.*;
import java.lang.*;
import java.io.*;
  
// A class to represent a student.
class Student {
    int rollno;
    String name, address;
  
    // Constructor
    public Student(int rollno, String name,
                   String address)
    {
        this.rollno = rollno;
        this.name = name;
        this.address = address;
    }
  
    // Used to print student details in main()
    public String toString()
    {
        return this.rollno + " "
            + this.name + " "
            + this.address;
    }
}
  
class Sortbyroll implements Comparator<Student> {
    // Used for sorting in ascending order of
    // roll number
    public int compare(Student a, Student b)
    {
        return a.rollno - b.rollno;
    }
}
  
// Driver class
class Main {
    public static void main(String[] args)
    {
        Student[] arr = { new Student(111, "bbbb", "london"),
                          new Student(131, "aaaa", "nyc"),
                          new Student(121, "cccc", "jaipur") };
  
        System.out.println("Unsorted");
        for (int i = 0; i < arr.length; i++)
            System.out.println(arr[i]);
  
        Arrays.sort(arr, 1, 2, new Sortbyroll());
  
        System.out.println("\nSorted by rollno");
        for (int i = 0; i < arr.length; i++)
            System.out.println(arr[i]);
    }
}

~~~
Output
~~~
Unsorted
111 bbbb london
131 aaaa nyc
121 cccc jaipur

Sorted by rollno
111 bbbb london
131 aaaa nyc
121 cccc jaipur
~~~

**Example 19: sort(T[] a, Comparator< super T> c) Method**

~~~java
// Java program to demonstrate working of Comparator
// interface
import java.util.*;
import java.lang.*;
import java.io.*;
  
// A class to represent a student.
class Student {
    int rollno;
    String name, address;
  
    // Constructor
    public Student(int rollno, String name,
                   String address)
    {
        this.rollno = rollno;
        this.name = name;
        this.address = address;
    }
  
    // Used to print student details in main()
    public String toString()
    {
        return this.rollno + " "
            + this.name + " "
            + this.address;
    }
}
  
class Sortbyroll implements Comparator<Student> {
  
    // Used for sorting in ascending order of
    // roll number
    public int compare(Student a, Student b)
    {
        return a.rollno - b.rollno;
    }
}
  
// Driver class
class Main {
    public static void main(String[] args)
    {
        Student[] arr = { new Student(111, "bbbb", "london"),
                          new Student(131, "aaaa", "nyc"),
                          new Student(121, "cccc", "jaipur") };
  
        System.out.println("Unsorted");
        for (int i = 0; i < arr.length; i++)
            System.out.println(arr[i]);
  
        Arrays.sort(arr, new Sortbyroll());
  
        System.out.println("\nSorted by rollno");
        for (int i = 0; i < arr.length; i++)
            System.out.println(arr[i]);
    }
}
~~~
Output
~~~
Unsorted
111 bbbb london
131 aaaa nyc
121 cccc jaipur

Sorted by rollno
111 bbbb london
121 cccc jaipur
131 aaaa nyc
~~~


