<h1 align ="Center"> Multi Threading </h1>

Thread is in-built class in java, which allows a program to operate more efficiently by doing multiple things at the same time and also can be used to perform complicated tasks in the background without interrupting the main program.

Every thread needs a method called run() , without run() method it is not possible to start thread.
While calling run()method, use start instead of run() and thread will understand that it should execute run() method.

There are two ways to create a thread 

+ Extending the Thread class and overriding run() method.

Syntax<br />
public class Main extends Thread {
  public void run() {
    System.out.println("This code is running in a thread");
  }
}

Eg: 
```java
class Hallo extends Thread
{
	public void run()
	{
		for(int i=1; i<=5; i++)
		{
			System.out.println("Hallo");
			// it makes thread to pause/suspend for 5 sec and then print.
			try{ Thread.sleep(5000);} catch(Exception e){}
		}
	}
}
class Morning extends Thread
{
	public void run()
	{
		for(int i=1; i<=5; i++)
		{
			System.out.println("Good Morning");
			try{ Thread.sleep(5000);} catch(Exception e){}
		}
	}
}
public class ThreadExample
{
	public static void main(String[] arg)
	{
		Hallo obj1 = new Hallo(); // hallo is thread as it is extended from thread
		Morning obj2 = new Morning();
		
		obj1.start(); //obj1.run();
		try{ Thread.sleep(1000);} catch(Exception e){} // to avoid randomness between two threads.
		obj2.start(); //obj2.run();
				
	}
}
			
```

+ Implement the Runnable interface.

Syntax : <br />
public class Main implements Runnable {
  public void run() {
    System.out.println("This code is running in a thread");
  }
}

Eg: 
```java
class Hallo implements Runnable
{
	public void run()
	{
		for(int i=1; i<=5; i++)
		{
			System.out.println("Hallo");
			// it makes thread to pause/suspend for 5 sec and then print.
			try{ Thread.sleep(5000);} catch(Exception e){}
		}
	}
}
class Morning implements Runnable
{
	public void run()
	{
		for(int i=1; i<=5; i++)
		{
			System.out.println("Good Morning");
			try{ Thread.sleep(5000);} catch(Exception e){}
		}
	}
}
public class ThreadExample
{
	public static void main(String[] arg)
	{
		Runnable obj1 = new Hallo(); //Hallo is reference of runnable
		Runnable obj2 = new Morning();
		
		Thread t1 = new Thread(obj1); // to make obj as thread.
		Thread t2 = new Thread(obj2);
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		t2.start();
				
	}
}
			
```

**Multi threading** using Lambda expression

We can make the code more efficient and also can reduce the number of code blocks using the lambda expressions.


```java
public class ThreadExample
{
	public static void main(String[] arg)
	{
		// runnable can be used as anonymous class
		Runnable obj1 = new Runnable()
		{
			public void run()
			{
				for(int i=1; i<=5; i++)
				{	
					System.out.println("Hallo");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			}
		}; 
		Runnable obj2 = new Runnable()
		{
			public void run()
			{
				for(int i=1; i<=5; i++)
				{
					System.out.println("Good Morning");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			}
		};
		Thread t1 = new Thread(obj1);
		Thread t2 = new Thread(obj2);
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		t2.start();
				
	}
}		
```

The block of the code can reduce after implementing Lambda expression.

```java
public class ThreadExample
{
	public static void main(String[] arg)
	{
		// implenting lambda expression
		Runnable obj1 = () =>
			{
				for(int i=1; i<=5; i++)
				{	
					System.out.println("Hallo");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			}
		; 
		Runnable obj2 = () =>
			{
				for(int i=1; i<=5; i++)
				{
					System.out.println("Good Morning");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			}
		;
		Thread t1 = new Thread(obj1);
		Thread t2 = new Thread(obj2);
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		t2.start();
				
	}
}		
```

The block of code can be further shorten to:

```java
public class ThreadExample
{
	public static void main(String[] arg)
	{
		// implenting lambda expression
		Thread t1 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{	
					System.out.println("Hallo");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		Thread t2 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{
					System.out.println("Good Morning");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		t2.start();
				
	}
}		
```

**Multi threading ** join and isAlive method

+ join method makes current thread invokes method on a second thread, causing the current thread to block until the second thread terminates.

In this below example, Main thread will wait till both threads to terminate and then execute the content in main thread. 

Eg:
```java
public class ThreadExample
{
	public static void main(String[] arg) throws Exception
	{
		// implenting lambda expression
		Thread t1 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{	
					System.out.println("Hallo");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		Thread t2 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{
					System.out.println("Good Morning");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		t2.start();
		t1.join();
		t2.join();
		System.out.print("Welcome"); // main thread contents
				
	}
}		
```

+ isAlive method is to check the running state of the thread.

Eg:
```java
public class ThreadExample
{
	public static void main(String[] arg) throws Exception
	{
		// implenting lambda expression
		Thread t1 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{	
					System.out.println("Hallo");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		Thread t2 = new Thread(() =>
			{
				for(int i=1; i<=5; i++)
				{
					System.out.println("Good Morning");
					try{ Thread.sleep(5000);} catch(Exception e){}
				}
			});
		
		t1.start();
		try{ Thread.sleep(1000);} catch(Exception e){}
		System.out.print(t1.isAlive()); // prints True until the thread is active.
		t2.start();
		t1.join();
		t2.join();
		System.out.print("Welcome"); // main thread contents
				
	}
}		
```

**Multi threading** Synchronized keyword - When two or more threads are using same method or resources, It may result into unforeseen due to concurrency issue. To avoid this type issues, java is introduced the keyword **Synchronized** ,where multiple threads make sure that only one thread can access the resource at a given point in time. 

Eg: 

```java
//The below example is to find the count of looping

class Counter
{
	int count; //initialization
	
	//Synchronized keyword, to make sure only one thread to access the increment() method.
	public synchronized void increment() 
	{
		count++;
	}
}
public class SyncDemo
{
	public static void main(String[] args) throws Exception
	{
		Counter c = new Counter();
		
		Thread t1 = new Thread(new Runnable()
			{
				public void run()
				{
					for(int i=1; i<=1000, i++);
					{
						c.increment();
					}
				}
			});
		Thread t2 = new Thread(new Runnable()
			{
				public void run()
				{
					for(int i=1; i<=1000, i++);
					{
						c.increment();
					}
				}
			});
		t1.start();
		t2.start();
		
		t1.join();
		t2.join(); 
		System.out.println("Count" + c.count);
	}
}	

```
