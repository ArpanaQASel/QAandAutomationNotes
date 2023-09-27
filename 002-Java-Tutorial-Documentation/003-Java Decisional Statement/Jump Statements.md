

# Jump Statements: 

Java supports three jump statements: break, continue, and return. These three statements transfer control to another part of the program. 

**Break:**

---

In Java, a break is majorly used for
Terminate a sequence in a switch statement or 
To exit a loop.

**Syntax:**
~~~
break;
~~~

*Example:**

~~~java
class guvi {
    public static void main (String[] args) {
      //assigning n as integer value
      int n = 1;
      //passing n to switch
      // it will check n and display output accordingly
      switch(n){
        case 1:
          System.out.println("first case");
          break;
        case 2:
          System.out.println("Second Case");
          break;
        default:
          System.out.println("default case");
      }
    }
}

~~~
**Output:**
~~~
first case
~~~

**Continue:**

---

Sometimes it is useful to force an early iteration of a loop. That is, you might want to continue running the loop but stop processing the remainder of the code in its body for this particular iteration. This is, in effect, a go-to just past the body of the loop, to the loop’s end. The continue statement performs such an action.

**Syntax:**
~~~
continue
~~~

**Example:**

~~~java
public class GFG {
 
    // Main driver method
    public static void main(String args[])
    {
        // For loop for iteration
        for (int i = 0; i <= 15; i++) {
 
            // Check condition for continue
            if (i == 10 || i == 12) {
 
                // Using continue statement to skip the
                // execution of loop when i==10 or i==12
                continue;
            }
            // Printing elements to show continue statement
            System.out.print(i + " ");
        }
    }
}

~~~
**Output**

~~~
0 1 2 3 4 5 6 7 8 9 11 13 14 15 
~~~

**Return:** 

---

The return statement is used to explicitly return from a method. That is, it causes program control to transfer back to the caller of the method.

**Syntax:**

~~~
return;
~~~

**Example**

~~~java
class guvi {
 
    // Method 1
    // Since return type of RR method is double
    // so this method should return double value
    double RR(double a, double b) {
        double sum = 0;
        sum = (a + b) / 2.0;
       
        // Return statement as we already above have declared
        // return type to be double
        return sum;
    }
 
    // Method 2
    // Main driver method
    public static void main(String[] args)
    {
        // Print statement
        System.out.println(new GFG().RR(5.5, 6.5));
    }
}
~~~

**Output**
~~~
6.0
~~~
