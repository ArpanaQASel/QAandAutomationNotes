## CharacterStream 

The java.io package provides CharacterStream classes to overcome the limitations of ByteStream classes, which can only handle the 8-bit bytes and is not compatible to work directly with the Unicode characters. CharacterStream classes are used to work with 16-bit Unicode characters. They can perform operations on characters, char arrays and Strings.

However, the CharacterStream classes are mainly used to read characters from the source and write them to the destination. For this purpose, the CharacterStream classes are divided into two types of classes, I.e., Reader class and Writer class.

**Reader Class**

---
 is used to read the 16-bit characters from the input stream. However, it is an abstract class and can't be instantiated, but there are various subclasses that inherit the Reader class and override the methods of the Reader class. All methods of the Reader class throw an IOException. The subclasses of the Reader class are given in the following table.

|**SN**|**Class**|**Description**|
| :-: | :-: | :-: |
|1\.|[BufferedReader]|This class provides methods to read characters from the buffer.|
|2\.|[CharArrayReader]|This class provides methods to read characters from the char array. |
|3\.|[FileReader]|This class provides methods to read characters from the file. |
|4\.|[FilterReader]|This class provides methods to read characters from the underlying character input stream.|
|5|[InputStreamReader]|This class provides methods to convert bytes to characters.|
|6|[PipedReader]|This class provides methods to read characters from the connected piped output stream.|
|7|[StringReader]|This class provides methods to read characters from a string.|

**The Reader class methods are given in the following table.**

---

|**SN**|**Method**|**Description**|
| :-: | :-: | :-: |
|1|int read()|This method returns the integral representation of the next character present in the input. It returns -1 if the end of the input is encountered.|
|2|int read(char buffer[])|This method is used to read from the specified buffer. It returns the total number of characters successfully read. It returns -1 if the end of the input is encountered.|
|3|int read(char buffer[], int loc, int nChars)|This method is used to read the specified nChars from the buffer at the specified location. It returns the total number of characters successfully read.|
|4|void mark(int nchars)|This method is used to mark the current position in the input stream until nChars characters are read.|
|5|void reset()|This method is used to reset the input pointer to the previous set mark.|
|6|long skip(long nChars)|This method is used to skip the specified nChars characters from the input stream and returns the number of characters skipped.|
|7|boolean ready()|This method returns a boolean value true if the next request of input is ready. Otherwise, it returns false.|
|8|void close()|This method is used to close the input stream. However, if the program attempts to access the input, it generates IOException.|

**Writer Class**

---

Writer class is used to write 16-bit Unicode characters to the output stream. The methods of the Writer class generate IOException. Like Reader class, Writer class is also an abstract class that cannot be instantiated; therefore, the subclasses of the Writer class are used to write the characters onto the output stream. The subclasses of the Writer class are given in the below table.

|**SN**|**Class**|**Description**|
| :-: | :-: | :-: |
|1|[BufferedWriter]|This class provides methods to write characters to the buffer.|
|2|[FileWriter]|This class provides methods to write characters to the file.|
|3|[CharArrayWriter]|This class provides methods to write the characters to the character array.|
|4|[OutpuStreamWriter]|This class provides methods to convert from bytes to characters.|
|5|[PipedWriter]|This class provides methods to write the characters to the piped output stream. |
|6|[StringWriter]|This class provides methods to write the characters to the string.|

To write the characters to the output stream, the Write class provides various methods given in the following table.

|**SN**|**Method**|**Description**|
| :-: | :-: | :-: |
|1|void write()|This method is used to write the data to the output stream.|
|2|void write(int i)|This method is used to write a single character to the output stream.|
|3|Void write(char buffer[])|This method is used to write the array of characters to the output stream. |
|4|void write(char buffer [],int loc, int nChars)|This method is used to write the nChars characters to the character array from the specified location.|
|5|void close ()|This method is used to close the output stream. However, this generates the IOException if an attempt is made to write to the output stream after closing the stream.|
|6|void flush ()|This method is used to flush the output stream and writes the waiting buffered characters.|

