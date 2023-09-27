
## LinkedList 

Java LinkedList class uses a doubly linked list to store the elements. It provides a linked-list data structure. It inherits the AbstractList class and implements List and Deque interfaces.


![LinkedList-Hierarchy](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/2abfbf74-cea7-4d5a-be7e-acbd1b410ed5)













**The important points about Java LinkedList are:**

---

- Java LinkedList class can contain duplicate elements.

-	Java LinkedList class maintains insertion order.

-	Java LinkedList class is non synchronized.

-	In Java LinkedList class, manipulation is fast because no shifting needs to occur.

-	Java LinkedList class can be used as a list, stack or queue.

**How Does LinkedList work Internally?**

---



![Java-LinkedList](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/3d605ae5-37c1-41ab-957f-3f317d73ed05)










**Constructors in the LinkedList:**

---

In order to create a LinkedList, we need to create an object of the LinkedList class. The LinkedList class consists of various constructors that allow the possible creation of the list. The following are the constructors available in this class:

1. LinkedList(): This constructor is used to create an empty linked list. If we wish to create an empty 

~~~java
LinkedList ll = new LinkedList();  
~~~

2. LinkedList(Collection C): This constructor is used to create an ordered list that contains all the elements of a specified collection, as returned by the collection’s iterator. If we wish to create a LinkedList with the name ll, then, it can be created as: 
~~~java
LinkedList ll = new LinkedList(C);
~~~

**Advantages of using LinkedList in Java:**

---

- Dynamic size: As with Vector, the size of a LinkedList can grow or shrink dynamically, so you don’t have to worry about setting an initial size.
- Efficient Insertions and Deletions: LinkedList is an efficient data structure for inserting or deleting elements in the middle of the list because you only need to change the links between elements, rather than shifting all elements after the insertion or deletion point.
- Flexible Iteration: With a linked list, you can efficiently iterate through the list in either direction, since each element has a reference to both its predecessor and successor elements.
- 

**Disadvantages of using LinkedList in Java:**

---

- Performance: LinkedList has a slower performance than ArrayList when it comes to accessing individual elements. This is because you need to traverse the list to reach the desired element, whereas with ArrayList, you can simply access the desired element using an index.
- Memory overhead: LinkedList requires more memory than ArrayList because each element requires additional memory for the links to its predecessor and successor elements.


**LinkedList Example:**
~~~java
    import java.util.*;  
    public class LinkedList1{  
     public static void main(String args[]){  
      
      LinkedList<String> al=new LinkedList<String>();  
      al.add("Ravi");  
      al.add("Vijay");  
      al.add("Ravi");  
      al.add("Ajay");  
      
      Iterator<String> itr=al.iterator();  
      while(itr.hasNext()){  
       System.out.println(itr.next());  
      }  
     }  
    }  
~~~
Output:
~~~
       Ravi
       Vijay
       Ravi
       Ajay
~~~
