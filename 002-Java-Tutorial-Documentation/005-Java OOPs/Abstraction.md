# Abstraction in Java

Abstraction is a process of hiding the implementation details and showing only functionality to the user. Another way, it shows only essential things to the user and hides the internal details, for example, sending SMS where you type the text and send the message. You don't know the internal processing of the message delivery.

Abstraction lets you focus on what the object does instead of how it does it.

**Ways to achieve Abstraction**

There are two ways to achieve abstraction in Java

1. Abstract class (0 to 100%)
1. Interface (100%)



**abstract keyword in Java**

---
In Java, abstract is a non-access modifier in java applicable for classes, and methods but not variables. It is used to achieve abstraction which is one of the pillars of Object Oriented Programming(OOP). Following are different contexts where abstract can be used in Java.
~~~java
abstract;
~~~

**Abstract Classes in Java**

---
The class which is having partial implementation(i.e. not all methods present in the class have method definitions). To declare a class abstract, use this general form :  
~~~java
abstract class class-name{

    //body of class

}
~~~

Due to their partial implementation, we cannot instantiate abstract classes. Any subclass of an abstract class must either implement all of the abstract methods in the super-class or be declared abstract itself. Some of the predefined classes in Java are abstract. They depend on their sub-classes to provide a complete implementation. 

**Characteristics of Java abstract class :**

- Abstract classes cannot be instantiated: An abstract class is a class that cannot be instantiated directly. Instead, it is meant to be extended by other classes, which can provide concrete implementations of its abstract methods.
- Abstract classes can have both abstract and concrete methods: Abstract classes can contain both abstract and concrete methods. Concrete methods are implemented in the abstract class itself and can be used by both the abstract class and its subclasses.
- Abstract classes can have constructors: Abstract classes can have constructors, which are used to initialize instance variables and perform other initialization tasks. However, because abstract classes cannot be instantiated directly, their constructors are typically called constructors in concrete subclasses.
- Abstract classes can implement interfaces: Abstract classes can implement interfaces, which define a set of methods that must be implemented by any class that implements the interface. In this case, the abstract class must provide concrete implementations of all methods defined in the interface.

**Abstract Methods in Java**

---

Sometimes, we require just method declaration in super-classes. This can be achieved by specifying the abstract type modifier. These methods are sometimes referred to as subclasses responsibility because they have no implementation specified in the super-class. Thus, a subclass must override them to provide a method definition. To declare an abstract method, use this general form:
~~~java
abstract type method-name(parameter-list);
~~~
![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 016](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/139f23b6-2e73-4f13-8b1f-f0addb669053)


**Important rules for abstract methods**

---

- Any class that contains one or more abstract methods must also be declared abstract
- Abstract methods do not have a body: An abstract method is a method that does not have an implementation. It is declared using the abstract keyword and ends with a semicolon instead of a method body.

**Example of Abstraction:**

TestAbstraction1.java
~~~java
    abstract class Shape{

    abstract void draw();

    }
~~~

~~~java
    //In real scenario, implementation is provided by others i.e. unknown by end user  
    class Rectangle extends Shape{  
    void draw(){
System.out.println("drawing rectangle");
}  
    }

    class Circle1 extends Shape{  
    void draw(){
System.out.println("drawing circle");
}  
    }

    //In real scenario, method is called by programmer or user  
    class TestAbstraction1{  
    public static void main(String args[]){  
    Shape s=new Circle1();//In a real scenario, object is provided through method, e.g., getShape() method

    s.draw();  
    }  
    }  
~~~
**Output:**
~~~
drawing circle
~~~
