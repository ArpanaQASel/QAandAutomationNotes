## File Handling


![file handling ](https://github.com/connectaman/Java_Notes_and_Programs/assets/124034778/70f8a998-cefe-4ff9-a556-d1b578372751)



**Java.io.File Class in Java**

---

Java File class is Java’s representation of a file or directory pathname. Because file and directory names have different formats on different platforms, a simple string is not adequate to name them. Java File class contains several methods for working with the pathname, deleting and renaming files, creating new directories, listing the contents of a directory, and determining several common attributes of files and directories. 

- It is an abstract representation of files and directory pathnames.
- A pathname, whether abstract or in string form can be either absolute or relative. The parent of an abstract pathname may be obtained by invoking the getParent() method of this class.
- First of all, we should create the File class object by passing the filename or directory name to it. A file system may implement restrictions to certain operations on the actual file-system object, such as reading, writing, and executing. These restrictions are collectively known as access permissions.
- Instances of the File class are immutable; that is, once created, the abstract pathname represented by a File object will never change.

**File Operations in Java**

---

In Java, a File is an abstract data type. A named location used to store related information is known as a File. There are several File Operations like creating a new File, getting information about File, writing into a File, reading from a File and deleting a File.

Before understanding the File operations, it is required that we should have knowledge of Stream and File methods. If you have knowledge about both of them, you can skip it.

**Stream**

---

A series of data is referred to as a stream. In Java, Stream is classified into two types, i.e., Byte Stream and Character Stream.

![file-operations-in-java](https://github.com/zen-class/zen-class-automation-testing-documentation/blob/main/diagram/Java%20tutorial-images/O%20Streams.jpg)






**Byte Stream**

---

Byte Stream is mainly involved with byte data. A file handling process with a byte stream is a process in which an input is provided and executed with the byte data.


**Character Stream**

---

Character Stream is mainly involved with character data. A file handling process with a character stream is a process in which an input is provided and executed with the character data.
