 ## Interface in java


- An interface in Java is a blueprint of a class. It has static constants and abstract methods.
- The interface in Java is a mechanism to achieve abstraction. There can be only abstract methods in the Java interface, not method body. It is used to achieve abstraction and multiple inheritance in Java.
- In other words, you can say that interfaces can have abstract methods and variables. It cannot have a method body.

**Why use Java interface?**

---

- There are mainly three reasons to use interface. They are given below.
- It is used to achieve abstraction.
- By interface, we can support the functionality of multiple inheritance.
- It can be used to achieve loose coupling.

**How to declare an interface?**

**Syntax:**
~~~java
interface <interface_name>{  



    // declare constant fields  

    // declare methods that abstract   

    // by default.  

}  

~~~
#### Internal addition by the compiler

---

The Java compiler adds public and abstract keywords before the interface method. Moreover, it adds public, static and final keywords before data members.

In other words, Interface fields are public, static and final by default, and the methods are public and abstract.

![](https://static.javatpoint.com/images/interface.png)

------

##### The relationship between classes and interfaces

---

As shown in the figure given below, a class extends another class, an interface extends another interface, but a class implements an interface.

![](https://static.javatpoint.com/images/core/interfacerelation.jpg)

##### Java Interface Example

~~~java
interface Printable{

    void print();

    }
~~~
~~~java
    interface Showable{

    void show();
 
    }
~~~

~~~java
    class A7 implements Printable,Showable{

public void print(){

System.out.println("Hello");

}

 public void show(){

System.out.println("Welcome");

}  
 public static void main(String args[]){  
    A7 obj = new A7();  
    obj.print();  
    obj.show();  
     }  
    }  
~~~
Output
```
Hello

Welcome
```
