

## ArrayList 


**What is ArrayList in Java?**

---

ArrayList is a Java class implemented using the List interface. Java ArrayList, as the name suggests, provides the functionality of a dynamic array where the size is not fixed as an array. Also as a part of the Collection framework, it has many features not available with arrays. 

![arraylist-diagram](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/bbcafa5e-ff45-4d3f-a372-d774d37f44d9)






**Constructors in ArrayList**

---

In order to create an ArrayList, we need to create an object of the ArrayList class. The ArrayList class consists of various constructors which allow the possible creation of the array list. The following are the constructors available in this class:

**1. ArrayList()**

This constructor is used to build an empty array list. If we wish to create an empty ArrayList with the name arr, then, it can be created as:
~~~java
ArrayList arr = new ArrayList();
~~~

**2. ArrayList(Collection c)**

This constructor is used to build an array list initialized with the elements from the collection c. Suppose, we wish to create an ArrayList arr which contains the elements present in the collection c, then, it can be created as: 

~~~java
ArrayList arr = new ArrayList(c);  
~~~

**3. ArrayList(int capacity)**

This constructor is used to build an array list with the initial capacity being specified. Suppose we wish to create an ArrayList with the initial size being N, then, it can be created as:

~~~java
ArrayList arr = new ArrayList(N);

~~~

**Important Features of ArrayList in Java**

---

- ArrayList inherits AbstractList class and implements the List interface.
- ArrayList is initialized by size. However, the size is increased automatically if the collection grows or shrinks if the objects are removed from the collection.
- Java ArrayList allows us to randomly access the list.
- ArrayList can not be used for primitive types, like int, char, etc. We need a wrapper class for such cases.
- ArrayList is not Synchronized. Its equivalent synchronized class in Java is Vector.


**Java ArrayList Example**

---

 ArrayListExample1.java
~~~java
    import java.util.*;  
     public class ArrayListExample1{  
     public static void main(String args[]){  
      ArrayList<String> list=new ArrayList<String>();//Creating arraylist    
          list.add("Mango");//Adding object in arraylist    
          list.add("Apple");    
          list.add("Banana");    
          list.add("Grapes");    
          //Printing the arraylist object   
          System.out.println(list);  
     }  
    }  
~~~
**Output:**
~~~
    [Mango, Apple, Banana, Grapes]
~~~

**Iterating ArrayList using Iterator**

---

Let's see an example to traverse ArrayList elements using the Iterator interface.

ArrayListExample2.java
~~~java
    import java.util.*;  
    public class ArrayListExample2{  
     public static void main(String args[]){  
      ArrayList<String> list=new ArrayList<String>();//Creating arraylist  
      list.add("Mango");//Adding object in arraylist    
      list.add("Apple");    
      list.add("Banana");    
      list.add("Grapes");    
      //Traversing list through Iterator  
      Iterator itr=list.iterator();//getting the Iterator  
      while(itr.hasNext()){//check if iterator has the elements  
       System.out.println(itr.next());//printing the element and move to next  
      }  
     }  
    } 
~~~

Output:
~~~
Mango
Apple
Banana
Grapes

~~~
