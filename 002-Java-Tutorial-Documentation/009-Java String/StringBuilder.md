## StringBuilder

StringBuilder in Java represents a mutable sequence of characters. 


~~~java
StringBuilderExample.java

    class StringBuilderExample{  
    public static void main(String args[]){  
    StringBuilder sb=new StringBuilder("Hello ");  

    System.out.println(sb);//prints Hello 
    }  
    }  
~~~
Output:
~~~
Hello 
~~~

**StringBuilder Class in Java** 

---
StringBuilder in Java represents a mutable sequence of characters. Since the String Class in Java creates an immutable sequence of characters, the StringBuilder class provides an alternative to String Class, as it creates a mutable sequence of characters. The function of StringBuilder is very much similar to the StringBuffer class, as both of them provide an alternative to String Class by making a mutable sequence of characters. However, the StringBuilder class differs from the StringBuffer class on the basis of synchronization.


The class hierarchy is as follows:
~~~
java.lang.Object

↳ java.lang

↳ Class StringBuilder

~~~


~~~java
public final class StringBuilder

   extends Object
  implements Serializable, CharSequence
  ~~~

**Constructors in Java StringBuilder Class** 

---

**StringBuilder():** Constructs a string builder with no characters in it and an initial capacity of 16 characters.

**StringBuilder(int capacity):** Constructs a string builder with no characters in it and an initial capacity specified by the capacity argument.

**StringBuilder(CharSequence seq):** Constructs a string builder that contains the same characters as the specified CharSequence.

**StringBuilder(String str):** Constructs a string builder initialized to the contents of the specified string.




**What are the differences between String, StringBuffer and StringBuilder?**

---


|StringBuffer|StringBuilder|
| :-: | :-: |
|StringBuffer operations are thread-safe and synchronized|   StringBuilder operations are not thread-safe are not-synchronized.|
|StringBuffer is to used when multiple threads are working on the same String |StringBuilder is used in a single-threaded environment.|
|StringBuffer performance is slower when compared to StringBuilder|StringBuilder performance is faster when compared to StringBuffer |
|Syntax: StringBuffer var = new StringBuffer(str);|Syntax: StringBuilder var = new StringBuilder(str);|
