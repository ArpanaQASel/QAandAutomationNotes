
**Lifecycle and States of a Thread in Java**

---

A thread in Java at any point of time exists in any one of the following states. A thread lies only in one of the shown states at any instant:

- New State
- Runnable State
- Blocked State
- Waiting State
- Timed Waiting State
- Terminated State

The diagram shown below represents various states of a thread at any instant in time.

![Lifecycle-and-States-of-a-Thread-in-Java-768](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/JVM2.jpg)


- **New Thread:** When a new thread is created, it is in the new state. The thread has not yet started to run when the thread is in this state. When a thread lies in the new state, its code is yet to be run and hasn’t started to execute.
- **Runnable State:** A thread that is ready to run is moved to a runnable state. In this state, a thread might actually be running or it might be ready to run at any instant of time. It is the responsibility of the thread scheduler to give the thread, time to run. 

A multi-threaded program allocates a fixed amount of time to each individual thread. Each and every thread runs for a short while and then pauses and relinquishes the CPU to another thread so that other threads can get a chance to run. When this happens, all such threads that are ready to run, waiting for the CPU and the currently running thread lie in a runnable state.


- **Blocked/Waiting state:** When a thread is temporarily inactive, then it’s in one of the following states: 
1. Blocked
1. Waiting
- **Timed Waiting:** A thread lies in a timed waiting state when it calls a method with a time-out parameter. A thread lies in this state until the timeout is completed or until a notification is received. For example, when a thread calls sleep or a conditional wait, it is moved to a timed waiting state.
- **Terminated State:** A thread terminates because of either of the following reasons: 
1. Because it exits normally. This happens when the code of the thread has been entirely executed by the program.
1. Because there occurred some unusual erroneous event, like a segmentation fault or an unhandled exception.


**Main thread in Java**

---

Java provides built-in support for multithreaded programming. A multi-threaded program contains two or more parts that can run concurrently. Each part of such a program is called a thread, and each thread defines a separate path of execution.

When a Java program starts up, one thread begins running immediately. This is usually called the main thread of our program because it is the one that is executed when our program begins. 

**There are certain properties associated with the main thread which are as follows:**

---

- It is the thread from which other “child” threads will be spawned.
- Often, it must be the last thread to finish execution because it performs various shutdown actions

The flow diagram is as follows:

![main-thread-in-java](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/JVM1.jpg)

**Java Thread Pool**

---

Java Thread pool represents a group of worker threads that are waiting for the job and reused many times.

In the case of a thread pool, a group of fixed-size threads is created. A thread from the thread pool is pulled out and assigned a job by the service provider. After completion of the job, the thread is contained in the thread pool again.


**Thread Pool Methods**

---

- **newFixedThreadPool(int s):** The method creates a thread pool of the fixed size s.
- **newCachedThreadPool():** The method creates a new thread pool that creates the new threads when needed but will still use the previously created thread whenever they are available to use.
- **newSingleThreadExecutor():** The method creates a new thread.

**Advantage of Java Thread Pool**

---

Better performance It saves time because there is no need to create a new thread.
