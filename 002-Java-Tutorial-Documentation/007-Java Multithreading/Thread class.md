## Thread class


   
  Thread class provide constructors and methods to create and perform operations on a thread.Thread class extends Object class and implements Runnable interface. 


**Threads can be created by using two mechanisms :** 

---

- Extending the Thread class 
- Implementing the Runnable Interface

**Thread creation by extending the Thread class**

---

We create a class that extends the java.lang.Thread class. This class overrides the run() method available in the Thread class. A thread begins its life inside run() method. We create an object of our new class and call start() method to start the execution of a thread. Start() invokes the run() method on the Thread object.
~~~java
// Java code for thread creation by extending

// the Thread class

class MultithreadingDemo extends Thread {

    public void run()

    {

       try {

            // Displaying the thread that is running
System.out.println("Thread " + Thread.currentThread().getId()

                + " is running");

        }

        catch (Exception e) {

            // Throwing an exception

        System.out.println("Exception is caught");

        }

    }

}



// Main Class

public class Multithread {

    public static void main(String[] args)

    {

       int n = 8; // Number of threads

     for (int i = 0; i < n; i++) {

MultithreadingDemo object= new MultithreadingDemo();

         object.start();

       }

   }

}
~~~
**Output**
~~~
Thread 15 is running

Thread 14 is running

Thread 16 is running

Thread 12 is running

Thread 11 is running

Thread 13 is running

Thread 18 is running

Thread 17 is running
~~~

**Thread creation by implementing the Runnable Interface**

---

We create a new class which implements java.lang.Runnable interface and override run() method. Then we instantiate a Thread object and call start() method on this object.
~~~java
// Java code for thread creation by implementing

// the Runnable Interface

class MultithreadingDemo implements Runnable {

    public void run()
    {

        try {

            // Displaying the thread that is running

System.out.println("Thread " + Thread.currentThread().getId()

                + " is running");

        }

        catch (Exception e) {

    // Throwing an exception

           System.out.println("Exception is caught");

        }

   }

}



// Main Class

class Multithread {

public static void main(String[] args)

{

        int n = 8; // Number of threads

        for (int i = 0; i < n; i++) {

Thread object= new Thread(new MultithreadingDemo());

            object.start();

        }

   }

}
~~~
**Output**
~~~
Thread 13 is running

Thread 11 is running

Thread 12 is running

Thread 15 is running

Thread 14 is running

Thread 18 is running

Thread 17 is running

Thread 16 is running
~~~

**Thread Class vs Runnable Interface** 

---

- If we extend the Thread class, our class cannot extend any other class because Java doesn’t support multiple inheritance. But, if we implement the Runnable interface, our class can still extend other base classes.
- We can achieve basic functionality of a thread by extending Thread class because it provides some inbuilt methods like yield(), interrupt() etc. that are not available in Runnable interface.
- Using runnable will give you an object that can be shared amongst multiple threads.