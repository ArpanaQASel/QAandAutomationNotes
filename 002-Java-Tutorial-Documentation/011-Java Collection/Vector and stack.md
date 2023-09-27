

## Vector 

The Vector class implements a growable array of objects. Vectors fall in legacy classes, but now it is fully compatible with collections. It is found in java.util package and implement the List interface, so we can use all the methods of the List interface as shown below as follows:

![vector](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/44488734-5239-4cc2-840f-6131de48a005)











**It is similar to the ArrayList, but with two differences**


- Vector is synchronized.
- Java Vector contains many legacy methods that are not the part of a collections framework.


**Constructors**

---

1. Vector(): Creates a default vector of the initial capacity is 10.
~~~java
Vector<E> v = new Vector<E>();
~~~
2. Vector(int size): Creates a vector whose initial capacity is specified by size.
~~~java
Vector<E> v = new Vector<E>(int size);
~~~
3. Vector(int size, int incr): Creates a vector whose initial capacity is specified by size and increment is specified by incr. It specifies the number of elements to allocate each time a vector is resized upward.
~~~java
Vector<E> v = new Vector<E>(int size, int incr);
~~~
4. Vector(Collection c): Creates a vector that contains the elements of collection c.
~~~java
Vector<E> v = new Vector<E>(Collection c);
~~~

**Advantages of using Vector in Java:**

---

- **Synchronization:** As mentioned before, Vector is synchronized, making it safe to use in a multi-threaded environment.
- **Dynamic Size:** The size of a Vector can grow or shrink dynamically as elements are added or removed, so you don’t have to worry about setting an initial size that will accommodate all elements.
- **Legacy support:** Vector has been part of Java since its inception and is still supported, so it’s a good option if you need to work with older Java code that uses Vector.

## Stack

The stack is a linear data structure that is used to store the collection of objects. It is based on Last-In-First-Out (LIFO). Java collection framework provides many interfaces and classes to store the collection of objects. One of them is the Stack class that provides different operations such as push, pop, search, etc..

The stack data structure has the two most important operations that are push and pop. The push operation inserts an element into the stack and pop operation removes an element from the top of the stack. Let's see how they work on stack.

![stack](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/2a4dc8fa-6b33-495b-8a87-c751ffa7bd7d)








**Java Stack Class**

---

In Java, Stack is a class that falls under the Collection framework that extends the Vector class. It also implements interfaces List, Collection, Iterable, Cloneable, Serializable. It represents the LIFO stack of objects. Before using the Stack class, we must import the java.util package. The stack class arranged in the Collections framework hierarchy, as shown below.

















**Stack Class Constructor**

---

The Stack class contains only the default constructor that creates an empty stack.
~~~java
public Stack()  
~~~

**Creating a Stack**

---

If we want to create a stack, first, import the java.util package and create an object of the Stack class.
~~~java
Stack stk = new Stack(); 

Or

Stack<type> stk = new Stack<>();  
~~~

**Methods in stack**

|methods|modifier|discription|
| :- | :- | :- |
|[empty()]|boolean|The method checks the stack is empty or not.|
|[push(E item)]|E|The method pushes (insert) an element onto the top of the stack.|
|[pop()]|E|The method removes an element from the top of the stack and returns the same element as the value of that function.|
|[peek()]|E|The method looks at the top element of the stack without removing it.|
|[search(Object o)]|int|The method searches the specified object and returns the position of the object.|



**StackEmptyMethodExample.java**
~~~java
    import java.util.Stack;  
    public class StackEmptyMethodExample  
    {  
    public static void main(String[] args)   
    {  
    //creating an instance of Stack class  
    Stack<Integer> stk= new Stack<>();  
    // checking stack is empty or not  
    boolean result = stk.empty();  
    System.out.println("Is the stack empty? " + result);  
    // pushing elements into stack  
    stk.push(78);  
    stk.push(113);  
    stk.push(90);  
    stk.push(120);  
    //prints elements of the stack  
    System.out.println("Elements in Stack: " + stk);  
    result = stk.empty();  
    System.out.println("Is the stack empty? " + result);  
    }  
    }  
~~~
Output:
~~~

Is the stack empty? true
Elements in Stack: [78, 113, 90, 120]
Is the stack empty? false

~~~