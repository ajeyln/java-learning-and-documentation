<h1 align=<"center">Conditional Statements</h1>

Java has the following conditional statements and these conditions to perform different actions for different decisions.

+ **if** to specify a block of code to be executed, if a specified condition is true
+ **else** to specify a block of code to be executed, if the same condition is false
+ **else if** to specify a new condition to test, if the first condition is false
+ **switch** to specify many alternative blocks of code to be executed

### if Statement

This statement will enable to execute block of codes, if the condition is **true**.

Syntax: <br />
if (condition) { <br />
  // block of code to be executed if the condition is true <br />
}

Eg: 
```java
if (20 > 18) {
  System.out.println("20 is greater than 18"); //outputs 20 is greater than 18
}
```

### else Statement

This statement will enable to execute block of codes , if the condition is **false**

Syntax: <br />
if (condition) { <br />
  // block of code to be executed if the condition is true <br />
} else { <br />
  // block of code to be executed if the condition is false <br />
}

Eg:
```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```

### else...if Statement

We can use the else if statement to specify a new condition if the first condition is **false**.

Syntax: <br/>
if (condition1) { <br />
  // block of code to be executed if condition1 is true <br />
} else if (condition2) { <br />
  // block of code to be executed if the condition1 is false and condition2 is true <br />
} else { <br />
  // block of code to be executed if the condition1 is false and condition2 is false <br />
}

Eg:
```java
int x = 30;

      if( x == 10 ) {
         System.out.print("Value of X is 10");
      }else if( x == 20 ) {
         System.out.print("Value of X is 20");
      }else if( x == 30 ) {
         System.out.print("Value of X is 30");
      }else {
         System.out.print("This is else statement");
      }
   }
}
// outputs Value of X is 30
```


### switch Statement

We can use Switch statement to select one of many code blocks to be executed. <br/>

These statements are work on the following manner:

+ The switch expression is evaluated once.
+ The value of the expression is compared with the values of each case.
+ If there is a match, the associated block of code is executed.
+ The break and default keywords are optional. Default keyword specifies some code to run if there is no case match

Syntax: <br />
switch(expression) { <br />
  case x: <br />
    // code block <br />
    break; <br />
  case y: <br />
    // code block <br />
    break; <br />
  default: <br />
    // code block <br />
}

Eg: 
```java
int day = 4;
switch (day) {
  case 1:
    System.out.println("Monday");
    break;
  case 2:
    System.out.println("Tuesday");
    break;
  case 3:
    System.out.println("Wednesday");
    break;
  case 4:
    System.out.println("Thursday");
    break;
  case 5:
    System.out.println("Friday");
    break;
  case 6:
    System.out.println("Saturday");
    break;
  case 7:
    System.out.println("Sunday");
    break;
  default:
    System.out.println("Day is not found!!");
}
// Outputs "Thursday" (day 4)
```
