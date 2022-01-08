<h1 align ="Center"> Encapsulation </h1>

The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users.

Encapsulation in Java is a mechanism of wrapping the data (variables) and code acting on the data (methods) from users. <br />
In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. 

To achieve encapsulation in Java, we must
+ Declare class variables/attributes as private.
+ Provide public get and set methods to access and update the value of a private variable

### Get and Set 

The private variables can only be accessed within the same class using public get and set methods. <br />
The **get** method returns the variable value, and the **set** method sets the value.

Eg:
```java
public class EncapTest {
   private String name;
   private String idNum;
   private int age;

   //getter and  Setter
   public int getAge() {
      return age;
   }

   public String getName() {
      return name;
   }

   public String getIdNum() {
      return idNum;
   }

   public void setAge( int newAge) {
      age = newAge;
   }

   public void setName(String newName) {
      name = newName;
   }

   public void setIdNum( String newId) {
      idNum = newId;
   }
}
```
