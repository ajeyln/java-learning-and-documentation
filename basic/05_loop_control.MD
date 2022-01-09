<h1 align ="Center"> Loop Control </h1>

Loops can execute a block of code as long as a specified condition is reached.
These are handy because they save time, reduce errors, and they make code more readable.

### while Loop

A while loop statement in Java programming language repeatedly executes a target statement as long as a given condition is **true**.

Syntax: <br />
while (condition) { <br />
  // code block to be executed <br />
}

Eg:
```java
public class Test {

   public static void main(String args[]) {
      int x = 10;

      while( x < 20 ) {
         System.out.print("value of x : " + x );
         x++;
         System.out.print("\n");
      }
   }
}
```

//Output
value of x : 10
value of x : 11
value of x : 12
value of x : 13
value of x : 14
value of x : 15
value of x : 16
value of x : 17
value of x : 18
value of x : 19

### do...while 

This loop is a variant of the while loop. This loop will execute the code block once, before
checking if the condition is true, then it will repeat the loop as long as the condition is **true**.

Syntax: <br/>
do { <br />
  // code block to be executed <br />
} <br />
while (condition);

Eg: 
```java
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```
//Output
0
1
2
3
4

### for loop

A for loop is a repetition control structure that allows us to efficiently write a loop that needs to be executed a specific number of times.

A for loop is useful when we know how many times a task is to be repeated.

Syntax: <br />
for (statement 1; statement 2; statement 3) { <br />
  // code block to be executed <br />
}

+ Statement 1 is executed (one time) before the execution of the code block.
+ Statement 2 defines the condition for executing the code block.
+ Statement 3 is executed (every time) after the code block has been executed.

Eg:
```java
public class Test {

   public static void main(String args[]) {

      for(int x = 10; x < 20; x = x + 1) {
         System.out.print("value of x : " + x );
         System.out.print("\n");
      }
   }
}
```