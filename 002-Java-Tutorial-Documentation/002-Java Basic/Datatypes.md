




**What are Data Types in Java ?**

---

Data types in Java are of different sizes and values that can be stored in the variable that is made as per convenience and circumstances to cover up all test cases. Java has two categories in which data types are segregated

1. **Primitive Data Type:** such as Boolean, char, int, short, byte, long, float, and double

1. **Non-Primitive Data Type or Object Data type:** such as String, Array, etc.


![Aspose Words d04dd5c6-5058-461f-907f-426e8aa3b525 003](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/data%20types%20in%20java.jpg)






**Primitive Data Types in Java**

---

Primitive data are only single values and have no special capabilities.  There are 8 primitive data types. They are depicted below in tabular format below as follows:



Let us discuss and implement each one of the following data types that are as follows:

1. **Boolean Data Type**

---

Boolean data type represents only one bit of information either **true or false** which is intended to represent the two truth values of logic and Boolean algebra, but the size of the Boolean data type is virtual machine-dependent. Values of type Boolean are not converted implicitly or explicitly (with casts) to any other type. But the programmer can easily write conversion code.

**Syntax**:
~~~
      boolean booleanVar;

~~~
**Size**: Virtual machine dependent.

**2. Byte Data Type**

---

The byte data type is an 8-bit signed two’s complement integer. The byte data type is useful for saving memory in large arrays.

**Syntax:**
~~~
byte byteVar;
~~~
**Size:** 1 byte (8 bits)

**3. Short Data Type**

---

The short data type is a 16-bit signed two’s complement integer. Similar to byte, use a short to save memory in large arrays, in situations where the memory savings actually matters.

**Syntax:** 
~~~
  short shortVar;
~~~
**Size:** 2 bytes (16 bits)

**4.Integer Data Type**

---

It is a 32-bit signed two’s complement integer.

**Syntax:** 
~~~
int intVar;
~~~
**Size:** 4 bytes ( 32 bits )

**5.Long Data Type**

---

The range of a long is quite large. The long data type is a 64-bit two’s complement integer and is useful for those occasions where an int type is not large enough to hold the desired value. The size of the Long Datatype is 8 bytes (64 bits).

**Syntax:** 
~~~
long longVar;
~~~
**6.Float Data Type**

---

The float data type is a single-precision 32-bit IEEE 754 floating-point. Use a float (instead of double) if you need to save memory in large arrays of floating-point numbers. The size of the float data type is 4 bytes (32 bits).

**Syntax:** 
~~~
 float floatVar;
~~~
**7.Double Data Type**

---

The double data type is a double-precision 64-bit IEEE 754 floating-point. For decimal values, this data type is generally the default choice. The size of the double data type is 8 bytes or 64 bits.

**Syntax:**
~~~
double doubleVar;
~~~
**8.Char Data Type**

---


The char data type is a single 16-bit Unicode character with the size of 2 bytes (16 bits).

**Syntax:** 
~~~
  char charVar;
~~~

**Non-Primitive Data Type or Reference Data Types :**

---
The Reference Data Types will contain a memory address of variable values because the reference types won’t store the variable value directly in memory. They are strings, objects, arrays, etc. 





**1.STRINGS** 

---

Strings are defined as an array of characters. The difference between a character array and a string in Java is, that the string is designed to hold a sequence of characters in a single variable whereas, a character array is a collection of separate char-type entities. Unlike C/C++, Java strings are not terminated with a null character.

**Syntax:** Declaring a string
~~~
<String_Type> <string_variable> = “<sequence_of_string>”;
~~~
**Example:** 
~~~java
// Declare String without using new operator 

String s = "welcome to Guvi"; 

// Declare String using new operator 

String s1 = new String("welcome to guvi");

~~~
**Primitive data type vs. non-primitive type in Java**

![difference-between-primitive-and-non-primitive-datatypes-12-1650387712](https://github.com/rhushikesh2000/Java_tutorial/assets/124034778/0be1bcd4-4324-4180-88f8-be280691e24c)









