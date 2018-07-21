---
title: Java Comments
toc: false
sidebar: labs_sidebar
folder: labs/lab1
permalink: /lab1_java_comments.html
summary: How to put comments in your code to make it rememberable, describable and understandable.
applies_to: [lab]
---

## Simple Comment Program


- Launch the Notepad or any other Text Editor and paste the following code:

    ```java
   public class Comment {
   /* This is my first java program.
    * This will print 'Hello World' as the output
    * This is an example of multi-line comments.
    */

   public static void main(String []args) {
   // This is an example of single line comment
   /* This is also an example of single line comment. */
    System.out.println("Hello World");
    }
   }
    ```

- Save this file as Comment.java

Open a terminal and run the following command:

{% include code.html content="-- Windows
 javac C:\work\Comment.java

 -- Linux
 javac $HOME/work/Comment.java
" %}

It will produce .class file in work directory now execute the program

{% include code.html content="-- Windows
 java -cp C:\work\ Comment

 -- Linux
 java -cp $HOME/work/ Comment
" %}

**Output**
Hello World

## Java Documentation Comment

The documentation comment is used to create documentation API. To create documentation API, you need to use javadoc tool.

**Syntax:**

{% include code.html content="/** This is 
  documentation 
  comment
*/
" %}

- **Example:**

    ```java
	/** This class provides methods to get addition and subtraction of given 2 numbers.*/
	public class Calculator {
	/** The add() method returns addition of given numbers.*/
	public static int add(int a, int b){return a+b;}
	/** The sub() method returns subtraction of given numbers.*/
	public static int sub(int a, int b){return a-b;}
	}
    ```

1. Compile it by javac tool:   `javac Calculator.java`
1. Create Documentation API by javadoc tool:   `javadoc Calculator.java`

Now, there will be HTML files created for your Calculator class in the current directory. Open the HTML files and see the explanation of Calculator class provided through documentation comment.


## Continue

Proceed to [Chap 1 - Programming Basics](chap1_overview.html).

