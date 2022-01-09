<h1 align ="Center"> Data Types</h1>

### Datatypes

Data types are divided into two types :

* Primitive data types - includes byte, short, int, long, float, double, boolean and char
* Non-primitive data types - such as String, Arrays and Classes.

#### Primitive Data Types

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

#### Non-Primitive Data Types

Non-primitive data types are called reference types because they refer to objects.

Charecteristic of Non-primitive data types

+ Non-primitive types are created by the programmer and is not defined by Java (except for String)
+ Non-primitive types can be used to call methods to perform certain operations.
+ Non-primitive types always starts with an uppercase letter.
+ Non-primitive types have all the same size.

### Type Casting

Type casting is when we assign a value of one primitive data type to another type and there are two types of casting:

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
