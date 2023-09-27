## Examples of Built-in Exception


**A. Arithmetic exception**

---
~~~java
// Java program to demonstrate ArithmeticException
class ArithmeticException_Demo
{
    public static void main(String args[])
    {
        try {
            int a = 30, b = 0;
            int c = a/b;  // cannot divide by zero
            System.out.println ("Result = " + c);
        }
        catch(ArithmeticException e) {
            System.out.println ("Can't divide a number by 0");
        }
    }
}
~~~
Output
~~~
Can't divide a number by 0
~~~


**B. NullPointer Exception**

---
~~~java
//Java program to demonstrate NullPointerException
class NullPointer_Demo
{
    public static void main(String args[])
    {
        try {
            String a = null; //null value
            System.out.println(a.charAt(0));
        } catch(NullPointerException e) {
            System.out.println("NullPointerException..");
        }
    }
}
~~~
Output
~~~
NullPointerException..
~~~

**C. StringIndexOutOfBound Exception**

---

~~~java
// Java program to demonstrate StringIndexOutOfBoundsException
class StringIndexOutOfBound_Demo
{
    public static void main(String args[])
    {
        try {
            String a = "This is like chipping "; // length is 22
            char c = a.charAt(24); // accessing 25th element
            System.out.println(c);
        }
        catch(StringIndexOutOfBoundsException e) {
            System.out.println("StringIndexOutOfBoundsException");
        }
    }
}
~~~
Output
~~~
StringIndexOutOfBoundsException
~~~

**D. FileNotFound Exception**

---

~~~java

//Java program to demonstrate FileNotFoundException
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
 class File_notFound_Demo {
 
    public static void main(String args[])  {
        try {
 
            // Following file does not exist
            File file = new File("E://file.txt");
 
            FileReader fr = new FileReader(file);
        } catch (FileNotFoundException e) {
           System.out.println("File does not exist");
        }
    }
}
~~~
Output:
~~~
File does not exist
~~~

**E. NumberFormat Exception**

---
~~~java

// Java program to demonstrate NumberFormatException
class  NumberFormat_Demo
{
    public static void main(String args[])
    {
        try {
            // "akki" is not a number
            int num = Integer.parseInt ("akki") ;
 
            System.out.println(num);
        } catch(NumberFormatException e) {
            System.out.println("Number format exception");
        }
    }
}
~~~
Output
~~~
Number format exception
~~~

**F. ArrayIndexOutOfBounds Exception**

---

~~~java
// Java program to demonstrate ArrayIndexOutOfBoundException
class ArrayIndexOutOfBound_Demo
{
    public static void main(String args[])
    {
        try{
            int a[] = new int[5];
            a[6] = 9; // accessing 7th element in an array of
                      // size 5
        }
        catch(ArrayIndexOutOfBoundsException e){
            System.out.println ("Array Index is Out Of Bounds");
        }
    }
}

~~~
Output

~~~
Array Index is Out Of Bounds
~~~

**G. IO Exception**

---

~~~java
// Java program to demonstrate IOException
class IOException_Demo {
 
    public static void main(String[] args)
    {
 
        // Create a new scanner with the specified String
        // Object
        Scanner scan = new Scanner("Hello Geek!");
 
        // Print the line
        System.out.println("" + scan.nextLine());
 
        // Check if there is an IO exception
        System.out.println("Exception Output: "
                           + scan.ioException());
 
        scan.close();
    }
}
~~~
Output:
~~~
Hello Geek! 
Exception Output: null
~~~


**H. IllegalArgumentException:**

---
  
This program, checks whether the person is eligible for voting or not. If the age is greater than or equal to 18 then it will not throw any error. If the age is less than 18 then it will throw an error with the error statement. 

Also, we can specify “throw new IllegalArgumentException()” without the error message. We can also specify Integer.toString(variable_name) inside the IllegalArgumentException() and It will print the argument name which is not satisfied the given condition.


~~~java
import java.io.*;
 
class GFG {
   public static void print(int a)
    {
         if(a>=18){
          System.out.println("Eligible for Voting");
          }
          else{
    
          throw new IllegalArgumentException("Not Eligible for Voting");
                                    
          }
       
    }
    public static void main(String[] args) {
         GFG.print(14);
    }
}
~~~
Output : 
~~~

Exception in thread "main" java.lang.IllegalArgumentException: Not Eligible for Voting
at GFG.print(File.java:13)
at GFG.main(File.java:19)
~~~

**I. IllegalStateException:** 

---
This program, displays the addition of numbers only for Positive integers. If both the numbers are positive then only it will call the print method to print the result otherwise it will throw the IllegalStateException with an error statement. Here, the method is not accessible for non-positive integers.

Also, we can specify the “throw new IllegalStateException()” without the error statement.

~~~java
 
import java.io.*;
 
class GFG {
      public static void  print(int a,int b)
     {
         System.out.println("Addition of Positive Integers :"+(a+b));
     }
     
    public static void main(String[] args) {
    int n1=7;
    int n2=-3;
     if(n1>=0 && n2>=0)
     {
         GFG.print(n1,n2);
     }
     else
     {
         throw new IllegalStateException("Either one or two numbers are not Positive Integer");
     }
    }
}
~~~
Output :
~~~
Exception in thread "main" java.lang.IllegalStateException: Either one or two numbers are not Positive Integer
at GFG.main(File.java:20)
~~~
**j. ClassNotFound Exception :**

---
~~~java
// Java program to demonstrate ClassNotFoundException
public class ClassNotFoundException_Demo
{
    public static void main(String[] args) {
        try{
            Class.forName("Class1");   // Class1 is not defined
        }
        catch(ClassNotFoundException e){
            System.out.println(e);
            System.out.println("Class Not Found...");
        }
    }
}
~~~
Output
~~~
java.lang.ClassNotFoundException: Class1
Class Not Found...
~~~


**User-Defined Exceptions**

---

The following program illustrates how to create your own exception class MyException.Details of account numbers, customer names, and balance amounts are taken in the form of three arrays.In main() method, the details are displayed using a for-loop. At this time, a check is done if in any account the balance amount is less than the minimum balance amount to be apt in the account.
If it is so, then MyException is raised and a message is displayed “Balance amount is less”.

Example
~~~java
// Java program to demonstrate user defined exception
 
// This program throws an exception whenever balance
// amount is below Rs 1000
class MyException extends Exception
{
    //store account information
    private static int accno[] = {1001, 1002, 1003, 1004};
 
    private static String name[] =
                 {"Nish", "Shubh", "Sush", "Abhi", "Akash"};
 
    private static double bal[] =
         {10000.00, 12000.00, 5600.0, 999.00, 1100.55};
 
    // default constructor
    MyException() {    }
 
    // parameterized constructor
    MyException(String str) { super(str); }
 
    // write main()
    public static void main(String[] args)
    {
        try  {
            // display the heading for the table
            System.out.println("ACCNO" + "\t" + "CUSTOMER" +
                                           "\t" + "BALANCE");
 
            // display the actual account information
            for (int i = 0; i < 5 ; i++)
            {
                System.out.println(accno[i] + "\t" + name[i] +
                                               "\t" + bal[i]);
 
                // display own exception if balance < 1000
                if (bal[i] < 1000)
                {
                    MyException me =
                       new MyException("Balance is less than 1000");
                    throw me;
                }
            }
        } //end of try
 
        catch (MyException e) {
            e.printStackTrace();
        }
    }
}
~~~
Runtime Error 
~~~
 MyException: Balance is less than 1000
    at MyException.main(fileProperty.java:36)
~~~
Output:  
~~~
ACCNO    CUSTOMER    BALANCE
1001    Nish    10000.0
1002    Shubh    12000.0
1003    Sush    5600.0
1004    Abhi    999.0
~~~
