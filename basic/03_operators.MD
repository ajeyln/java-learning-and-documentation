<h1 align=<"center">Operators</h1>

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

### String

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

### Math

The Java Math class has many methods that allows us to perform mathematical tasks on numbers.

| **Method**| **Description** | **Example**|
|----------|-------------- |----------|
|	Math.max(x,y	|	 used to find the highest value of x and y	|	Math.max(5, 10); //outputs 10	|
|	Math.min(x,y)	|	used to find the lowest value of x and y	|	Math.min(5, 10); //outputs 5	|
|	Math.sqrt(x)	|	 method returns the square root of x	|	Math.sqrt(64); //outputs 8	|
|	Math.abs(x)	|	method returns the absolute (positive) value of x	|	Math.abs(-4.7);//Outputs 4.7	|
|	Math.random()	|	 returns a random number between 0.0 (inclusive), and 1.0 (exclusive)	|	Math.random()	|

### Boolean

Java has a boolean data type, which can take the values true or false.A boolean type is declared <br />
with the boolean keyword and can only take the values true or false.

Eg: 
```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```