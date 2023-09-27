

## SortedSet 

The SortedSet interface present in java.util package extends the Set interface present in the collection framework. It is an interface that implements the mathematical set. This interface contains the methods inherited from the Set interface and adds a feature that stores all the elements in this interface to be stored in a sorted manner.

![java-treeset-hierarchy](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/2f2cf7b0-1d17-4c23-8394-286bdcee93f3)




**TreeSet in Java**

---

TreeSet is one of the most important implementations of the SortedSet interface in Java that uses a Tree for storage. The ordering of the elements is maintained by a set using their natural ordering whether or not an explicit comparator is provided. This must be consistent with equals if it is to correctly implement the Set interface.


**Constructors of TreeSet Class are as follows:**

---

In order to create a TreeSet, we need to create an object of the TreeSet class. The TreeSet class consists of various constructors which allow the possible creation of the TreeSet. The following are the constructors available in this class:

**TreeSet():** 

This constructor is used to build an empty TreeSet object in which elements will get stored in default natural sorting order.

Syntax: 
~~~java
TreeSet ts = new TreeSet(); 
~~~
**TreeSet(Comparator):**

This constructor is used to build an empty TreeSet object in which elements will need an external specification of the sorting order.

Syntax: 
~~~java
TreeSet ts = new TreeSet(Comparator comp); 
~~~
**TreeSet(Collection):** 
This constructor is used to build a TreeSet object containing all the elements from the given collection in which elements will get stored in default natural sorting order. In short, this constructor is used when any conversion is needed from any Collection object to TreeSet object.

Syntax: 
~~~java
TreeSet t = new TreeSet(Collection col);  
~~~

**TreeSet(SortedSet):**

This constructor is used to build a TreeSet object containing all the elements from the given sortedset in which elements will get stored in default natural sorting order. In short, this constructor is used to convert the SortedSet object to the TreeSet object.

Syntax: 
~~~java
TreeSet t = new TreeSet(SortedSet s);
~~~

**Features of a TreeSet:**

---

- TreeSet implements the SortedSet interface. So, duplicate values are not allowed.
- Objects in a TreeSet are stored in a sorted and ascending order.
- TreeSet does not preserve the insertion order of elements but elements are sorted by keys.
- If we are depending on the default natural sorting order, the objects that are being inserted into the tree should be homogeneous and comparable. TreeSet does not allow the insertion of heterogeneous objects. It will throw a classCastException at Runtime if we try to add heterogeneous objects.

TreeSet.java
~~~java
    import java.util.*;  
    class TreeSet2{  
     public static void main(String args[]){  
     TreeSet<String> set=new TreeSet<String>();  
             set.add("Ravi");  
             set.add("Vijay");  
             set.add("Ajay");  
             System.out.println("Traversing element through Iterator in descending order");  
             Iterator i=set.descendingIterator();  
             while(i.hasNext())  
             {  
                 System.out.println(i.next());  
             }  
               
     }  
    }  

~~~

Output:
~~~
Traversing element through Iterator in descending order
Vijay
Ravi
Ajay
Traversing element through NavigableSet in descending order
Vijay
Ravi
Ajay
~~~