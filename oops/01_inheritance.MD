<h1 align ="Center"> Inheritance </h1>

Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. With the use of inheritance the information is made manageable in a hierarchical order.

* **subclass (child)** - the class that inherits from another class
* **superclass (parent)** - the class being inherited from

### extends keyword

**extends** is the keyword used to inherit the properties of a class.

Syntax :
```java
class Super {
   .....
   .....
}
class Sub extends Super {
   .....
   .....
}
```

Eg:
```java
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```

### super keyword

**Super** refers to superclass (parent) objects and following are the scenarios where the super keyword is used.
+ It is used to differentiate the members of superclass from the members of subclass, if they have same names.
+ It is used to invoke the superclass constructor from subclass.

Eg:
```java
class Super_class {
   int num = 20;

   // display method of superclass
   public void display() {
      System.out.println("This is the display method of superclass");
   }
}

public class Sub_class extends Super_class {
   int num = 10;

   // display method of sub class
   public void display() {
      System.out.println("This is the display method of subclass");
   }

   public void my_method() {
      // Instantiating subclass
      Sub_class sub = new Sub_class();

      // Invoking the display() method of sub class
      sub.display();

      // Invoking the display() method of superclass
      super.display();

      // printing the value of variable num of subclass
      System.out.println("value of the variable named num in sub class:"+ sub.num);

      // printing the value of variable num of superclass
      System.out.println("value of the variable named num in super class:"+ super.num);
   }

   public static void main(String args[]) {
      Sub_class obj = new Sub_class();
      obj.my_method();
   }
}
```

### Invoking Superclass Constructor

When a class is inheriting the properties of another class, the child class automatically acquires the default constructor of the superclass. But if we want to call a parameterized constructor of the superclass, we need to use the super keyword with value inside parenthesis.

Eg:
```java
class Superclass {
   int age;

   Superclass(int age) {
      this.age = age; 		 
   }

   public void getAge() {
      System.out.println("The value of the variable named age in super class is: " +age);
   }
}

public class Subclass extends Superclass {
   Subclass(int age) {
      super(age);
   }

   public static void main(String args[]) {
      Subclass s = new Subclass(24);
      s.getAge();
   }
}
```

### IS-A Relationship

The concept of IS-A is a totally based on Inheritance, which can be of two types Class Inheritance or Interface Inheritance and is a key point to note that Wherever wesee an extends keyword or implements keyword in a class declaration, then this class is said to have IS-A relationship.

Eg:
```java
public class Animal {
}

public class Mammal extends Animal {
}

public class Reptile extends Animal {
}

public class Dog extends Mammal {
}
```
based on the above example, in Object-Oriented terms, the following are true

+ Mammal IS-A Animal
+ Reptile IS-A Animal
+ Dog IS-A Mammal
+ Hence: Dog IS-A Animal as well

With the use of the extends keyword, the subclasses will be able to inherit all the properties of the superclass except for the private properties of the superclass.

We can assure that Mammal is actually an Animal with the use of the instance operator.

```java
class Animal {
}

class Mammal extends Animal {
}

class Reptile extends Animal {
}

public class Dog extends Mammal {

   public static void main(String args[]) {
      Animal a = new Animal();
      Mammal m = new Mammal();
      Dog d = new Dog();

      System.out.println(m instanceof Animal);// true (Mammal is Animal)
      System.out.println(d instanceof Mammal);// true (Dog is Mammal)
      System.out.println(d instanceof Animal);// true (Dog is Animal)
   }
}
```

### HAS-A Relationship

Composition(HAS-A) simply mean the use of instance variables that are references to other objects and it determines whether a certain class HAS-A certain thing. This relationship helps to reduce duplication of code as well as bugs.

Eg:
```java
public class Bike  
{  
    private String color;  
    private int maxSpeed;  
    public void bikeInfo()  
    {  
        System.out.println("Bike Color= "+color + " Max Speed= " + maxSpeed);  
    }  
    public void setColor(String color)  
    {  
        this.color = color;  
    }  
    public void setMaxSpeed(int maxSpeed)  
    {  
        this.maxSpeed = maxSpeed;  
    }  
}

public class Pulsar extends Bike  
{  
    public void PulsarStartDemo()  
    {  
        Engine PulsarEngine = new Engine();  
        PulsarEngine.stop();  
    }  
} 

public class Engine  
{  
    public void start()  
    {  
        System.out.println("Started:");  
    }  
    public void stop()  
    {  
        System.out.println("Stopped:");  
    }  
} 

public class Demo  
{  
    public static void main(String[] args)  
    {  
        Pulsar myPulsar = new Pulsar();  
        myPulsar.setColor("BLACK");  
        myPulsar.setMaxSpeed(136);  
        myPulsar.bikeInfo();  
       myPulsar.PulsarStartDemo();  
    }  
}  
```
