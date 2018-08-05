---
title: Variables & Primitive Data Types
toc: false
sidebar: labs_sidebar
folder: lectures/chap1
permalink: /chap1_variables.html
summary: Data types represent the different values to be stored in the variable.
applies_to: [lecture]
---

## What is Data Type ?

1.  Data types classify the different values to be stored in the variable.

    In **Java**, there are two types of data types:

+ Primitive Data Types
+ Non-primitive Data Types
	
    ![](./images/lectures/chap1/datatypes.png)


###  Primitive Data Types

Primitive Data Types are predefined and available within the Java language. Primitive values do not share state with other primitive values.

There are 8 primitive types: **byte**, **short**, **int**, **long**, **char**, **float**, **double** and **boolean**.

{% include tip.html content="1 byte = 8 bit" %}

-   Integer Data Type

    > byte: `1 byte`
    > 
    > short: `2 bytes`
    > 
    > int: `4 bytes`
    > 
    > long: `8 bytes`

{% include important.html content="All numeric data types are signed it can represent both positive and negative numbers, where unsigned can only represent non-negative numbers (zero or positive numbers).
" %}

-   Floating Data Type

    > float: `4 bytes`
    > 
    > double: `8 bytes`

-   Text Data Type

    > char: `2 bytes`

{% include note.html content="The char data type in Java is 2 bytes because it uses **UNICODE** character set.<br/>**UNICODE** is a character set which covers all known scripts and language in the world.
" %}

-   Logical Data Type

    > boolean: `1 byte (true/false)`

{% include tip.html content="The size of data type remains the same on all platforms (standardized).
" %}

## What is a Variable ?

**Variable** is name of reserved area allocated in memory. In other words, It is a name of memory location. It is a combination of `vary + able` that means its value can be changed.

A variable can be thought of as a container which holds value for you during the life of your program. Every variable is assigned a data type which designates the type and quantity of a value it can hold.

![](./images/lectures/chap1/variable.png)

### Types of Variable

![](./images/lectures/chap1/variable_types.png)

1. **Local Variable**
A variable which is declared inside the method is called local variable.

1. **Instance Variable**
A variable which is declared inside the class but outside the method, is called instance variable . It is not declared as static.

1. **Class/Static variable**
A variable that is declared as static is called static variable. It cannot be local.

**Example:**

{% include code.html lang="java" content="class A{
 int data=50;       //instance variable
 static int m=100;  //static variable
 void method(){
 int n=90;          //local variable
 }
}//end of class" %}

### Variable Declaration & Initialization

**1) Variable Declaration:** To declare a variable, you must specify the data type & give the variable a unique name.

1. int a,b,c; 
1. float pi;
1. double d;
1. char a;

![](./images/lectures/chap1/declare_var.png)

**2) Variable Initialization:** To initialize a variable you must assign it a valid value.

1. pi = 3.14f;
1. d = 20.22d;
1. a = 'v';

![](./images/lectures/chap1/initialize_var.png)

**3) Variable Initialization and Declaration:** To declare and initialize a variable in same line.

1. int a = 10; 
1. float pi = 1.1;
1. double d = 10.01;
1. char a = 'j';

### Local Variables

+ Local variables are declared in methods, constructors, or blocks (instance initializer block).
+ Local variables are created when the method, constructor or block is entered and the variable will be destroyed once it exits the method, constructor, or block.
+ Access modifiers cannot be used for local variables.
+ Local variables are implemented at stack level internally.
+ There is no default value for local variables, so local variables should be declared and an initial value should be assigned before the first use.

{% include tip.html content="The constructor is a special type of method which is used to initialize the object and Instance Initializer block is used to initialize the instance data member." %}

{% include note.html content="We will learn constructor and instance initializer block in the next lectures.
" %}

### Instance Variables

+ Instance variables are declared in a class, but outside a method, constructor or blocks.
+ When a space is allocated for an object in the heap, a slot for each instance variable value is created.
+ Instance variables are created when an object is created with the use of the keyword `new` and destroyed when the object is destroyed.
+ Instance variables hold values that must be referenced by more than one method, constructor or block, or essential parts of an object's state that must be present throughout the class.
+ Access modifiers can be given for instance variables.
+ The instance variables are visible for all methods, constructors and block in the class. Normally, it is recommended to make these variables private (access level). However, visibility for subclasses can be given for these variables with the use of access modifiers.
+ Instance variables have default values. 
   1. **For Numbers:** The default value is 0, 
   2. **For Boolean:** It is false as default, and for object references it is null. 

	Values can be assigned during the declaration or within the constructor.
+ Instance variables can be accessed directly by calling the variable name inside the class. However, within static methods (when instance variables are given accessibility), they should be called using the fully qualified name. `ObjectReference.VariableName`.

### Class/Static Variables

+ Class variables also known as static variables are declared with the static keyword in a class, but outside a method, constructor or a block.
+ It is a variable which belongs to the class and not to object(instance).
+ Static variables are initialized only once , at the start of the execution . These variables will be initialized first, before the initialization of any instance variables
+ A single copy to be shared by all instances of the class, regardless of how many objects are created from it.
+ A static variable can be accessed directly by the class name and doesn’t need any object
+ Static variables are rarely used other than being declared as constants. Constants are variables that are declared as public/private, final, and static. Constant variables never change from their initial value.
+ Static variables are created when the program starts and destroyed when the program stops.
+ Visibility is similar to instance variables. However, most static variables are declared public since they must be available for users of the class.
+ Default values are same as instance variables. For numbers, the default value is 0; for Booleans, it is false; and for object references, it is null. 
+ Values can be assigned during the declaration or within the constructor. Additionally, values can be assigned in special static initializer blocks.
+ Static variables can be accessed by calling with the class name ClassName.VariableName.
+ The static variable can be used to refer the common property of all objects (that is not unique for each object) e.g. company name of employees,college name of students etc.
+ The static variable gets memory only once in class area at the time of class loading.
+ When declaring class variables as public static final, then variable names (constants) are all in uppercase. If the static variables are not public and final, the naming syntax is the same as instance and local variables.

## Advantage of static variable

It makes your program memory efficient (i.e it saves memory).

**Understanding problem without static variable**

![](./images/lectures/chap1/static_var.png)

{% include note.html content="What is Stack and Heap ? <br/> This is the memory areas manage by Java, we will discuss in detail in other chapter." %}

{% include code.html lang="java" content="class Student{ 
     int rollno; 
     String name; 
     String college=\"FUUAST\";
}" %}

Suppose there are 500 students in the college, now all instance data members will get memory each time when object is created. All student have its unique rollno with name so instance data member is good. But, when college refers to the common property for all objects. so we make it static, this will make space in memory only once.

## Java Variable Type Conversion & Type Casting

A variable of one type can receive the value of another type.

Here, there are 2 cases -

**case 1)** Variable of smaller capacity is be assigned to another variable of bigger capacity.

**Example:**

{% include code.html lang="java" content="double d;   // declare var 
int i = 10; // declare diff datatype var
d = i;	// assign val of i into d implicitly
" %}

This process is Automatic, and non-explicit is known as auto Conversion.

**case 2)** Variable of larger capacity is be assigned to another variable of smaller capacity.

![](./images/lectures/chap1/typecast.png)

In such cases you have to explicitly specify the type cast operator.

This process is known as **Type Casting**.

In case, you do not specify a type cast operator, the compiler gives an error. Since this rule is enforced by the compiler, it makes the programmer aware that the conversion he is about to do may cause some loss in data and prevents accidental losses.


## Continue

Now you know the basic fundamentals of programming in Java Syntax. In the next lesson, you will learn the precedence of programming operators and what they do.

Proceed to [Chap 1 - Java Operators](chap1_operators.html).
