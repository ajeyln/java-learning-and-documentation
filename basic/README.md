<h1 align ="Center"> Basic Concepts </h1>

In this, I have noted down some basic java concepts.

## Table of Content

* [Content](#content)
    + [Introduction](#introduction)
	+ [Java Comments](#coments)
	+ [Variables](#variable)
		+ [Declaring Variables](#declare)
		+ [Final Variables](#final)
		+ [Identifiers](#identifiers)
	+ [Data Types](#datatypes)
		+ [Primitive Data Types](#primitive)
		+ [Non-primitive Data Types](#nonprimitive)
	+ [Type Casting](#casting)
	+ [Operators](#operators)
	+ [String](#string)
	+ [Math](#math)
	+ [Boolean](#boolean)
	+ [Conditional Statements](#condition)
		+ [If Statement](#if)
		+ [If..else](#ifelse)
		+ [Else..if](#elseif)
		+ [Switch](#switch)
	
* [Reference](#Reference)
* [Useful Links](#useful_links)

## <a name="introduction"></a>Introduction

Java is popular programming language. In Java, every application starts with with class name and that class must match the filename.

Eg: 
```java
public class main{
	public static void main(String[] args){
		System.out.println("Hellow World!!");
	}
}
```
 The out put for the above example is Hellow world!!

+ In the java program, every line of codes must be under class and in the above example, class is named as **Main**. <br />
A class should always start with an uppercase. while saving the file, we need to save with".java"to the end of the filename. <br />

+  The main() method is required for java program and it is the starting point of java program or the entry point from where the code <br />
should start to execute. 

+ The System.out.println() method to print a line of text on the screen or is command to show the output of executed code.


## <a name="coments"></a>Java Comments

Comments can be used to explain java code and it should be simple and easy to understand. It can also be used to prevent execution <br />
when testing alternative code.

**Single-line Comments**
	* Single-line comments start with two forward slashes (//).
	* Any text between // and the end of the line is ignored by Java (will not be executed).

Eg:
```java
// This is a single-line comment
System.out.println("Hello World");
```

**Multi-line Comments**
	* Multi-line comments start with /* and ends with */.
	* Any text between /* and */ will be ignored by Java.

Eg:
```java
/* This is a multi-line comments, which we normally use 
when the comments are very long */
System.out.println("Hello World");
```

## <a name="variable"></a>**Variables** 

Variables are containers for storing data values. There are different types of variables

| **Variable** | **Explaination** | 
|----------|--------------|
| String | stores text and String values are surrounded by double quotes |
| int | stores integers (whole numbers), without decimals|
| float | stores floating point numbers, with decimals |
| char  |  stores single characters and Char values are surrounded by single quotes. |
| boolean  | stores values with two states: true or false |

### <a name="declare"></a>**Declaring Variables** 

To create/declare a variable, we must specify the type and assign it a value.

The general rules for naming variables are as follows 

+ Names can contain letters, digits, underscores and dollar signs.
+ Names must begin with a letter or can also begin with $ and _ (underscore)
+ Names should not contain whitespace & Reserved words cannot be used as names
+ Names are case sensitive ("myVar" and "myvar" are different variables).

Syntax : **type variableName = value;**

Eg: 
```java
String name = "Java";
```
In the above example,variable called name of type String and assign it the value "Java".

We can also declare a variable without assigning the value and assign the value later. <br />
If we assign a new value to an existing variable, it will overwrite the previous value/s.

Eg: 
```java
int empNum;
empNum = 15;
```

### <a name="final"></a>**Final Variables** 

If we declare variable and assign the value with final keyword, It is not spossible change or overwrite existing values.

Eg:
```java
final int empNum = 15;
empNum = 20;  // will generate an error: cannot assign a value to a final variable
```

### <a name="identifiers"></a>**Identifiers** 

All Java variables must be identified with unique names and these are called as identifiers. <br />
Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume) and it is recommended  <br />
to use descriptive names in order to create understandable and maintainable code.

Eg: 
```java
String empName = "Albert"
char empIntial = 'D';
int empNum = 11355;
float yearOfExp = 5.99f;
```

## <a name="datatypes"></a>**Data Types** 

Data types are divided into two types :

* Primitive data types - includes byte, short, int, long, float, double, boolean and char
* Non-primitive data types - such as String, Arrays and Classes.

### <a name="primitive"></a>**Primitive Data Types** 

A primitive data type specifies the size and type of variable values, and it has no additional methods. <br />

| **Data Type** | **Size** | **Description** |
----------|--------------|-------------- |
| byte |	1 byte |	Stores whole numbers from -128 to 127 |
| short |	2 bytes |	Stores whole numbers from -32,768 to 32,767 | 
| int |	4 bytes |	Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
| long |	8 bytes |	Stores whole numbers from -9,223,372,036,854,775,808 to 9, 223,372,036,854,775,807 |
| float |	4 bytes |	Stores fractional numbers and stores upto 7 decimal digits |
| double |	8 bytes |	Stores fractional numbers and store upto 15 decimal digits |
| boolean | 1 bit |	Stores true or false values |
| char |	2 bytes |	Stores a single character or ASCII values |

Primitive Data Types are further divided into two groups.

+ **Integer types**, which stores whole numbers, positive or negative without decimals and those are byte, short, int and long <br />

| **Data Type**| **Value** |
----------|-------------- |
| byte  |Stores whole numbers from -128 to 127 |
| short |Stores whole numbers from -32768 to 32767 |
| int  |Stores whole numbers from -2147483648 to 2147483647 |
| long  |Stores whole numbers from -9223372036854775808 to 9223372036854775807<br /> (We should end the value with an "L") |

+ **Floating point types** represents numbers with a fractional part, containing one or more decimals and there are two types: float and double.

| **Data Type**| **Value** |
----------|-------------- |
| float   |Stores whole numbers from 3.4e−038 to 3.4e+038 <br /> (We should end the value with an "f") |
| double   |Stores whole numbers from 1.7e−308 to 1.7e+308 <br /> (We should end the value with an "d") |

### <a name="nonprimitive"></a>**Non-Primitive Data Types** 

Non-primitive data types are called reference types because they refer to objects.

Charecteristic of Non-primitive data types

+ Non-primitive types are created by the programmer and is not defined by Java (except for String)
+ Non-primitive types can be used to call methods to perform certain operations.
+ Non-primitive types always starts with an uppercase letter.
+ Non-primitive types have all the same size.

## <a name="casting"></a>Type Casting

Type casting is when you assign a value of one primitive data type to another type and there are two types of casting:

* Widening Casting (automatically) - converting a smaller type to a larger type size
**byte -> short -> char -> int -> long -> float -> double** and it is done automatically <br />
when passing a smaller size type to a larger size type.

Eg: 
```java
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```

* Narrowing Casting (manually) - converting a larger type to a smaller size type 
**double -> float -> long -> int -> char -> short -> byte**and must be done manually <br />
by placing the type in parentheses in front of the value.

Eg: 
```java
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```

## <a name="operators"></a>Operators

Operators are used to perform operations on variables and values and it is divided into 4 groups

* Arithmetic operators: Arithmetic operators are used to perform common mathematical operations.

| **Operator**| **Name** | **Description**| **Example** |
|----------|-------------- |------------------|----------|
|	+	|	Addition	|	Adds together two values	|	x + y	|
|	-	|	Subtraction	|	Subtracts one value from another	|	x - y	|
|	*	|	Multiplication	|	Multiplies two values	|	x * y	|
|	/	|	Division	|	Divides one value by another	|	x / y	|
|	%	|	Modulus	|	Returns the division remainder	|	x % y	|
|	++	|	Increment	|	Increases the value of a variable by 1	|	++x	|
|	--	|	Decrement	|	Decreases the value of a variable by 1	|	 --x	|


* Assignment operators: Assignment operators are used to assign values to variables.

| **Operator**| **Example** | **Same**|
|----------|-------------- |----------|
|	=	|	x = 5	|	x = 5	|
|	+=	|	x += 3	|	x = x + 3	|
|	-=	|	x -= 3	|	x = x - 3	|
|	*=	|	x *= 3	|	x = x * 3	|
|	/=	|	x /= 3	|	x = x / 3	|
|	%=	|	x %= 3	|	x = x % 3	|
|	&=	|	x &= 3	|	x = x & 3	|
|	\|=	|	x |= 3	|	x = x | 3	|
|	^=	|	x ^= 3	|	x = x ^ 3	|
|	>>=	|	x >>= 3	|	x = x >> 3	|
|	<<=	|	x <<= 3	|	x = x << 3	|


* Comparison operators: Comparison operators are used to compare two values

| **Operator**| **Name** | **Example**|
|----------|-------------- |----------|
|	==	|	Equal to	|	x == y	|
|	!=	|	Not equal	|	x != y	|
|	>	|	Greater than	|	x > y	|
|	<	|	Less than	|	x < y	|
|	>=	|	Greater than or equal to	|	x >= y	|
|	<=	|	Less than or equal to	|	x <= y	|

* Logical operators: Logical operators are used to determine the logic between variables or values

| **Operator**| **Name** | **Description**| **Example** |
|----------|-------------- |------------------|----------|
|	&& 	|	Logical and	|	Returns true if both statements are true	|	x < 5 &&  x < 10	|
|	\|\| 	|	Logical or	|	Returns true if one of the statements is true	|	x < 5 \|\| x < 4	|
|	!	|	Logical not	|	Reverse the result, returns false if the result is true	|	!(x < 5 && x < 10)	|

## <a name="string"></a>String

A String variable contains a collection of characters surrounded by double quotes

Eg:
```java
String greeting = "Hello";
```

* The length() method to find the length of the string

Eg:
```java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println("The length of the txt string is: " + txt.length()); //output 26
```

*  The toUpperCase() to make the string to upper case charecters and toLowerCase() to string to Lower case charecters <br />

Eg:
```java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Outputs "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Outputs "hello world"
```

* The indexOf() method returns the index (the position) of the first occurrence of a specified text in a string

Eg:
```java
String txt = "Please locate where 'locate' occurs!";
System.out.println(txt.indexOf("locate")); // Outputs 7
```

* concat() method to concatenate two strings and we can also "+" operator to concatenate two strings.

Eg: 
```java
String firstName = "Ajey ";
String lastName = "Nayak";
System.out.println(firstName.concat(lastName)); // outputs "Ajeya Nayak"
```

* Special charecter - There are 6 valid escape valid sequences in java <br />

|	**Code**	|	**Result** |
|-----------|---------|	
|	\n	|	New Line |
|	\t	|	Tab |
|	\b	|	Backspace |
|	\f	|	Form Feed |

* The backslash (\) escape character turns special characters into string characte

|	**Escape character**	|	**Result** | **Description** |
|-----------|---------|--------|
|	\'	|	'	|	Single quote	|
|	\"	|	"	|	Double quote	|
|	\\	|	\	|	Backslash	|

## <a name="math"></a>Math

The Java Math class has many methods that allows you to perform mathematical tasks on numbers.

| **Method**| **Description** | **Example**|
|----------|-------------- |----------|
|	Math.max(x,y	|	 used to find the highest value of x and y	|	Math.max(5, 10); //outputs 10	|
|	Math.min(x,y)	|	used to find the lowest value of x and y	|	Math.min(5, 10); //outputs 5	|
|	Math.sqrt(x)	|	 method returns the square root of x	|	Math.sqrt(64); //outputs 8	|
|	Math.abs(x)	|	method returns the absolute (positive) value of x	|	Math.abs(-4.7);//Outputs 4.7	|
|	Math.random()	|	 returns a random number between 0.0 (inclusive), and 1.0 (exclusive)	|	Math.random()	|

## <a name="boolean"></a>Boolean

Java has a boolean data type, which can take the values true or false.A boolean type is declared <br />
with the boolean keyword and can only take the values true or false.

Eg: 
```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```

## <a name="condition"></a>Conditional Statements

Java has the following conditional statements and these conditions to perform different actions for different decisions.

+ **if** to specify a block of code to be executed, if a specified condition is true
+ **else** to specify a block of code to be executed, if the same condition is false
+ **else if** to specify a new condition to test, if the first condition is false
+ **switch** to specify many alternative blocks of code to be executed

### <a name="if"></a>If Statement

This statement will enable to execute block of codes, if the condition is **true**.

Syntax: <br />
if (condition) {
  // block of code to be executed if the condition is true
}

Eg: 
```java
if (20 > 18) {
  System.out.println("20 is greater than 18"); //outputs 20 is greater than 18
}
```

### <a name="ifelse"></a>Else Statement

This statement will enable to execute block of codes , if the condition is **false**

Syntax: <br />
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}

Eg:
```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```

### <a name="elseif"></a>Else...if Statement

We can use the else if statement to specify a new condition if the first condition is **false**.

Syntax: <br/>
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}

Eg:
```java
int x = 30;

      if( x == 10 ) {
         System.out.print("Value of X is 10");
      }else if( x == 20 ) {
         System.out.print("Value of X is 20");
      }else if( x == 30 ) {
         System.out.print("Value of X is 30");
      }else {
         System.out.print("This is else statement");
      }
   }
}
// outputs Value of X is 30
```


### <a name="switch"></a>Switch Statement

We can use Switch statement to select one of many code blocks to be executed. <br/>

These statements are work on the following manner:

+ The switch expression is evaluated once.
+ The value of the expression is compared with the values of each case.
+ If there is a match, the associated block of code is executed.
+ The break and default keywords are optional. Default keyword specifies some code to run if there is no case match

Syntax: <br />
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}

Eg: 
```java
int day = 4;
switch (day) {
  case 1:
    System.out.println("Monday");
    break;
  case 2:
    System.out.println("Tuesday");
    break;
  case 3:
    System.out.println("Wednesday");
    break;
  case 4:
    System.out.println("Thursday");
    break;
  case 5:
    System.out.println("Friday");
    break;
  case 6:
    System.out.println("Saturday");
    break;
  case 7:
    System.out.println("Sunday");
    break;
  default:
    System.out.println("Day is not found!!");
}
// Outputs "Thursday" (day 4)
```
