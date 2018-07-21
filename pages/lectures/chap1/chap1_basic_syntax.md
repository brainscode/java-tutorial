---
title: Methods In Java
toc: false
sidebar: labs_sidebar
folder: lectures/chap1
permalink: /chap1_methods.html
summary: A Java method is a collection of statements that are grouped together to perform an operation.<br/> When you call the <b>System.out.println()</b> method, for example, the system actually executes several statements in order to display a message on the console.
applies_to: [lecture]
---

Lets consider a Java program, it can consist of a class, methods and other data members.

### Class

A class can be defined as a template or blueprint that describes the behavior and state of an object. It can contain variables, operations, methods and other properties for an object.

**Syntax:**

{% include code.html lang="java" 
content="class NameofClass {
// class body
}" %}

### Methods

1.  Methods define actions that a class's objects (or instances) can do.
1.  A method has a declaration part and a body.
1.  The declaration part consists of a return value, the method name, and a list of arguments.
1.  The body contains code that perform the action.
1.  The return type of a method can be a primitive, an object, or void.
1.  The return type void means that the method returns nothing.
1.  The declaration part of a method is also called the signature of the method.

**Syntax:**

{% include code.html lang="java" 
content="accessModifier returnType nameOfMethod (params or args) {
 	// method body
}" %}


**accessModifier** − It defines the access type of the method and it is optional to use.

**returnType** − Method may return a value.

**nameOfMethod** − This is the method name. The method signature consists of the method name and the parameter list.

**params or args** − The input parameters, the number of declared variables for a method. Method may contain no parameters.

**method body** − The method body contains the list of statements which has to be execute.

### Calling of a Method

{% include code.html lang="java" content="methodname(args); //calling method with args
methodname(); //calling method which have no args
" %}

## Recursion in Java

Recursion in Java is a process in which a method calls itself continuously. A method in Java that calls itself is called recursive method.

It makes the code compact but complex to understand or if any condition include in method gone wrong, it will stuck in a continuous recursion.

{% include code.html lang="java" content="returntype methodname(){
  methodcode	//code to be executed
  methodname(); //calling same method
} " %}


{% include tip.html  content="It is better not to recall a method when there is no need." %}


## Continue

In this section, you learn what is method and calling of a method, later you will learn the types of methods and how to call by value or reference.

Proceed to [Chap 1 - Java Variables & Primitive Data Types](chap1_variables.html).
