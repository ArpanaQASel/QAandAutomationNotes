## Bitwise Operator

In Java, an **operator** is a symbol that performs the specified operations. In this section, we will discuss only the **bitwise operator and its types** with proper examples.

**Types of Bitwise Operator**

---

 types of the bitwise operator

- Bitwise AND
- Bitwise exclusive OR
- Bitwise inclusive OR
- Bitwise Compliment
- Bit Shift Operators



|**Operators**|**Symbol**|**Uses**|
| :-: | :-: | :-: |
|Bitwise AND|&|op1 & op2|
|Bitwise exclusive OR|^|op1 ^ op2|
|Bitwise inclusive OR|||op1 | op2|
|Bitwise Compliment|~|~ op|
|Bitwise left shift|<<|op1 << op2|
|Bitwise right shift|>>|op1 >> op2|
|Unsigned Right Shift Operator|>>> op >>>|number of places to shift|

Let's explain the bitwise operator in detail.

**Bitwise AND (&)**

---

It is a binary operator denoted by the symbol **&**. It returns 1 if and only if both bits are 1, else returns 0.

![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 001](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/3b31be6e-995b-498f-80a2-ee150a2b8dff)



Let's use the bitwise AND operator in a Java program.

**BitwiseAndExample.java**

~~~java

public class BitwiseAndExample   

{   

public static void main(String[] args)   

{   

int x = 9, y = 8;   

// bitwise and   

// 1001 & 1000 = 1000 = 8  

System.out.println("x & y = " + (x & y));   

}  

}  
~~~
**Output**
~~~

x & y = 8
~~~

**Bitwise exclusive OR (^)**

---

It is a binary operator denoted by the symbol **^** (pronounced as caret). It returns 0 if both bits are the same, else returns 1.

![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 003](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/b31e6085-6a22-459e-b312-254ddf255876)


**BitwiseXorExample.java**

~~~java
public class BitwiseXorExample   

{   

public static void main(String[] args)   

{   

int x = 9, y = 8;   

// bitwise XOR   

// 1001 ^ 1000 = 0001 = 1  

System.out.println("x ^ y = " + (x ^ y));   

}  

}  
~~~
**Output**
~~~
x ^ y = 1
~~~


**Bitwise inclusive OR (|)**

---

It is a binary operator denoted by the symbol **|** (pronounced as a pipe). It returns 1 if either of the bit is 1, else returns 0.

![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 004](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/eaff96c9-2679-4bcc-adae-bcf37ee9e3f7)

Let's use the bitwise exclusive OR operator in a Java program.

**BitwiseInclusiveOrExample.java**

~~~java
public class BitwiseInclusiveOrExample  

{   

public static void main(String[] args)   

{   

int x = 9, y = 8;   

// bitwise inclusive OR  

// 1001 | 1000 = 1001 = 9  

System.out.println("x | y = " + (x | y));   

}  

}  
~~~
**Output**
~~~
x | y = 9
~~~

**Bitwise Complement (~)**

---

It is a unary operator denoted by the symbol **~** (pronounced as the tilde). It returns the inverse or complement of the bit. It makes every 0 a 1 and every 1 a 0.

![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 005](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/62a111a4-9bdc-4935-9e4b-6b17b8c603a7)

Let's use the bitwise complement operator in a Java program.

**BitwiseComplimentExample.java**

~~~java
public class BitwiseComplimentExample  

{   

public static void main(String[] args)   

{   

int x = 2;   

// bitwise compliment  

// ~0010= 1101 = -3  

System.out.println("~x = " + (~x));   

}  

}  
~~~
**Output**

~~~
~x = -3
~~~


**Bit Shift Operators**

---

Shift operator is used in shifting the bits either right or left. We can use shift operators if we divide or multiply any number by 2. The general format to shift the bit is as follows:

~~~
 variable << or >> number of places to shift;   

For example, if
int a=10:

1. a>>2; //shifts two bits  
1. a>>4; //shifts 4 bits   
~~~

Java provides the following types of shift operators:

- Signed Right Shift Operator or Bitwise Right Shift Operator
- Unsigned Right Shift Operator
- Signed Left Shift Operator or Bitwise Left Shift Operator

`
Note: Java does not support the unsigned left shift operator (<<<).
`

**Signed Right Shift Operator (>>)**

---

The signed right shift operator shifts a bit pattern of a number towards the **right** with a specified number of positions and fills 0. The operator is denoted by the symbol **>>.** It also preserves the leftmost bit (sign bit). If **0** is presented at the leftmost bit, it means the number is **positive**. If **1** is presented at the leftmost bit, it means the number is **negative**.

In general, if we write a>>n, it means to shift the bits of a number toward the right with a specified position (n). In the terms of mathematics, we can represent the signed right shift operator as follows:


![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 006](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/664cf5f3-d8f7-4f4e-84db-092ba96cea74)

`
Note: When we apply right shift operator on a positive number, we get the positive number in the result also. Similarly, when we apply right shift operator on a negative number, we get the negative number in the result also.
`
**Example: Apply the signed right shift operator with specified positions 4 if x = 256 and x = -256.**


~~~
If x = 256

256 >> 4

256/2<sup>4</sup> = 16

If x = -256

-256 >> 4

-256/2<sup>4</sup> = -16
~~~

In the above example, we have observed that after shifting the operator 256 converted into 16 and -256 converted into -16.

Let's create a Java program and implement the left shift operator.

**SignedRightShiftOperatorExample.java**

~~~java
public class SignedRightShiftOperatorExample   

{   

public static void main(String args[])   

{   

int x = 50;   

System.out.println("x>>2 = " + (x >>2));   

}  

}  

~~~
**Output**
~~~
x>>2 = 12
~~~


**Signed Left Shift Operator (<<)**

---

The signed left shift operator (<<) shifts a bit pattern to the left. It is represented by the symbol **<<.** It also preserves the leftmost bit (sign bit). It does not preserve the sign bit.

In general, if we write a<<n, it means to shift the bits of a number toward the left with specified position (n). In the terms of mathematics, we can represent the signed right shift operator as follows:


![Aspose Words 11f50469-bd22-460b-99e4-eb3807001bec 007](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/de5e29c5-4acf-443e-9f3b-8014a36419f9)


**Example 1: What will be the result after shifting a<<3. The value of a is 20.**

---


- Representation of 20 in binary is = 00010100

**After performing the left shift operator, we get:**
~~~
a << 3 = 10100000 (last three bits are the filled bits)

a << 3 = 160
~~~
Let's check the result by using the formula.
~~~
20 << 3

20\*2<sup>3</sup> = 20\*8 = 160
~~~


**Let's create a Java program and implement the signed left shift operator.**


**SignedLeftShiftOperatorExample.java**

~~~java
 public class SignedLeftShiftOperatorExample   
 {   
 public static void main(String args[])   
 {   
 int x = 12;   
 System.out.println("x<<1 = " + (x << 1));   
 }  
 }  

~~~
**Output**
~~~
x<<1 = 24
~~~

**Unsigned Right Shift Operator (>>>)**

---

It shifts a zero at the leftmost position and fills 0. It is denoted by the symbol **>>>.** Note that the leftmost position after >> depends on the sign bit. It does not preserve the sign bit.

**Example:**
~~~
If a=11110000 and b=2,
find a>>>b?

a >>> b = 11110000 >>> 2 = 00111100
~~~
The left operand value is moved right by the number of bits specified by the right operand and the shifted bits are filled up with zeros. Excess bits shifted off to the right are discarded.

Therefore, before shifting the bits the decimal value of a is 240, and after shifting the bits the decimal value of a is 60.

Let's create a Java program and use the unsigned right shift operator.


**UnsignedRightShiftOperatorExample.java**


~~~
public class UnsignedRightShiftOperatorExample   

{   

public static void main(String args[])   

{   

int x = 20;   

System.out.println("x>>>2 = " + (x >>>2));   

}  

}  
~~~
**Output**
~~~
x>>>2 = 5
~~~

