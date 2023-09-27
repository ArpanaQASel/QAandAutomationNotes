# Java Methods

The method in Java or Methods of Java is a collection of statements that perform some specific task and return the result to the caller. A Java method can perform some specific task without returning anything. Java Methods allow us to reuse the code without retyping the code.  

1. A method is like a function i.e. used to expose the behavior of an object.

2. It is a set of codes that perform a particular task.Syntax of Method

**Syntax :**
~~~java
<access_modifier> <return_type> <method_name>( list_of_parameters)

{

   //body

}
~~~
**Advantage of Method**

---

- Reusability: Methods allow you to write code once and use it many times, making your code more modular and easier to maintain.
- Abstraction: Methods allow you to abstract away complex logic and provide a simple interface for others to use. This makes your code more readable and easier to understand.
- Improved readability: By breaking up your code into smaller, well-named methods, you can make your code more readable and easier to understand.
- Encapsulation: Methods allow you to encapsulate complex logic and data, making it easier to manage and maintain.
- Improved modularity: Methods allow you to break up your code into smaller, more manageable units, improving the modularity of your code.

**Method Declaration**

---

In general, method declarations have 6 components:

- Modifier: It defines the access type of the method i.e. from where it can be accessed in your application. In Java, there 4 types of access specifiers. 
- The return type: The data type of the value returned by the method or void if does not return a value. It is Mandatory in syntax.
- Method Name: the rules for field names apply to method names as well, but the convention is a little different. It is Mandatory in syntax.
- Parameter list: Comma-separated list of the input parameters is defined, preceded by their data type, within the enclosed parenthesis. If there are no parameters, you must use empty parentheses ().  It is Optional in syntax.
- Method body: it is enclosed between braces. The code you need to be executed to perform your intended operations.  It is Optional in syntax.

![Aspose Words f3723b02-6634-4f10-85b1-e8cd9a1e8868 004](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/4e215dc5-a2c9-415e-8248-e512eb457189)




**Method Calling**

---

The method needs to be called for use its functionality. There can be three situations when a method is called: 

A method returns to the code that invoked it when:  

- It completes all the statements in the method
- It reaches a return statement
- Throws an exception

![java-method-return-value](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/d89d5119-7ea3-45fb-9754-2ac88c8d1cbe)
