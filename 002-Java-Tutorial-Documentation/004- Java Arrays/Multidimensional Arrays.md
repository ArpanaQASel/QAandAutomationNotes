

# Multidimensional Arrays



Multidimensional arrays are arrays of arrays with each element of the array holding the reference of other arrays. These are also known as Jagged Arrays. A multidimensional array is created by appending one set of square brackets ([]) per dimension. 

**Syntax :**
~~~java
datatype[1st dimension][2nd dimension][]……….[Nth dimension] array name = new datatype[size1][size2]….[size];
~~~
- datatype: Type of data to be stored in the array. For example: int, char, etc.
- dimension: The dimension of the array created. For example: 1D, 2D, etc.
- array name: Name of the array
- size1, size2, …, sizeN: Sizes of the dimensions respectively.

**Examples:**
~~~java
Two-dimensional array:

int[][] twoD\_arr = new int[10][20];

Three-dimensional array:

int[][][] threeD\_arr = new int[10][20][30];
~~~
Size of multidimensional arrays: The total number of elements that can be stored in a multidimensional array can be calculated by multiplying the size of all the dimensions.

**For example:** 
~~~java

array int[][] x = new int[10][20] can store a total of (10*20) = 200 elements. 

array int[][][] x = new int[5][10][20] can store a total of (5*10*20) = 1000 elements.
~~~

- Application of Multi-Dimensional Array
- Multidimensional arrays are used to store the data in a tabular form. For example, storing the roll number and marks of a student can be easily done using multidimensional arrays. Another common usage is to store the images in 3D arrays.
- In dynamic programming questions, multidimensional arrays are used which are used to represent the states of the problem.
- Apart from these, they also have applications in many standard algorithmic problems like:  Matrix Multiplication, Adjacency matrix representation in graphs, Grid search problems.

**Two – dimensional Array (2D-Array)**

---

Two – dimensional array is the simplest form of a multidimensional array. A two – dimensional array can be seen as an array of one – dimensional array for easier understanding.  


**Indirect Declaration –**

**Syntax :**
~~~java
data\_type[][] array\_name = new data\_type[x][y];

 For example: int[][] arr = new int[10][20];
       
       
 ~~~


 **Initialization –** 

 **Syntax:**
~~~java
array\_name[row\_index][column\_index] = value;

     For example: arr[0][0] = 1;
~~~


**Direct Method of Declaration: Syntax:**
~~~java

data\_type[][] array\_name = {

    {valueR1C1, valueR1C2, ....}, 

{valueR2C1, valueR2C2, ....}
};

For example: int[][] arr = {{1, 2}, {3, 4}};

~~~



**Accessing Elements of Two-Dimensional Arrays**

Elements in two-dimensional arrays are commonly referred to by x[i][j] where ‘i’ is the row number and ‘j’ is the column number. 

**Syntax:**
~~~java
 x[row\_index][column\_index]
~~~

**For example:**
~~~java
int[][] arr = new int[10][20];

arr[0][0] = 1;
~~~


**Representation of 2D array in Tabular Format:**

---

A two – dimensional array can be seen as a table with ‘x’ rows and ‘y’ columns where the row number ranges from 0 to (x-1) and column number ranges from 0 to (y-1). A two – dimensional array ‘x’ with 3 rows and 3 columns is shown below:

![Aspose Words fa48cee7-5a27-44b0-b207-89444d2a6cf3 002](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/5129d8ae-0e7a-4cc1-a756-bebf2ebb5745)



**Three – dimensional Array (3D-Array)**

---

Three – dimensional array is a complex form of a multidimensional array. A three-dimensional array can be seen as an array of two – dimensional array for easier understanding. 

**Indirect Method of Declaration:**
~~~java
data\_type[][][] array\_name = new data\_type[x][y][z];

For example: int[][][] arr = new int[10][20][30];
~~~

**Initialization – Syntax:**
~~~java
array\_name[array\_index][row\_index][column\_index] = value;

For example: arr[0][0][0] = 1;
~~~

**Direct Method of Declaration:**
~~~java

data\_type[][][] array\_name = {

{

{valueA1R1C1, valueA1R1C2, ....}, 

{valueA1R2C1, valueA1R2C2, ....}

},

{

{valueA2R1C1, valueA2R1C2, ....}, 

{valueA2R2C1, valueA2R2C2, ....}

}
};

For example: int[][][] arr = { {{1, 2}, {3, 4}}, {{5, 6}, {7, 8}} };
~~~

**Accessing Elements of Three-Dimensional Arrays**

Elements in three-dimensional arrays are commonly referred by x[i][j][k] where ‘i’ is the array number, ‘j’ is the row number and ‘k’ is the column number. 

**Syntax:**
~~~java
x[array\_index][row\_index][column\_index]

~~~

**For example:**
~~~java

int[][][] arr = new int[10][20][30];

arr[0][0][0] = 1;
~~~

`
Note: In arrays if size of array is N. Its index will be from 0 to N-1. Therefore, for row\_index 2, actual row number is 2+1 = 3.
`

**Representation of 3D array in Tabular Format:**

![Aspose Words fa48cee7-5a27-44b0-b207-89444d2a6cf3 003](https://github.com/rhushikesh2000/JAVA_TUTORIAL_/assets/124034778/040bc6a1-f37b-4a87-82bb-4c802517e5a8)




