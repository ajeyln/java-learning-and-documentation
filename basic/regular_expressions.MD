<h1 align ="Center"> Regular Expressions </h1>

A regular expression is sequence of characters that constructs a search pattern. When we search for data in a text,we can use this search pattern to describe what we are searching for.
 
 The Java Regex is an API, which is used to define a pattern for searching or manipulate Strings. It is widely used to define the constraint on Strings such as password and email validation.
 
+ A regular expression can be a single character, or a more complicated pattern.

+ Regular expressions can be used to perform all types of text search and text replace operations.

 We need to import the java.util.regex package to work with regular expressions. <br />
 
 The package includes the following classes:
 
1. Matcher Class - Used to search for the pattern
2. Pattern Class - Defines a pattern (used in a search)
3. PatternSyntaxException Class - Indicates syntax error in a regular expression pattern


### Matcher class <br/> 

It is used to perform the match operations on a character sqeuence and is used to match a character sequence.<br />
There are various method in this class:

|Method| Description|
|-------|----------|
|boolean matches() | Checks whether the given regular expression matches or not |
|boolean find()| Used to find the next expression that matches the pattern |
|boolean find(int start) | Searches the next expression from the given start number |
|int start()| return the starting index |
|int end()| return the ending index |
|int groupCount() | return the total number of the matched sequence | 
 
 ### Pattern class <br/> 
 
 It is the compiled version of regular expression, which is used to define the pattern for a regex engine.<br />
 It consists of various methods
 
 |Method| Description|
|-------|----------|
|Static Pattern compile(String regex) | Compiles the given regex and returns the instance of the pattern |
|Matcher matcher(charSequence input)| Used to create a matcher that matches the given input with the pattern|
|Static boolean matches(String regex) | it works as a combination of compile and matcher methods |
|String split| Used to split the given String around the matches of the given pattern |
|String pattern()| helps to return regex pattern |
|int end()| returns the ending index | 

Eg:
```java
import java.util.regex.*;
public class RegexExample{
	public static void main(String[] args){
		Pattern pattern = Pattern.compile(".xx.");
		Matcher matcher = pattern.matcher("AxxB");
		System.out.println("String matches the given Regex - " + matcher.matches());
	}
}
```

**Regular Expression Patterns**

The first parameter of the Pattern.compile() method is the pattern. It describes what is being searched for.

Brackets are used to find a range of characters:

|	Expression	|	Description	|
|	-------------------	|	-------------------	|
|	[abc]	|	Find one character from the options between the brackets	|
|	[^abc]	|	Find one character NOT between the brackets	|
|	[0-9]	|	Find one character from the range 0 to 9	|

Eg:
```java
import java.util.regex.*;
public class CharacterExample{
	public static void main(String[] args){
		System.out.println("Pattern.matches("[xyz]", "wdcd")); //false (not x or y or z)
		System.out.println("Pattern.matches("[xyz]", "x"));// true (among x or y or z)
		System.out.println("Pattern.matches("[xyz]", "xxyyyyzz"));//false (x and y comes more than once)
	}
}
```

**Regex Quantifiers**

Regex Quantifier specifies the number of occurence of character. It consists of various quantifiers.

|	Quantifier	|	Description	|
|	-------------------	|	-------------------	|
|	n+	|	Matches any string that contains at least one n	|
|	n*	|	Matches any string that contains zero or more occurrences of n	|
|	n?	|	Matches any string that contains zero or one occurrences of n	|
|	n{x}	|	Matches any string that contains a sequence of X n's	|
|	n{x,y}	|	Matches any string that contains a sequence of X to Y n's	|
|	n{x,}	|	Matches any string that contains a sequence of at least X n's	|

Eg:
```java
import java.util.regex.*;
public class Quant{
	public static void main(String[] args){
		System.out.println("? Quantifier....."); 
		System.out.println(Pattern.matches("[ayz]?","a"));// true (a or y or z come one time)
		System.out.println(Pattern.matches("[ayz]?","aaa"));//false (a comes more than one time)
		System.out.println(Pattern.matches("[ayz]?","ayyyyzz")); //false (y and z comes more than one time)
		System.out.println(Pattern.matches("[ayz]?","amnta"));// false (a comes more than one time)
		System.out.println(Pattern.matches("[ayz]?","ayz"));//true (a, y and z come one time)
		System.out.println("+ Quantifier.....");
		System.out.println(Pattern.matches("[ayz]+","a"));// true (a comes one or more times)
		System.out.println(Pattern.matches("[ayz]+","aaa"));//true (a come one times)
		System.out.println(Pattern.matches("[ayz]+","ayyyyzz")); //true(a, y and z come one time)
		System.out.println(Pattern.matches("[ayz]+","aamnta"));// false (m and t are not matching patterns)
		System.out.println(Pattern.matches("[ayz]+","ay"));//false (x and y comes more than once)
		System.out.println("* Quantifier.....");
		System.out.println(Pattern.matches("[ayz]*","ayyza"));//false (a, y and z come zero or more times)
	}
}
```

**Regex Metacharacters**

The Metacharacter works as shortcuts with a special meaning

|	Metacharacter	|	Description	|
|	-------------------	|	-------------------	|
|	.	|	It can be any character|
|	d	|	represents any digit	|
|	D	|	represents any non digit|
|	s	|	represents any white space|
|	S	|	represents any non white space character|
|	w	|	can be a word character|
|	W	|	can be a word character|
|	b	|	represents a word boundary|
|	B	|	represents a non word boundary|

Eg:
```java
import java.util.regex.*;
public class MetacharExample{
	public static void main(String[] args){
		System.out.println("metacharacters d....."); // d means digit
		System.out.println(Pattern.matches("d","abc"));// false (non digit)
		System.out.println(Pattern.matches("d","1"));//true (digit)
		System.out.println(Pattern.matches("d","7855")); //false (digit but comes more than once)
		System.out.println(Pattern.matches("d","4754cvsch"));// false (digit and char)
		
		System.out.println("metacharacters D....."); // D means Non Digit
		System.out.println(Pattern.matches("D","124"));// false (digit)
		System.out.println(Pattern.matches("D","abc"));//false (non digit but comes more than once)
		System.out.println(Pattern.matches("D","444ada")); //false(digit and char)
		System.out.println(Pattern.matches("D","s"));// true (non-digit and come once)

		System.out.println("metacharacter D with Quantifier.....");
		System.out.println(Pattern.matches("D*","abc"));//true (non digit may come 0 or more time)
	}
}
```

### PatternSyntaxException Class <br /> 

 It is an unchecked exception that indicates a syntax error in a regular expression pattern.


