<h1 align ="Center"> Variables & Identifiers </h1>

### Variables

Variables are containers for storing data values. There are different types of variables

| **Variable** | **Explaination** | 
|----------|--------------|
| String | stores text and String values are surrounded by double quotes |
| int | stores integers (whole numbers), without decimals|
| float | stores floating point numbers, with decimals |
| char  |  stores single characters and Char values are surrounded by single quotes. |
| boolean  | stores values with two states: true or false |

+ **Declaring Variables** 

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

+ **Final Variables** 

If we declare variable and assign the value with final keyword, It is not spossible change or overwrite existing values.

Eg:
```java
final int empNum = 15;
empNum = 20;  // will generate an error: cannot assign a value to a final variable
```

### Identifiers

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
