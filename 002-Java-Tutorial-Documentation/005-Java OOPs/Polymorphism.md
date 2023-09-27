

# Polymorphism in Java


- The word polymorphism means having many forms. In simple words, we can define polymorphism as the ability of a message to be displayed in more than one form. 
- Real-life Illustration Polymorphism: A person at the same time can have different characteristics. Like a man at the same time is a father, a husband, and an employee. So the same person possesses different behavior in different situations. This is called polymorphism. 

**What is Polymorphism in Java?**

---

Polymorphism is considered one of the important features of Object-Oriented Programming. Polymorphism allows us to perform a single action in different ways. In other words, polymorphism allows you to define one interface and have multiple implementations. The word “poly” means many and “morphs” means forms, So it means many forms.

**Types of Java polymorphism**


1. Compile-time Polymorphism
1. Runtime Polymorphism









![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 018](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/28e97c76-644a-40b8-b847-c636ecf0d8d3)











**Compile-Time Polymorphism**

---

It is also known as static polymorphism. This type of polymorphism is achieved by function overloading or operator overloading.

**Method Overloading**

When there are multiple functions with the same name but different parameters then these functions are said to be overloaded. Functions can be overloaded by changes in the number of arguments or/and a change in the type of arguments.
~~~java
// Java Program for Method overloading

// By using Different Types of Argument

class Helper {

    // Method with 2 integer parameters
   static int Multiply(int a, int b)
   {

       // Returns product of integer numbers

       return a \* b;

    }



    // Method 2

    // With same name but with 2 double parameters

   static double Multiply(double a, double b)

    {


       // Returns product of double numbers

        return a \* b;

    }

} 

// Class 2

// Main class

class GFG {



   // Main driver method

    public static void main(String[] args)

    {

       // Calling method by passing
       // input as in arguments

       System.out.println(Helper.Multiply(2, 4));

      System.out.println(Helper.Multiply(5.5, 6.3));

   }

}

~~~

**Runtime Polymorphism**

---

It is also known as Dynamic Method Dispatch. It is a process in which a function call to the overridden method is resolved at Runtime. This type of polymorphism is achieved by Method Overriding. Method overriding, on the other hand, occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.

**Example:**
~~~java
// Java Program for Method Overriding



// Class 1

// Helper class

class Parent {


    // Method of parent class

    void Print()

    {



        // Print statement

        System.out.println("parent class");

    }

}



// Class 2

// Helper class

class subclass1 extends Parent {



   // Method

void Print() { System.out.println("subclass1"); }

}



// Class 3

// Helper class

class subclass2 extends Parent {



// Method

void Print()

    {

        // Print statement

        System.out.println("subclass2");
  }

}

// Class 4

// Main class

class GFG {



    // Main driver method

    public static void main(String[] args)

    {

        // Creating object of class 1

        Parent a;



        // Now we will be calling print methods

        // inside main() method



        a = new subclass1();

    `a.Print();



        a = new subclass2();

       a.Print();

    }
    }
~~~
**Output:**
~~~
subclass1

subclass2
~~~
**Advantages of Polymorphism in Java**

- Increases code reusability by allowing objects of different classes to be treated as objects of a common class.
- Improves readability and maintainability of code by reducing the amount of code that needs to be written and maintained.
- Supports dynamic binding, enabling the correct method to be called at runtime, based on the actual class of the object.
- Enables objects to be treated as a single type, making it easier to write generic code that can handle objects of different type




**Difference between Compile-time Polymorphism and Runtime Polymorphism**



![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 019](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/b7dcb123-56fa-450d-a216-2d104dc7ebfb)