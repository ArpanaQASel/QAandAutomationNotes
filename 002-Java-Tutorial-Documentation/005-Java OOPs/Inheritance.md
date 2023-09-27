# Inheritance in java

Java, Inheritance is an important pillar of OOP(Object-Oriented Programming). It is the mechanism in Java by which one class is allowed to inherit the features(fields and methods) of another class. In Java, Inheritance means creating new classes based on existing ones. A class that inherits from another class can reuse the methods and fields of that class. In addition, you can add new fields and methods to your current class as well.


**Why Do We Need Java Inheritance?**

---

- Code Reusability: The code written in the Superclass is common to all subclasses. Child classes can directly use the parent class code.
- Method Overriding: Method Overriding is achievable only through Inheritance. It is one of the ways by which Java achieves Run Time Polymorphism.
- Abstraction: The concept of abstract where we do not have to provide all details is achieved through inheritance. Abstraction only shows the functionality to the user.


**Important Terminologies Used in Java Inheritance**

---

- Class: Class is a set of objects which shares common characteristics/ behavior and common properties/ attributes. Class is not a real-world entity. It is just a template or blueprint or prototype from which objects are created.
- Super Class/Parent Class: The class whose features are inherited is known as a superclass(or a base class or a parent class).
- Sub Class/Child Class: The class that inherits the other class is known as a subclass(or a derived class, extended class, or child class). The subclass can add its own fields and methods in addition to the superclass fields and methods.
- Reusability: Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. By doing this, we are reusing the fields and methods of the existing class.


**How to Use Inheritance in Java?**

---

The extends keyword is used for inheritance in Java. Using the extends keyword indicates you are derived from an existing class. In other words, “extends” refers to increased functionality.

Syntax : 
~~~java
class derived-class extends base-class  

{  

   //methods and fields  

}  
~~~
**Java Inheritance Types**

---

Below are the different types of inheritance which are supported by Java.

1. Single Inheritance
1. Multilevel Inheritance
1. Hierarchical Inheritance
1. Multiple Inheritance
1. Hybrid Inheritance


**1. Single Inheritance**

---

In single inheritance, subclasses inherit the features of one superclass. In the image below, class A serves as a base class for the derived class B.

![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 008](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/f079aa30-1c52-4d0c-abe0-82e6b6b328e6)

**Example:**
~~~java
class one {

    public void print_student()

    {

       System.out.println("students");

   }

}



class two extends one {

   public void print_for()

 { System.out.println("for"); }

}

// Driver class

public class Main {

      // Main function
    public static void main(String[] args)

    {

        two g = new two();

        g.print_ student ();

        g.print_for();

        g.print_ student ();

    }

}
~~~

**2. Multilevel Inheritance**

---

In Multilevel Inheritance, a derived class will be inheriting a base class, and as well as the derived class also acts as the base class for other classes. In the below image, class A serves as a base class for the derived class B, which in turn serves as a base class for the derived class C.

![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 009](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/04adb185-5303-4cf5-83e8-3f58644755f8)






**Example:**
~~~java

class one {

    public void print_student()

    {

       System.out.println("Geeks");

    }

}

class two extends one {

    public void print_for() { System.out.println("for"); }

}



class three extends two {

    public void print_student()

    {

        System.out.println("students");

   }

}


// Drived class

public class Main {

    public static void main(String[] args)

    {

        three g = new three();

        g.print_student();

       g.print_for();

        g.print_student();

    }

}

~~~




**3. Hierarchical Inheritance**

---

In Hierarchical Inheritance, one class serves as a superclass (base class) for more than one subclass. In the below image, class A serves as a base class for the derived classes B, C, and D.


![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 010](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/9303bf9c-233d-4dbf-9d57-f8ee30d4da74)


**Example:**
~~~java
class A {

    public void print_A() { System.out.println("Class A"); }

}



class B extends A {

  public void print_B() { System.out.println("Class B"); }

}



class C extends A {

public void print_C() { System.out.println("Class C"); }

}



class D extends A {

    public void print_D() { System.out.println("Class D"); }

}



// Driver Class

public class Test {

   public static void main(String[] args)

    {

       B obj_B = new B();

      obj_B.print_A();

       obj_B.print_B();



       C obj_C = new C();

       obj_C.print_A();

        obj_C.print_C();



        D obj_D = new D();

        obj_D.print_A();

        obj_D.print_D();

    }

}
~~~

**4. Multiple Inheritance**

---

In Multiple inheritances, one class can have more than one superclass and inherit features from all parent classes. Please note that Java does not support multiple inheritances with classes. In Java, we can achieve multiple inheritances only through Interfaces. In the image below, Class C is derived from interfaces A and B.
![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 011](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/797d1c3e-bf1d-47f3-82f8-976813922c87)




**Example :**
~~~java
interface one {

    public void print_student();

}



interface two {

    public void print_for();

}



interface three extends one, two {

    public void print_student();

}

class child implements three {

    @Override
     public void print_student()

    {

       System.out.println("student");
`    }



    public void print_for() { System.out.println("for");
     }

}

// Drived class

public class Main {

   public static void main(String[] args)

    {

        child c = new child();

        c.print_student();

        c.print_for();

        c.print_student();

    }

}
~~~

**5. Hybrid Inheritance**

---

It is a mix of two or more of the above types of inheritance. Since Java doesn’t support multiple inheritances with classes, hybrid inheritance is also not possible with classes. In Java, we can achieve hybrid inheritance only through Interfaces.

![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 012](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/67798de7-0661-448c-8415-9be8b23dbb5b)


**Advantages Of Inheritance in Java:**

---

- Code Reusability: Inheritance allows for code reuse and reduces the amount of code that needs to be written. The subclass can reuse the properties and methods of the superclass, reducing duplication of code.
- Abstraction: Inheritance allows for the creation of abstract classes that define a common interface for a group of related classes. This promotes abstraction and encapsulation, making the code easier to maintain and extend.
- Class Hierarchy: Inheritance allows for the creation of a class hierarchy, which can be used to model real-world objects and their relationships.
- Polymorphism: Inheritance allows for polymorphism, which is the ability of an object to take on multiple forms. Subclasses can override the methods of the superclass, which allows them to change their behavior in different ways.


