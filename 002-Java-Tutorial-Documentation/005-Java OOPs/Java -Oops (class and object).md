
**What is Oop’s (Object-Oriented Programming)?**

---

As the name suggests, Object-Oriented Programming or OOPs refers to languages that use objects in programming, they use objects as a primary source to implement what is to happen in the code. Objects are seen by the viewer or user, performing tasks assigned by you. Object-oriented programming aims to implement real-world entities like inheritance, hiding, polymorphism, etc. in programming. The main aim of OOP is to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 001](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/OOPS%20concepts%20in%20java.jpg)


**List of OOPs Concepts in Java**

---

1. Objects
1. Classes
1. Object 
1. Class
1. Abstraction
1. Inheritance 
1. Polymorphism
1. Encapsulation

   
**Java Classes**

---

A class in Java is a set of objects which shares common characteristics/ behavior and common properties/ attributes.

It is a user-defined blueprint or prototype from which objects are created. For example, a Student is a class while a particular student named Ravi is an object.

**Properties of Java Classes**

1. Class is not a real-world entity. It is just a template or blueprint or prototype from which objects are created.
1. Class does not occupy memory.
1. Class is a group of variables of different data types and a group of methods.

**A-Class in Java can contain:**

- Data member

- Method

- Constructor

- Nested Class

- Interface

**Class Declaration in Java**
~~~java
access\_modifier class <class\_name>

{  

    data member;  

    method;  

    constructor;

    nested class;

   interface;

}
~~~
**Components of Java Classes**

---

In general, class declarations can include these components, in order: 

- **Modifiers:** A class can be public or has default access (Refer this for details).
- **Class keyword:** class keyword is used to create a class.
- **Class name:** The name should begin with an initial letter (capitalized by convention).
- **Superclass(if any):** The name of the class’s parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.
- **Interfaces(if any):** A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.
- **Body:** The class body is surrounded by braces, { }.


![classbody](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/495c7550-7677-413c-9441-d6b83afab150)




**Java Object**

---

An object in Java is a basic unit of Object-Oriented Programming and represents real-life entities. Objects are the instances of a class that are created to use the attributes and methods of a class.  A typical Java program creates many objects, which as you know, interact by invoking methods. An object consists of : 

- State: It is represented by attributes of an object. It also reflects the properties of an object.
- Behavior: It is represented by the methods of an object. It also reflects the response of an object with other objects.
- Identity: It gives a unique name to an object and enables one object to interact with other objects.

![Classes-and-Objects-in-Java](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/Object.jpg)







**Initializing a Java object**

---

The new operator instantiates a class by allocating memory for a new object and returning a reference to that memory. The new operator also invokes the class constructor.

Create an Object of a Class
~~~java
// creating object of class Test

Test t = new Test();

~~~
**Example**
~~~java
class Person {

    String name;

    int age;

    void sayHello() {

        System.out.println("Hello, my name is " + name + " and I am " + age + " years old.");

    }

}

public class Main {

    public static void main(String[] args) {

        // Creating an object of the Person class

       Person person1 = new Person();

    person1.name = "Alice";

        person1.age = 25;

        // Using the object's methods

        person1.sayHello();

    }

}
~~~
