

## LinkedHashSet

Java LinkedHashSet class is a Hashtable and Linked list implementation of the Set interface. It inherits the HashSet class and implements the Set interface.


![java-linkedhashset-hierarchy](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/3950156b-d89e-4a79-a8dc-4cdf0d8a1fd0)















**The important points about the Java LinkedHashSet class are:**

---

- Java LinkedHashSet class contains unique elements only like HashSet.*
- Java LinkedHashSet class provides all optional set operations and permits null elements.
- Java LinkedHashSet class is non-synchronized.
- Java LinkedHashSet class maintains insertion order.

**Constructors of LinkedHashSet Class**

---

**1. LinkedHashSet():** 

This constructor is used to create a default HashSet
~~~java
LinkedHashSet<E> hs = new LinkedHashSet<E>();
~~~
**2. LinkedHashSet(Collection C):** 

Used in initializing the HashSet with the elements of the collection C.
~~~java
LinkedHashSet<E> hs = new LinkedHashSet<E>(Collection c);
~~~
**3. LinkedHashSet(int size):** 

Used to initialize the size of the LinkedHashSet with the integer mentioned in the parameter.
~~~java
LinkedHashSet<E> hs = new LinkedHashSet<E>(int size);
~~~

**4. LinkedHashSet(int capacity, float fillRatio):** 

Can be used to initialize both the capacity and the fill ratio, also called the load capacity of the LinkedHashSet with the arguments mentioned in the parameter. When the number of elements exceeds the capacity of the hash set is multiplied with the fill ratio thus expanding the capacity of the LinkedHashSet.
~~~java
LinkedHashSet<E> hs = new LinkedHashSet<E>(int capacity, int fillRatio);
~~~

 LinkedHashSet.java**

~~~java
    import java.util.*;  
      
    public class LinkedHashSet3   
    {  
      
    // main method  
    public static void main(String argvs[])  
    {  
      
    // Creating an empty LinekdhashSet of string type  
    LinkedHashSet<String> lhs = new LinkedHashSet<String>();  
      
    // Adding elements to the above Set  
    // by invoking the add() method  
    lhs.add("Java");  
    lhs.add("T");  
    lhs.add("Point");  
    lhs.add("Good");  
    lhs.add("Website");  
      
    // displaying all the elements on the console  
    System.out.println("The hash set is: " + lhs);  
      
    // Removing an element from the above linked Set  
      
    // since the element "Good" is present, therefore, the method remove()  
    // returns true  
    System.out.println(lhs.remove("Good"));  
      
    // After removing the element  
    System.out.println("After removing the element, the hash set is: " + lhs);  
      
    // since the element "For" is not present, therefore, the method remove()  
    // returns false  
    System.out.println(lhs.remove("For"));  
      
    }  
    }  
~~~
Output:
~~~
The hash set is: [Java, T, Point, Good, Website]
true
After removing the element, the hash set is: [Java, T, Point, Website]
false

~~~
