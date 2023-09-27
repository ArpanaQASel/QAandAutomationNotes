# if-else:

The if statement alone tells us that if a condition is true it will execute a block of statements and if the condition is false it won’t. But what if we want to do something else if the condition is false? Here comes the else statement. We can use the else statement with the if statement to execute a block of code when the condition is false.

Syntax:
~~~java
if (condition)

{

    // Executes this block if

   // condition is true

}

else

{

// Executes this block if

// condition is false

}
~~~
**Control flow :**


![Aspose Words 961e2e08-e773-471c-8bd0-982c88ba3fa7 002](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/da560526-3b6a-4a90-a2b0-a02a1f619c10)

**Example:**
~~~java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
}
 else {
  System.out.println("Good evening.");
}
~~~
**Outputs:**
~~~java
Good evening.
~~~

