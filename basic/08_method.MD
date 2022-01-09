<h1 align ="Center"> Method </h1>

Method is a collection of statements that are grouped together to perform an operationand which only runs whn it is called.
We can pass data known as parameters into method. Methods are used to perform certain actions, and they are also known as functions.

### Create Method

A method must be declared within a class. It is defined with the name of the method, followed by parentheses ().

Syntax: <br />
modifier returnType nameOfMethod (Parameter List) {
   // method body
}

In the above syntax <br /> 
* modifier − It defines the access type of the method and it is optional to use.
* returnType − Method may return a value.
* nameOfMethod − This is the method name and it consists of the method name and the parameter list.
* Parameter − passing data through method(These are optional).

### Call a Method
To call a method in Java, write the method's name followed by two parentheses () and a semicolon.

Syntax : <br />
public class Main {
  static void myMethod() {
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}

// Outputs "I just got executed!"

### Passing parameters by value
Information can be passed to methods as parameter. Parameters act as variables inside the method.
Parameters are specified after the method name, inside the parentheses and need to separate them with a comma.

Eg:
```java
public class Main {
  static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }

  public static void main(String[] args) {
    myMethod("Liam", 5);
    myMethod("Jenny", 8);
    myMethod("Anja", 31);
  }
}

// Liam is 5
// Jenny is 8
```

### Return value
The void keyword indicates that the method should not return a value. If we want the method to return a value, 
we can use a primitive data type instead of void, and use the return keyword inside the method

Eg: 
```java
public class ExampleVoid {

   public static void main(String[] args) {
      methodRankPoints(255.7);
   }

   public static void methodRankPoints(double points) {
      if (points >= 202.5) {
         System.out.println("Rank:A1");
      }else if (points >= 122.4) {
         System.out.println("Rank:A2");
      }else {
         System.out.println("Rank:A3");
      }
   }
}
```

### Method Overloading
When a class has two or more methods by the same name but different parameters, it is known as method overloading. 
It is different from overriding. In overriding, a method has the same method name, type, number of parameters, etc.

Eg:
```java
public class ExampleOverloading {

   public static void main(String[] args) {
      int a = 11;
      int b = 6;
      double c = 7.3;
      double d = 9.4;
      int result1 = minFunction(a, b);
      
      // same function name with different parameters
      double result2 = minFunction(c, d);
      System.out.println("Minimum Value = " + result1);
      System.out.println("Minimum Value = " + result2);
   }

   // for integer
   public static int minFunction(int n1, int n2) {
      int min;
      if (n1 > n2)
         min = n2;
      else
         min = n1;

      return min; 
   }
   
   // for double
   public static double minFunction(double n1, double n2) {
     double min;
      if (n1 > n2)
         min = n2;
      else
         min = n1;

      return min; 
   }
}
/* This produce the following result
Minimum Value = 6
Minimum Value = 7.3 */
```
