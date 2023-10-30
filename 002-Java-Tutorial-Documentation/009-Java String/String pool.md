## String Constant Pool

In Java, Strings are the type of objects that can store the character of values. A string acts the same as an array of characters in Java. Memory allocation is not possible without String Constant Pool. In this article, we will learn about Java String Constant Pool.


**What is Java String Pool?**

---

A Java String Pool is a place in heap memory where all the strings defined in the program are stored. A separate place in a stack is there where the variable storing the string is stored. Whenever we create a new string object, JVM checks for the presence of the object in the String pool, If String is available in the pool, the same object reference is shared with the variable, else a new object is created.

**Example of Java String Pool**


---
Consider the following two Java programs, the first program produces the output as “Yes”, but the second program produces the output as “No”. Can you guess the reason? 

**Example 1:**

~~~java
// Program 1: Comparing two references to objects
// created using literals.
import java.util.*;
  
// Driver Class
class Guvi {
    // main function
    public static void main(String[] args)
    {
        String s1 = "abc";
        String s2 = "abc";
  
        // Note that this == compares whether
        // s1 and s2 refer to same object or not
        if (s1 == s2)
            System.out.println("Yes");
        else
            System.out.println("No");
    }
}


~~~

**Output**
~~~
Yes
~~~
**Example 2:**

~~~java
// Program 2: Comparing two references to objects
// created using new operator.
import java.util.*;
  
// Driver Class
class Guvi{
    // main function
    public static void main(String[] args)
    {
        String s1 = new String("abc");
        String s2 = new String("abc");
  
        // Note that this == compares whether
        // s1 and s2 refer to same object or not
        if (s1 == s2)
            System.out.println("Yes");
        else
            System.out.println("No");
    }
}


~~~

**Output**
~~~
No
~~~


**Let us understand why we get different outputs with the below explanation.** 

---

The String is a sequence of characters. One of the most important characteristics of a string in Java is that they are immutable. In other words, once created, the internal state of a string remains the same throughout the execution of the program. This immutability is achieved through the use of a special string constant pool in the heap. In this article, we will understand about the storage of the strings. A string constant pool is a separate place in the heap memory where the values of all the strings which are defined in the program are stored. When we declare a string, an object of type String is created in the stack, while an instance with the value of the string is created in the heap. On standard assignment of a value to a string variable, the variable is allocated stack, while the value is stored in the heap in the string constant pool. For example, let’s assign some value to a string str1.


**How String Pool Works?**

---

In Java, a string is defined and the value is assigned as:
~~~java
String str1 = "Hello";
~~~
The following illustration explains the memory allocation for the above declaration:

![Aspose Words 26479d7e-6c73-45cd-9002-f78bf423a012 001](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/string%20constant2.jpg)



In the above scenario, a string object is created in the stack, and the value “Hello” is created and stored in the heap. Since we have normally assigned the value, it is stored in the constant pool area of the heap. A pointer points towards the value stored in the heap from the object in the stack. Now, let’s take the same example with multiple string variables having the same value as follows:

~~~java
String str1 = "Hello";

String str2 = "Hello";
~~~
The following illustration explains the memory allocation for the above declaration: 

![Aspose Words 26479d7e-6c73-45cd-9002-f78bf423a012 002](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/2f336f83-22dd-4e8c-aa6d-1efbdfedc0d7)



In this case, both the string objects get created in the stack, but another instance of the value “Hello” is not created in the heap. Instead, the previous instance of “Hello” is re-used. The *string constant pool* is a small cache that resides within the heap. Java stores all the *values* inside the string constant pool on direct allocation. This way, if a similar value needs to be accessed again, a new string object created in the stack can reference it directly with the help of a pointer. In other words, the string constant pool exists mainly to reduce memory usage and improve the reuse of existing instances in memory. When a string object is assigned a different value, the new value will be registered in the string constant pool as a separate instance. 

**Let’s understand this with the following example:**
~~~java
String str1 = "Hello";

String str2 = "Hello";

String str3 = "Class";

~~~

The following illustration explains the memory allocation for the above declaration: 

![Aspose Words 26479d7e-6c73-45cd-9002-f78bf423a012 003](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/b0a8a662-a297-466a-895e-6ca8312e0015)

One way to skip this memory allocation is to use the **new keyword** while creating a new string object. The ‘new’ keyword forces a new instance to always be created regardless of whether the same value was used previously or not. Using ‘new’ forces the instance to be created in the heap outside the string constant pool which is clear, since caching and re-using of instances isn’t allowed here. 

**Let’s understand this with an example:**

---
~~~Java
String str1 = new String("John");

String str2 = new String("Doe");
~~~
The following illustration explains the memory allocation for the above declaration:




![Aspose Words 26479d7e-6c73-45cd-9002-f78bf423a012 004](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/string%20constant4.jpg)



