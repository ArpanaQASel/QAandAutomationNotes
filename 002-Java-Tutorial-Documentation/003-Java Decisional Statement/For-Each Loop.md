

# For-Each Loop

Enhanced For Loop or Java For-Each loop in Java is another version of for loop introduced in Java 5. Enhanced for loop provides a simpler way to iterate through the elements of a collection or array. It is inflexible and should be used only when there is a need to iterate through the elements in a sequential manner without knowing the index of the currently processed element.

**Syntax**

~~~java
for (T element: Collection obj/array)

{

    // loop body

   // statement(s)

}
~~~

**Control Flow**

![Aspose Words 961e2e08-e773-471c-8bd0-982c88ba3fa7 008](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/72089ef2-f8bc-4ab9-bb75-855d122cabc4)

**Example**

~~~java
class Easy
  
{
  
    public static void main(String[] args)
  
    {
  
        // array declaration
  
        int ar[] = { 10, 50, 60, 80, 90 };
  
        for (int element : ar)
  
            System.out.print(element + " ");
    }
}
~~~

**Output**
~~~
10 50 60 80 90 
~~~
