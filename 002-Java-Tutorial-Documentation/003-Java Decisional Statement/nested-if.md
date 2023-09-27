

# nested-if:

A nested if is an if statement that is the target of another if or else. Nested if statements mean an if statement inside an if statement. Yes, java allows us to nest if statements within if statements. i.e., we can place an if statement inside another if statement.

**Syntax:**
~~~java
if (condition1)

{

   // Executes when condition1 is true

   if (condition2) 

  {

      // Executes when condition2 is true

}

}
~~~
**Control Flow**

![Aspose Words 961e2e08-e773-471c-8bd0-982c88ba3fa7 003](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/0b99bba6-a23b-4685-9ced-93f47493099f)



**Example**
~~~java
class guvi
{  
    public static void main(String args[])
    {
        int a=10;
          int b=20;
       
        if(a==10){
            if(b==20){
                System.out.println("welcome");
            }
        }
    }
}

~~~
**Output:**
~~~java
Welcome
~~~
