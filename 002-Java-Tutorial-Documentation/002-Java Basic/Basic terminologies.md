**Java - Basic terminologies**
----
When we consider a Java program, it can be defined as a collection of objects that communicate via invoking each other's methods. Let us now briefly look into what class, object, methods, and instance variables mean.

- **Class:** The class is a blueprint (plan) of the instance of a class (object). It can be defined as a logical template that shares common properties and methods.

Example 1: Blueprint of the house is class.


- **Object:**  Objects have states and behaviors. Example: A dog has states color, name, and breed as well as behavior such as wagging their tail, barking, and eating. An object is an instance of a class.

- **Methods:** A method is a behavior. A class can contain many methods. It is in methods where the logic are written, data is manipulated and all the actions are executed.


- **Instance Variables :** Each object has its unique set of instance variables. An object's state is created by the values assigned to these instance variables.

- **public static void main(String [] args):** The method main() is the main entry point into a Java program; this is where the processing starts. Also allowed is the signature 

**public static void main(String… args){ ..}**
~~~java
Public Class   class_name {

public static void main(String[] args)

  {

        System.out.println("welcome to GUVI");

    }


            }
~~~
**Output:**
~~~
welcome to GUVI
~~~
**Comments in Java**

---

There are TWO types of comments in Java. 

**Single line Comment**

---

~~~

//System.out.println("This is an comment.");

~~~
**Multiline Comment**

---

~~~
/*

   System.out.println("This is the first line comment.");
    System.out.println("This is the second line comment.");

*/
~~~

**Identifiers in java :**

---
All Java components require names. Names used for classes, variables, and methods are called identifiers.

![identifier](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/example%20of%20identifier.jpg)


  

**Rules to write** **Identifiers :**

---

- All identifiers should begin with a letter (A to Z or a to z), currency character ($) or an underscore (\_).
- After the first character, identifiers can have any combination of characters.
- A key word cannot be used as an identifier.
- We can’t use space in between an identifier.
- Most importantly, identifiers are case sensitive.
- Examples of legal identifiers: age, $salary, \_value, \_\_1\_value.
- Examples of illegal identifiers: 123abc, -salary.

