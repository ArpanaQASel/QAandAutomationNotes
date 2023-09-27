# Multiple Inheritance In Java



Multiple Inheritance is a feature of an object-oriented concept, where a class can inherit properties of more than one parent class. The problem occurs when there exist methods with the same signature in both the superclasses and subclass. On calling the method, the compiler cannot determine which class method to be called and even on calling which class method gets the priority. 

`
Note: Java doesn’t support Multiple Inheritance
`
~~~java
// Java Program to Illustrate Unsupportance of

// Multiple Inheritance 

//  Class 1

// First Parent class

class Parent1 {


  // Method inside first parent class

  void fun() {



    // Print statement if this method is called

    System.out.println("Parent1");

 }

}


// Class 2

// Second Parent Class

class Parent2 {



  // Method inside first parent class
  void fun() {



    // Print statement if this method is called

    System.out.println("Parent2");

  }

}

// Class 3

// Trying to be child of both the classes

class Test extends Parent1, Parent2 {



  // Main driver method

  public static void main(String args[]) {



    // Creating object of class in main() method

    Test t = new Test();



    // Trying to call above functions of class where

`    `// Error is thrown as this class is inheriting

    // multiple classes

    t.fun();

  }

}
~~~
~~~
Output: Compilation error is thrown
~~~


- it throws compiler error when run fun() method as multiple inheritances cause a diamond problem when allowed in other languages like C++. From the code, we see that: On calling the method fun() using Test object will cause complications such as whether to call Parent1’s fun() or Parent2’s fun() method. Therefore, in order to avoid such complications, Java does not support multiple inheritances of classes.

- Multiple inheritance is not supported by Java using classes, handling the complexity that causes due to multiple inheritances is very complex. It creates problems during various operations like casting, constructor chaining, etc, and the above all reason is that there are very few scenarios on which we actually need multiple inheritances, so better to omit it for keeping things simple and straightforward.

**How are the above problems handled for Default Methods and Interfaces?** 

---

Java 8 supports default methods where interfaces can provide a default implementation of methods. And a class can implement two or more interfaces. In case both the implemented interfaces contain default methods with the same method signature, the implementing class should explicitly specify which default method is to be used in some method excluding the main() of implementing class using super keyword, or it should override the default method in the implementing class, or it should specify which default method is to be used in the default overridden method of the implementing class.


**Example :**
~~~java
/ Java program to demonstrate How Diamond Problem

// Is Handled in case of Default Methods



// Interface 1

interface GPI {



    // Default method

    default void show()
    {



        // Print statement

       System.out.println("Default GPI");

    }

}



// Interface 2

// Extending the above interface

interface PI1 extends GPI {

}



// Interface 3

// Extending the above interface

interface PI2 extends GPI {

}



// Main class

// Implementation class code

class TestClass implements PI1, PI2 {



    // Main driver method

    public static void main(String args[])

   {



        // Creating object of this class

       // in main() method

        TestClass d = new TestClass();



        // Now calling the function defined in interface 1

        // from whom Interface 2and 3 are deriving

       d.show();

    }

}
~~~
Output
~~~
Default GPI
~~~

