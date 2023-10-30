

## Exception Handling

Exception Handling in Java is one of the effective means to handle runtime errors so that the regular flow of the application can be preserved. Java Exception Handling is a mechanism to handle runtime errors such as ClassNotFoundException, IOException, SQLException, RemoteException, etc.


**How Programmer Handle an Exception?**

---

There are 5 keywords which are used in handling exceptions in Java.

|Keyword	| Description|
|----------|--------------|
|try	|The "try" keyword is used to specify a block where we should place exception code. The try block must be followed by either catch or finally. It means, we can't use try block alone.|
|catch	|The "catch" block is used to handle the exception. It must be preceded by try block which means we can't use catch block alone. It can be followed by finally block later.|
|finally	|The "finally" block is used to execute the important code of the program. It is executed whether an exception is handled or not.|
|throw|	The "throw" keyword is used to throw an exception.|
|throws	|The "throws" keyword is used to declare exceptions. It doesn't throw an exception. It specifies that there may occur an exception in the method. It is always used with method signature.|


**How to Use the Try-catch Clause?**

**Syntax:**
~~~java
try {
    // block of code to monitor for errors
     // the code you think can raise an exception
     }
      catch (ExceptionType1 exOb) {
          // exception handler for ExceptionType1
          
          } catch (ExceptionType2 exOb) { 
              // exception handler for ExceptionType2
              }
~~~


**Certain key points need to be remembered that are as follows:**   

---

1. In a method, there can be more than one statement that might throw an exception, So put all these statements within their try block and provide a separate exception handler within their catch block for each of them.
1. If an exception occurs within the try block, that exception is handled by the exception handler associated with it. To associate the exception handler, we must put a catch block after it. There can be more than one exception handler. Each catch block is an exception handler that handles the exception to the type indicated by its argument. The argument, ExceptionType declares the type of exception that it can handle and must be the name of the class that inherits from the Throwable class.
1. For each try block, there can be zero or more catch blocks, but only one final block.


![Aspose Words 79714d40-67ba-4a78-a748-ddf1ce86cc4c 002](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/exception%20object.jpg)

**Example**

---

```java
public class JavaExceptionExample{  
  public static void main(String args[]){  
   try{  
      //code that may raise exception  
      int data=100/0;  
   }catch(ArithmeticException e){System.out.println(e);}  
   //rest code of the program   
   System.out.println("rest of the code...");  
  }  
}  
```
Output
```
Exception in thread main java.lang.ArithmeticException:/ by zero
rest of the code...
```


**throw and throws in Java**

---

**Java throw**

The throw keyword in Java is used to explicitly throw an exception from a method or any block of code. We can throw either checked or unchecked exceptions. The throw keyword is mainly used to throw custom exceptions.

**Syntax in Java throw**

~~~java
throw new ArithmeticException("/ by zero");
~~~

**Example:**
```java
public class TestThrow1{  
   static void validate(int age){  
     if(age<18)  
      throw new ArithmeticException("not valid");  
     else  
      System.out.println("welcome to vote");  
   }  
   public static void main(String args[]){  
      validate(13);  
      System.out.println("rest of the code...");  
  }  
}  
```
Output
```
Exception in thread main java.lang.ArithmeticException:not valid
```

**Java throws**

---

throws is a keyword in Java that is used in the signature of a method to indicate that this method might throw one of the listed type exceptions. The caller to these methods has to handle the exception using a try-catch block. 

Syntax of Java throws
~~~java
type method_name(parameters) throws exception_list{


}
~~~
**Example:**

```java
import java.io.IOException;  
class Testthrows1{  
  void m()throws IOException{  
    throw new IOException("device error");//checked exception  
  }  
  void n()throws IOException{  
    m();  
  }  
  void p(){  
   try{  
    n();  
   }catch(Exception e){System.out.println("exception handled");}  
  }  
  public static void main(String args[]){  
   Testthrows1 obj=new Testthrows1();  
   obj.p();  
   System.out.println("normal flow...");  
  }  
}  
```
Output
```
exception handled
normal flow...
```

**Java Custom Exception**

---

In Java, we can create our exceptions that are derived classes of the Exception class. Creating our Exception is known as a custom exception or user-defined exception. Java custom exceptions are used to customize the exception according to user needs.

Consider example 1 in which InvalidAgeException class extends the Exception class.

Using the custom exception, we can have your exception and message. Here, we have passed a string to the constructor of the superclass i.e. Exception class that can be obtained using the getMessage() method on the object we have created.

**Why use custom exceptions?**

---

Java exceptions cover almost all the general types of exceptions that may occur in the programming. However, we sometimes need to create custom exceptions.

Following are a few of the reasons to use custom exceptions:

1. To catch and provide specific treatment to a subset of existing Java exceptions.
2. Business logic exceptions: These are the exceptions related to business logic and workflow. It is useful for the application users or the developers to understand the exact problem.

**finally, block**

---

The finally block in Java is used to put important codes such as clean-up code e.g. closing the file or closing the connection. The finally block executes whether the exception rise or not and whether the exception is handled or not. Finally contains all the crucial statements regardless of whether the exception occurs or not.

**Example:**

```java
class TestFinallyBlock{  
  public static void main(String args[]){  
  try{  
   int data=25/5;  
   System.out.println(data);  
  }  
  catch(NullPointerException e){System.out.println(e);}  
  finally{System.out.println("finally block is always executed");}  
  System.out.println("rest of the code...");  
  }  
}  
```
Output
```
Output:5
       finally block is always executed
       rest of the code...
```
