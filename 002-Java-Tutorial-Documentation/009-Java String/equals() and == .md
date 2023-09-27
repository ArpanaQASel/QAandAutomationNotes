## Difference between comparing String using == and .equals() method in Java


- Both equals() method and the == operator are used to compare two objects in Java. == is an operator and equals() is method. 
- But == operator compares reference or memory location of objects in a heap, whether they point to the same location or not.
- Whenever we create an object using the operator new, it will create a new memory location for that object.

- So we use the == operator to check memory location or address of two objects are the same or not.

- In general, both equals() and “==” operators in Java are used to compare objects to check equality, but here are some of the differences between the two: 

- The main difference between the.equals() method and == operator is that one is a method, and the other is the operator.
- We can use == operators for reference comparison (**address comparison**) and .equals() method for **content comparison**. In simple 
     words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the 
     objects.
-    a class does not override the equals method, then by default, it uses the equals(Object o) method of the closest parent class that has overridden this method. See [Why to Override equals(Object) in detail.

~~~java
// the concept of == operator
 
public class Test {
    public static void main(String[] args)
    {
        String s1 = "HELLO";
        String s2 = "HELLO";
        String s3 =  new String("HELLO");
 
        System.out.println(s1 == s2); // true
        System.out.println(s1 == s3); // false
        System.out.println(s1.equals(s2)); // true
        System.out.println(s1.equals(s3)); // true
    }
}
~~~

**Output**
~~~java
true

false

true

true
~~~

**Explanation:** Here, we create two objects, namely s1 and s2. 

- Both s1 and s2 refer to same objects.
- When we use the == operator for s1 and s2 comparison, the result is true as both have the same addresses in the string constant pool.
- Using equals, the result is true because it’s only comparing the values given in s1 and s2.
~~~java

s1 = “HELLO”

s2 = “HELLO”

s3 = “HELLO” 

~~~

Let us understand both the operators in detail:


**Equality operator(==)**

---

We can apply equality operators for every primitive type, including the boolean type. We can also apply equality operators for object types. 

~~~java
// Java program to illustrate
// == operator for compatible data
// types
 
class Test {
    public static void main(String[] args)
    {
        // integer-type
        System.out.println(10 == 20);
 
        // char-type
        System.out.println('a' == 'b');
 
        // char and double type
        System.out.println('a' == 97.0);
 
        // boolean type
        System.out.println(true == true);
    }
}
~~~
**Output**
~~~java

false

false

true

true

~~~
If we apply == for object types then, there **should be compatibility between arguments types** (either child to parent or parent to child or same type). Otherwise, we will get a compile-time error. 

~~~java
// Java program to illustrate
// == operator for incompatible data types
 
class Test {
    public static void main(String[] args)
    {
        Thread t = new Thread();
        Object o = new Object();
        String s = new String("GEEKS");
 
        System.out.println(t == o);
        System.out.println(o == s);
 
       // Uncomment to see error
       System.out.println(t==s);
    }
}

~~~
**Output:** 
~~~java
false

false

// error: incomparable types: Thread and String
~~~


**.equals() Method**

---

In Java, the String equals() method compares the two given strings based on the data/content of the string. If all the contents of both the strings are the same, it returns true. If all characters are not matched, then it returns false. 

~~~java
public class Test {
    public static void main(String[] args)
    {
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        Thread t3 = t1;
 
        String s1 = new String("Guvi");
        String s2 = new String("Guvi ");
 
        System.out.println(t1 == t3);
        System.out.println(t1 == t2);
        System.out.println(s1 == s2);
 
        System.out.println(t1.equals(t2));
        System.out.println(s1.equals(s2));
    }
}

~~~
**Explanation:** Here, we are using the .equals method to check whether two objects contain the same data or not. 

- In the above example, we create 3 Thread objects and 2 String objects.
- In the first comparison, we check whether t1 == t3 or not. As we know that both **t1 and t3 point to the** **same object**. That’s why it returns true.
- In the second comparison, we are using the operator “==” for comparing the String Objects and not the contents of the objects. Here, both the objects are different, and hence the outcome of this comparison is “False.”
- When we are comparing 2 String objects by .equals() operator, then we are checking that is both objects contain the same data or not.
- Both the objects contain the same String, i.e., Guvi. That’s why it returns true.

