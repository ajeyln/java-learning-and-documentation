<h1 align ="Center"> Polymorphism </h1>

Polymorphism is the ability of an object to take on many forms. The most common use of polymorphism in OOP occurs when  a parent class <br /> 
reference is used to refer to a child class object. Inheritance allows inherit attributes and methods from another class. Polymorphism <br /> 
uses those methods to perform different tasks. This allows us to perform a single action in different ways.

Eg:
```java
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object
    myAnimal.animalSound();// The animal makes a sound
    myPig.animalSound();// The pig says: wee wee
    myDog.animalSound();// The dog says: bow wow
  }
}

```
