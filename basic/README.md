<h1 align ="Center"> Basic Concepts </h1>

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


### Java Comments

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
### Basic Concepts – Table of Contents

1. [Variables](./01_variables.md)
2. [Data Types and Casting](./02_datatypes_and_casting.md)
3. [Operators](./03_operators.md)
4. [Conditional Statements](./04_conditional_statements.md)
5. [Loop Control](./05_loop_control.md)
6. [Regular Expression](./06_regular_expressions.md)
7. [Object and Class](./07_object_class.md)
8. [Methods](./08_method.md)
9. [Wrapper Classes](./09_wrapper_classes.md)
10. [Exceptions](./10_exceptions.md)
11. [File Handling](./11_file_handling.md)

* [Reference](#Reference)

* [Useful Links](#useful_links)