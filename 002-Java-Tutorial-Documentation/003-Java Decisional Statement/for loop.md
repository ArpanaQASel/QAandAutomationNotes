

# for loop

for loop provides a concise way of writing the loop structure. Unlike a while loop, a for statement consumes the initialization, condition and increment/decrement in one line thereby providing a shorter, easy to debug structure of looping.

**Syntax**
~~~
for (initialization expr; test expr; update exp)**

{

     // body of the loop

    // statements we want to execute

}

~~~
**How does a For loop work?**  

1. Control falls into the for loop. Initialization is done
1. The flow jumps to ConditionCondition is tested. 
1. If the Condition yields true, the flow goes into the Body
1. If the Condition yields false, the flow goes outside the loop
1. The statements inside the body of the loop get executed.
1. The flow goes to the Updation
1. Updation takes place and the flow goes to Step 3 again
1. The for loop has ended and the flow has gone outside.

**Control flow**
![Aspose Words 961e2e08-e773-471c-8bd0-982c88ba3fa7 007](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/for%20loop.jpg)

**Example**

~~~java

class Guvi {
    public static void main(String[] args)
    {
        for (int i = 1; i <= 10; i++) {
            System.out.println(i);
        }
    }
}
~~~

**Output**

~~~
1
2
3
4
5
6
7
8
9
10
~~~
