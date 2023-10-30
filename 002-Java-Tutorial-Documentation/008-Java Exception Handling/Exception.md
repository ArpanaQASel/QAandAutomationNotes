

# Exceptions in Java

In Java, Exception is an unwanted or unexpected event, which occurs during the execution of a program, i.e. at run time, that disrupts the normal flow of the program’s instructions. Exceptions can be caught and handled by the program. When an exception occurs within a method, it creates an object. This object is called the exception object. It contains information about the exception, such as the name and description of the exception and the state of the program when the exception occurred.

**Major reasons why an exception Occurs**

- Invalid user input
- Device failure
- Loss of network connection
- Physical limitations (out-of-disk memory)
- Code errors
- Opening an unavailable file

**Exception Hierarchy:**

![Exception-in-java1](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/exception.jpg)



**Types of Exceptions**

---

Exceptions can be categorized in two ways:

- **Built-in Exceptions**
1. Checked Exception
1. Unchecked Exception 
- **User-Defined Exceptions**


**1. Built-in Exceptions**

---
Built-in exceptions are the exceptions that are available in Java libraries. These exceptions are suitable to explain certain error situations.

- **Checked Exceptions:** 

Checked exceptions are called compile-time exceptions because these exceptions are checked at compile-time by the compiler.

- **Unchecked Exceptions:** 

The unchecked exceptions are just the opposite to the checked exceptions. The compiler will not check these exceptions at compile time. In simple words, if a program throws an unchecked exception, and even if we didn’t handle or declare it, the program would not give a compilation error.

- **Errors :** 


represent irrecoverable conditions such as Java virtual machine (JVM) running out of memory, memory leaks, stack overflow errors, library incompatibility, infinite recursion, etc. Errors are usually beyond the control of the programmer, and we should not try to handle errors.

**Here are some examples of unchecked exceptions in Java:**

---

- **ArrayIndexOutOfBoundsException:** This exception is thrown when you attempt to access an array index that is out of bounds.

- **NullPointerException:** This exception is thrown when you attempt to access a null object reference.

- **ArithmeticException:** This exception is thrown when you attempt to divide by zero or perform an invalid arithmetic operation.


**2. User-Defined Exceptions:**

---

Sometimes, the built-in exceptions in Java are not able to describe a certain situation. In such cases, users can also create exceptions, which are called ‘user-defined Exceptions’. 

**Methods to print the Exception information:**

---

**1. printStackTrace()**

This method prints exception information in the format of the Name of the exception: description of the exception, stack trace.

**2. toString()** 

The toString() method prints exception information in the format of the Name of the exception: description of the exception.

**3. getMessage()** 

The getMessage() method prints only the description of the exception.
