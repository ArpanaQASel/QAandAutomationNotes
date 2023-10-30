# String 




**What are Strings in Java?**

---

Strings are the type of objects that can store the character of values. A string acts the same as an array of characters in Java.

Example:  
~~~java

String s1 = "Welcome";
~~~









**Ways of Creating a String**

---

**There are two ways to create a string in Java:**

- String Literal
- Using new Keyword


**1. String literal**

---

To make Java more memory efficient (because no new objects are created if it exists already in the string constant pool). 
Each time you create a string literal, the JVM checks the "string constant pool" first. If the string already exists in the pool, a reference to the pooled instance is returned

Example:

~~~java
String s1 = “ WelCome ”;

String s2 = “ WelCome ”;
~~~

![java-string](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/string%20constant2.jpg)


**2. Using new keyword**

---
~~~java
String s = new String(“Welcome”);
~~~
In such a case, JVM will create a new string object in normal (non-pool) heap memory and the literal “Welcome” will be placed in the string constant pool. The variable s will refer to the object in the heap (non-pool)





**Java.lang.String class in Java**

---

![string-implements](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/de4635b0-90b1-43fe-adb1-4fe2abef4d19)




**Strings in java are immutable. Now lets discuss some of the methods provided by String class. Methods:**


---






|**Methods**          |**Description**|
| :- | :- |
|contains()|checks whether the string contains a substring|
|substring()|returns the substring of the string|
|join()|join the given strings using the delimiter|
|replace()|replaces the specified old character with the specified new character|
|replaceAll()|replaces all substrings matching the regex pattern|
|replaceFirst()|replace the first matching substring|
|charAt()|returns the character present in the specified location|
|getBytes()|converts the string to an array of bytes|
|indexOf()|returns the position of the specified character in the string|
|compareTo()|compares two strings in the dictionary order|
|compareToIgnoreCase()|compares two strings ignoring case differences|
|trim()|removes any leading and trailing whitespaces|
|format()|returns a formatted string|
|split()|breaks the string into an array of strings|
|toLowerCase()|converts the string to lowercase|
|toUpperCase()|converts the string to uppercase|
|valueOf()|returns the string representation of the specified argument|
|toCharArray()|converts the string to a char array|
|matches()|checks whether the string matches the given regex|
|startsWith()|checks if the string begins with the given string|
|endsWith()|checks if the string ends with the given string|
|isEmpty()|checks whether a string is empty of not|
|intern() |returns the canonical representation of the string|
|contentEquals()|checks whether the string is equal to charSequence|
|hashCode()|returns a hash code for the string|
|subSequence()|returns a subsequence from the string|

**Why Java Strings are immutable in nature?**

---

The String pool cannot be possible if String is not immutable in Java. A lot of heap space is saved by JRE. The same string variable can be referred to by more than one string variable in the pool. String interning can also not be possible if the String would not be immutable.

If we don’t make the String immutable, it will pose a serious security threat to the application. For example, database usernames, and passwords are passed as strings to receive database connections. The socket programming host and port descriptions are also passed as strings. The String is immutable, so its value cannot be changed. If the String doesn’t remain immutable, any hacker can cause a security issue in the application by changing the reference value.

