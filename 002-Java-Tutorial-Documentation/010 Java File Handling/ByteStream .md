## ByteStream 

ByteStream classes are used to read bytes from the input stream and write bytes to the output stream. In other words, we can say that ByteStream classes read/write the data of 8-bits. We can store video, audio, characters, etc., by using ByteStream classes. These classes are part of the java.io package.

The ByteStream classes are divided into two types of classes, i.e., InputStream and OutputStream. These classes are abstract and the super classes of all the Input/Output stream classes.

**InputStream Class**

---

The InputStream class provides methods to read bytes from a file, console or memory. It is an abstract class and can't be instantiated; however, various classes inherit the InputStream class and override its methods. The subclasses of InputStream class are given in the following table.

|**SN**|**Class**|**Description**|
| :-: | :-: | :-: |
|1|[BufferedInputStream]|This class provides methods to read bytes from the buffer. |
|2|[ByteArrayInputStream]|This class provides methods to read bytes from the byte array.|
|3|[DataInputStream]|This class provides methods to read Java primitive data types.|
|4|[FileInputStream]|This class provides methods to read bytes from a file.|
|5|[FilterInputStream]|This class contains methods to read bytes from the other input streams, which are used as the primary source of data.|
|6|[ObjectInputStream]|This class provides methods to read objects.|
|7|[PipedInputStream]|This class provides methods to read from a piped output stream to which the piped input stream must be connected.|
|8|[SequenceInputStream]|This class provides methods to connect multiple Input Stream and read data from them.|


The InputStream class contains various methods to read the data from an input stream. These methods are overridden by the classes that inherit the InputStream class. However, the methods are given in the following table.


|**SN**|**Method**|**Description**|
| :-: | :-: | :-: |
|1|int read()|This method returns an integer, an integral representation of the next available byte of the input. The integer -1 is returned once the end of the input is encountered.|
|2|int read (byte buffer [])|This method is used to read the specified buffer length bytes from the input and returns the total number of bytes successfully read. It returns -1 once the end of the input is encountered.|
|3|int read (byte buffer [], int loc, int nBytes)|This method is used to read the 'nBytes' bytes from the buffer starting at a specified location, 'loc'. It returns the total number of bytes successfully read from the input. It returns -1 once the end of the input is encountered.|
|4|int available ()|This method returns the number of bytes that are available to read.|
|5|Void mark(int nBytes)|This method is used to mark the current position in the input stream until the specified nBytes are read.|
|6|void reset ()|This method is used to reset the input pointer to the previously set mark.|
|7|long skip (long nBytes)|This method is used to skip the nBytes of the input stream and returns the total number of bytes that are skipped.|
|8|void close ()|This method is used to close the input source. If an attempt is made to read even after the closing, IOException is thrown by the method.|

**OutputStream Class**

---

The OutputStream is an abstract class that is used to write 8-bit bytes to the stream. It is the superclass of all the output stream classes. This class can't be instantiated; however, it is inherited by various subclasses that are given in the following table.

|**SN**|**Class**|**Description**|
| :-: | :-: | :-: |
|1|[BufferedOutputStream]|This class provides methods to write the bytes to the buffer.|
|2|[ByteArrayOutputStream]|This class provides methods to write bytes to the byte array.|
|3|[DataOutputStream]|This class provides methods to write the java primitive data types. |
|4|[FileOutputStream]|This class provides methods to write bytes to a file.|
|5|[FilterOutputStream]|This class provides methods to write to other output streams.|
|6|ObjectOutputStream|This class provides methods to write objects. |
|7|[PipedOutputStream]|It provides methods to write bytes to a piped output stream.|
|8|[PrintStream]|It provides methods to print Java primitive data types.|

The OutputStream class provides various methods to write bytes to the output streams. The methods are given in the following table.


|**SN**|**Method**|**Description**|
| :-: | :-: | :-: |
|1|void write (int i)|This method is used to write the specified single byte to the output stream.|
|2|void write (byte buffer [] )|It is used to write a byte array to the output stream.|
|3|Void write(bytes buffer[],int loc, int nBytes)|It is used to write nByte bytes to the output stream from the buffer starting at the specified location.|
|4|void flush ()|It is used to flush the output stream and writes the pending buffered bytes.|
|5|void close ()|It is used to close the output stream. However, if we try to close the already closed output stream, the IOException will be thrown by this method.|

**Example:**

---

The following example uses the [ByteArrayInputStream] to create an input stream from a byte array "content". We use the read() method to read the content from an input stream. We have also used the write() method on a FileOutputStream object to write the byte array content in the file.

Consider the following example.

~~~java

import java.io.ByteArrayInputStream;  

import java.io.File;  

import java.io.FileInputStream;  

import java.io.FileNotFoundException;  

import java.io.FileOutputStream;  

import java.io.IOException;  





public class InputOutputStreamExample {  





public static void main(String[] args) throws IOException {  

// TODO Auto-generated method stub  

byte content[] = "Jtp is the best website to learn new technologies".getBytes();  

ByteArrayInputStream inputStream = new ByteArrayInputStream(content);  



inputStream.read(content);  



File newFile = new File("/Users/MyUser/Desktop/MyNewFile.doc");  

FileOutputStream outputStream = new FileOutputStream(newFile);  

outputStream.write(content);  



}  





}  

~~~

**Output:**

~~~

A new file MyNewFile.doc will be created on desktop with the content "Jtp is the best website to learn new technologies".

~~~
