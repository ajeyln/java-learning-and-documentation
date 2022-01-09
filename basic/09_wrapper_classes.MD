<h1 align ="Center"> Wrapper Classes </h1>

The wrapper class in Java provides the mechanism to convert primitive into object and object into primitive. <br />
Java supports only call by value. So, if we pass a primitive value, it will not change the original value. <br /> 
But, if we convert the primitive value in an object, it will change the original value.

The table below shows the primitive type and the equivalent wrapper class:

|	Primitive Data Type	|	Wrapper Class		|
|	-------------------	|	-------------------	|
|	byte			|	Byte			|
|	short			|	Short			|
|	int			|	Integer		|
|	long			|	Long			|
|	float			|	Float			|
|	double			|	Double			|
|	boolean		|	Boolean		|
|	char			|	Character		|

### Autoboxing

The automatic conversion of primitive data type into its corresponding wrapper class.

Eg:
```java
    //Java program to convert primitive into objects  
    //Autoboxing example of int to Integer  
    public class WrapperExample1{  
    public static void main(String args[]){  
    //Converting int into Integer  
    int a=20;  
    Integer i=Integer.valueOf(a);//converting int into Integer explicitly  
    Integer j=a;//autoboxing, now compiler will write Integer.valueOf(a) internally  
      
    System.out.println(a+" "+i+" "+j);  
    }}  
```

### Unboxing

The automatic conversion of wrapper type into its corresponding primitive type is known as unboxing. It is the reverse process of autoboxing.

Eg:
```java
//Java program to convert object into primitives  
//Unboxing example of Integer to int  
public class WrapperExample2{    
public static void main(String args[]){    
//Converting Integer to int    
Integer a=new Integer(3);    
int i=a.intValue();//converting Integer to int explicitly  
int j=a;//unboxing, now compiler will write a.intValue() internally    
    
System.out.println(a+" "+i+" "+j);    
}}   
```
