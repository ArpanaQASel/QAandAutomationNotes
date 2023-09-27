## Exception and Error Handling: ##

Java provides a robust exception handling mechanism to deal with errors during runtime. Exceptions are objects that represent errors. The main keywords are try, catch, throw, throws, and finally.

**Example:**
~~~
try {

int result = 10 / 0; // This will cause an ArithmeticException

} catch (ArithmeticException e) {

System.out.println("An arithmetic error occurred: " + e.getMessage());

}
~~~
