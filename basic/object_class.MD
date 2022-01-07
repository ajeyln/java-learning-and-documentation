<h1 align ="Center"> Object & Class </h1>

Java is an object-oriented programming language.

Everything in Java is associated with classes and objects, along with its attributes and methods. <br />
For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.

A Class is like an object constructor, or a "blueprint" for creating objects.

### Objects

An entity that has state and behavior is known as an object e.g., chair, bike, marker, pen, table, car, etc.

An object has three characteristics

+ State: represents the data (value) of an object.
+ Behavior: represents the functionality of an object such as deposit, withdraw, etc.
+ Identity: An object identity is typically implemented via a unique ID. The value of the ID is not visible to the external user. However, it is used internally by the JVM to identify each object uniquely.

### Class

A class is a group of objects which have common properties. It is a template or blueprint from which objects are created. It is a logical entity. It can't be physical.

### Creating an Object

A class provides the blueprints for objects. So basically, an object is created from a class. In Java, the new keyword is used to create new objects.

There are three steps when creating an object from a class −

+ Declaration − A variable declaration with a variable name with an object type.
+ Instantiation − The 'new' keyword is used to create the object.
+ Initialization − The 'new' keyword is followed by a call to a constructor. This call initializes the new object.

Eg:
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main(); \\Creating Object myObj
    System.out.println(myObj.x);
  }
}
```

### Creating a Class

A class is a blueprint from which individual objects are created. To create a class, use the keyword **class**

Eg:
```java
public class Dog {
   String breed;
   int age;
   String color;

   void barking() {
   }

   void hungry() {
   }

   void sleeping() {
   }
}
```

A class can have any number of methods to access the value of various kinds of methods. In the above example, barking(), hungry() and sleeping() are methods.
