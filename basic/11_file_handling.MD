<h1 align ="Center"> File Handling </h1>

File Handling means how to read from and write to file in Java. java provides the basic input or output package for reading and writing stream. java.io package allows to do all Input and Output task in Java.

### File Methods

|Method| Description|
|-------|----------|
|canRead() | Checks whether file is readable or not |
|canWrite()| Checks wheter the file is writable r not |
|createNewFile() | Creates an empty file |
|delete() | Deletes a file |
|exists() | Checks whether the file exists or not | 
|getName() | return the file name|
|getAbsolutePath() | returns the absolute pathname of the file |
|length() | return the file size in bytes |
|list() | return the array of the file in the directory |
|mkdir() | Creates a directory |

### File Operations

+ **Create a file**

In order to create a file in Java, we need to use the **createNewFile()** method. This method returns a boolean value: true if the file was successfully created, and false if the file already exists. It is recommended that the method is enclosed in a try...catch block.This is necessary because it throws an IOException if an error occurs.

Eg: 
```java
import java.io.File; //Import the File class
import java.io.IOException; //Import IOException class to handle errors

public class CreateFile{
	public static void main(String[] args)
	{
		try{	
			File myObj = new File("F:\\FileHandling\\file1.txt"); // file location 				
			if (myObj.CreateNewFile()){ //Creating an file
				System.out.println("File Created: " + myObj.getName());
			}else{
				System.out.println("File already exists");
			}
		} catch(IOException e){
			System.out.println("An error occured");
			e.printStackTrace();
		}
	}
}
```

+ **Write a file**

we use the FileWriter class together with its write() method to write some text to the file and we should close the file using close() method after writing to the file.

Eg: 
```java
import java.io.FileWriter; //Import the FileWriter class

public class WriteToFile {
	public static void main(String[] args){
		try{
			//File Location
			FileWriter myWriter = new FileWriter("F:\\FileHandling\\file1.txt");
			// Write to the file
			myWriter.write("India is famous for its ancient history");
			myWriter.close(); //Closing a file.
			System.out.println("Successfully wrote to the file");
		} catch(IOException e){
			System.out.println("An error occured");
			e.printStackTrace();
		}
	}
}			
```

+ **Read a file**

There are many available classes in the Java API that can be used to read files in Java, such as Scanner, FileReader, BufferedReader, Files, Scanner, FileInputStream, FileWriter, BufferedWriter, FileOutputStream, etc.

Eg: 
```java
import java.io.File; //Import the File class
import java.util.Scanner; //import the Scanner class

public class ReadfromFile{
	public static void main(String[] args)
	{
		try{	
			File myObj = new File("F:\\FileHandling\\file1.txt");
			Scanner myReader = new Scanner(myObj);
			while (myReader.hasNextLine()) {
				String data = myReader.nextLine();
				System.out.println(data);
			}
			myReader.close();
		} catch(FileNotFoundException e){
			System.out.println("An error occured");
			e.printStackTrace();
		}
	}
}

```
