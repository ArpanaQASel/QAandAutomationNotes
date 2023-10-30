## StringBuffer

- StringBuffer is a class in Java that represents a mutable sequence of characters. It provides an alternative to the immutable String class, allowing you to modify the contents of a string without creating a new object every time.

- StringBuffer objects are mutable, meaning that you can change the contents of the buffer without creating a new object.
- The initial capacity of a StringBuffer can be specified when it is created, or it can be set later with the ensureCapacity() method.

StringBufferExample.java
~~~java
    class StringBufferExample{  
    public static void main(String args[]){  
    StringBuffer sb=new StringBuffer("Hello ");  
    
    System.out.println(sb);//prints Hello 
    }  
    }  
~~~
Output:
~~~
Hello Java
~~~
**StringBuffer Constructors**


![stringbuffer](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/string%20buffer.jpg)

**Here are some important features and methods of the StringBuffer class:**

---

- **The append():** method is used to add characters, strings, or other objects to the end of the buffer.
- **The insert():** method is used to insert characters, strings, or other objects at a specified position in the buffer.
- **The delete():** method is used to remove characters from the buffer.
- **The reverse():** method is used to reverse the order of the characters in the buffer.

**There are several advantages of using StringBuffer over regular String objects in Java:**

---

- **Mutable:** StringBuffer objects are mutable, which means that you can modify the contents of the object after it has been created. In contrast, String objects are immutable, which means that you cannot change the contents of a String once it has been created.
  
- **Efficient:** Because StringBuffer objects are mutable, they are more efficient than creating new String objects each time you need to modify a string. This is especially true if you need to modify a string multiple times, as each modification to a String object creates a new object and discards the old one.
