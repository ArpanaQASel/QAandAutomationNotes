## Packages in java



A package is nothing but a physical folder structure (directory) that contains a group of related classes, interfaces, and sub-packages according to their functionality. It provides a convenient way to organize your work. The Java language has various in-built packages.

**Advantages of using Packages in Java**

---

- **Maintenance:** Java packages are used for proper maintenance. If any developer newly joined a company, he can easily reach to files needed.
- **Reusability:** We can place the common code in a common folder so that everybody can check that folder and use it whenever needed.
- **Name conflict:** Packages help to resolve the naming conflict between the two classes with the same name. 
- **Organized:** It also helps in organizing the files within our project.
- **Access Protection:** A package provides access protection. It can be used to provide visibility control. The members of the class can be defined in such a manner that they will be visible only to elements of that package.

**Types of Packages in Java**

1. User-defined package
1. built-in package (also called predefined package)


**User-defined Package in Java**

---

Naming Convention for User-defined Package in Realtime Project

While developing your project, you must follow some naming conventions regarding packages declaration. Let’s take an example to understand the convention.

![package-naming-convention](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/961ddaa4-2b9a-4eb8-aacf-26b55a501590)


**How to Create Package in Eclipse IDE?**

---

In Eclipse IDE, there are the following steps to create a package in java. They are as follows:

1\.Right-click on the src folder as shown in the below screenshot

![Aspose Words 277065cb-7b3e-4c96-8d8d-65d8f05a614c 002](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/333886ca-f4a5-4006-b252-086d3685c4dd)






2\. Go to New option and then click on package.

A window dialog box will appear where you have to enter the package name according to the naming convention and click on Finish button. Once the package is created, a package folder will be created in your file system where you can create classes and interfaces.


**Predefined Packages in Java (Built-in Packages)**

---

Predefined packages in Java are those which are developed by Sun Microsystem. They are also called built-in packages. These packages consist of a large number of predefined classes, interfaces, and methods that are used by the programmer to perform any task in his programs.

Java APIs contains the following predefined packages, as shown in the below figure:

![Aspose Words 277065cb-7b3e-4c96-8d8d-65d8f05a614c 003](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/bdaae051-6732-4364-97d1-53727c992d97)

**Java Core Packages:**

---

**1. Java. lang:** lang stands for language. The Java language package consists of java classes and interfaces that form the core of the Java language and the JVM. It is a fundamental package that is useful for writing and executing all Java programs. Examples are classes, objects, String, Thread, predefined data types, etc. It is imported automatically into the Java programs.

**2. Java.io:** io stands for input and output. It provides a set of I/O streams that are used to read and write data to files. A stream represents a flow of data from one place to another place.

**3. Java util:** util stands for utility. It contains a collection of useful utility classes and related interfaces that implement data structures like LinkedList, Dictionary, HashTable, stack, vector, Calender, data utility, etc.

**4. Java.net:** net stands for network. It contains networking classes and interfaces for networking operations. The programming related to client-server can be done by using this package.

**Importing Packages in Java**

There are three approaches to import one package into another package in Java.

1. import package.*;
1. import package.classname;

**Using package.**

---




An import is a keyword that is used to make the classes and interfaces of other packages accessible to the current package. If we use package.\*, all the classes and interfaces of this package can be accessed (imported) from outside the packages. Let’s understand it by a simple example program.

![Aspose Words 277065cb-7b3e-4c96-8d8d-65d8f05a614c 004](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/1aa96999-a177-49b9-bf4f-3ce24f9a0839)










**Using packageName.className**

---

If you import packageName.className, you can only access the declared class of this package. 

![60c32dab395ca2b5d181b730_https2F2Fsecure notion-static com2FUntitled_Diagram_(1)](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/790fa364-8a4f-4524-8e4f-77c807350ea5)

**Key points:**

---

1\. While importing another package, package declaration must be the first statement and followed by package import.

2\. A class can have only one package statement but it can be more than one import package statement.

3\. import can be written multiple times after the package statement and before the class statement.

4\. You must declare the package with root folder name (No subfolder name) and the last file name must be class name with a semicolon.
