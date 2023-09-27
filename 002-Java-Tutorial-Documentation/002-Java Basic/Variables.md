**Java-Variables**
---

Java variable is a name given to a memory location. It is the basic unit of storage in a program.

- The value stored in a variable can be changed during program execution.

- Variables in Java are only a name given to a memory location. All the operations done on the variable affect that memory location.

- In Java, all variables must be declared before use.

**How to Declare Variables in Java?**

---

We can declare variables in Java as pictorially depicted below as a visual aid.

![Aspose Words d04dd5c6-5058-461f-907f-426e8aa3b525 006](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/b8faa581-504a-4b58-97b8-4bd568e91f16)


From the image, it can be easily perceived that while declaring a variable, we need to take care of two things that are:

- **datatype:** Type of data that can be stored in this variable. 

- **data\_name**: Name was given to the variable.


**How to Initialize Variables in Java?**

---

It can be perceived with the help of 3 components that are as follows:

![Variables-Syntax-in-Java](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/61408b89-dcb4-4259-820d-6a38d260331b)

**datatype:** Type of data that can be stored in this variable.

**value:** It is the initial value stored in the variable.



**Types of Variables in Java**

---

Now let us discuss different types of variables which are listed as follows: 

- Local Variables
- Instance Variables
- Static Variables


**1.Local Variables** 

---

A variable defined within a block or method or constructor is called a local variable. 

- These variables are created when the block is entered, or the function is called and destroyed after exiting from the block or when the call returns from the function.
- The scope of these variables exists only within the block in which the variables are declared, i.e., we can access these variables only within that block.
- Initialization of the local variable is mandatory before using it in the defined scope.

Below is the implementation of the above approach:
~~~java
Class guvi {

    public static void main(String[] args)

{

        // Declared a Local Variable

        int var = 10;



       // This variable is local to this main method only

        System.out.println("Local Variable: " + **var**);

    }

}
~~~
**2. Instance Variables**

---

Instance variables are non-static variables and are declared in a class outside of any method, constructor, or block. 

- As instance variables are declared in a class, these variables are created when an object of the class is created and destroyed when the object is destroyed.
- Unlike local variables, we may use access specifiers for instance variables. If we do not specify any access specifier, then the default access specifier will be used.
- Initialization of an instance variable is not mandatory. Its default value is dependent on the data type of variable. 
- Instance variables can be accessed only by creating objects.
- We initialize instance variables using constructors while creating an object. We can also use instance blocks to initialize the instance variables.

~~~java

// Java Program to demonstrate

class Guvi {

	// Declared instance variable

	String student = "Shubham Jain";

	public static void main(String[] args)

{

    Guvi Zen=new Guvi();

		// geek variable can be accessed by creating object

	System.out.print(Zen. student); 
   }

}
~~~
**3.Static Variables**

---

Static variables are also known as class variables. 

- These variables are declared similarly to instance variables. The difference is that static variables are declared using the static keyword within a class outside of any method, constructor, or block.
- Unlike instance variables, we can only have one copy of a static variable per class, irrespective of how many objects we create.
- Static variables are created at the start of program execution and destroyed automatically when execution ends.
- Initialization of a static variable is not mandatory. Its default value is dependent on the data type of variable
~~~java
// Java Program to demonstrate

class guvi {

	// Declared instance variable

	Public static String student = "Shubham Jain";

	public static void main(String[] args)
{


// student variable can be accessed without object

        // static variable

	System.out.print(guvi. student);  }

}
~~~


 **Scope of variables** 

 ---
 
 
 ![scope-and-lifetime-of-a-variable-summary](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/6062056d-fc19-4670-8c06-d20afa21b79f)
