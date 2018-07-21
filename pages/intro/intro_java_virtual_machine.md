---
title: Java Virtual Machine
toc: false
sidebar: labs_sidebar
folder: intro
permalink: /intro_java_virtual_machine.html
summary: We must understand the differences between JDK, JRE and JVM before proceeding further to Java.
applies_to: [lecture]
---

## What is JVM?
JVM (Java Virtual Machine) is an abstract machine. It is a engine that provides runtime environment in which Java bytecode can be executed.

JVMs are available for many hardware and software platforms. JVM, JRE and JDK are platform dependent (need to be install in OS separately) because configuration of all Operating Systems are different. But, Java bytecode is platform independent.

The JVM performs following main tasks:
-	Loads code
-	Verify code
-	Executes code
-	Provides runtime environment

## JRE
JRE is an acronym for Java runtime environment, implementation of JVM, contains set of libraries + other files that JVM uses at runtime.

![](./images/lectures/jre.png)

## JDK
JDK is an acronym for Java Development Kit, contains JRE + development tools.

![](./images/lectures/jdk.png)

---

## JVM Architecture

Let's understand the Architecture of JVM. It contains classloader, memory area, execution engine etc.

![](./images/lectures/jvm.png)


**1) Class Loader** is a subsystem used for loading class files. It performs three major functions viz. Loading, Linking, and Initialization. 

**2) Class/Method Area** stores per-class structures like metadata such as the constant runtime pool, field and method data, the code for methods.

**3) Heap** is the runtime data area in which objects are allocated and their related instance variables, and arrays are stored. This memory is common and shared across multiple threads.

**4) Stack** stores frames It holds local variables and it's partial results. Each thread has a private JVM stack, created at the same time as thread is created. A new frame is created whenever a method is invoked, and it is destroyed when method invocation process is complete.

**5) PC (program counter) Register** contains the address of the Java virtual machine instruction which is currently executing. In Java, each thread has its separate PC register.

**6) Native Method Stack** hold the instruction of native code depends on the native library. It is written in another language instead of Java e.g. assembly, C++.

**7) Execution Engine** is a type of software used to test hardware, software, or complete systems. The test execution engine never carries any information about the tested product.

 - It contains:

   - A virtual processor.

   - Interpreter which read bytecode streaming then execute the instructions.

   - Just-In-Time (JIT) compiler which is used to improve the performance.

{% include note.html content="
        Here the term compiler refers to a translator from the instruction set of a Java virtual machine (JVM) to the instruction set of a specific CPU.
"%}

**8) Native Method Interface** is a programming framework. It allows Java code which is running in a JVM to call by libraries and native applications.

**9) Native Method Libraries** is a collection of the Native Libraries (C, C++) which are needed by the Execution Engine. 

---

## How Does JVM Work?

### Lets Consider C Program Execution.

Suppose in the main, you have called two function f1 and f2. The main function is stored in a1.c file, function f1 is stored in a2.c file, function f2 is stored in a3.c file. All these files, i.e. a1.c, a2.c, and a3.c, is fed to the compiler. Whose output is the corresponding object files which are the machine code.

![](./images/lectures/jvm01.jpg)

The next step is integrating all these object files into a single .exe (executable) file with the help of linker. The linker will club all these files together and produces the .exe file.

![](./images/lectures/jvm02.jpg)

### Now Java code Compilation and Execution in Java VM

Let's look at the process for JAVA. In your main, you have two methods f1 and f2.

-    The main method is stored in file a1.java
-    f1 is stored in a file as a2.java
-    f2 is stored in a file as a3.java

![](./images/lectures/jvm03.jpg)

The compiler will compile the three files and produces 3 corresponding .class file which consists of BYTE code. Unlike C, no linking is done.

The Java Virtual Machine resides on the RAM. During execution, using the class loader the class files are brought on the RAM. The BYTE code is verified for any security breaches.

Next, the execution engine will convert the Bytecode into Native machine code. This is just in time compiling. It is one of the main reason why Java is comparatively slow. 

![](./images/lectures/jvm04.jpg)

{% include note.html content="
         JIT interprets part of the byte code that have similar functionality at the same time, and hence reduces the amount of time needed for compilation.
"%}

### Java is both interpreted and compiled language

Programming languages are classified as

-    High Level Languages e.g. C++, Java.
-    Middle Level Languages e.g. C.
-    Low Level Languages e.g. Assembly.
-    finally the lowest level as the Machine/Binary Language.

A **compiler** is a program that converts instructions into a machine-code or lower-level form so that they can be read and executed by a computer.

The Java compiler converts high-level (Human Readable) Java code into bytecode (which is also a type of machine code).

An **interpreter** is a program which converts a program at one level to another programming language at the same level. Example conversion of Java bytecode into Binary code.

In Java, the Just In Time Code generator converts the bytecode into the native machine code which are at the same programming level.

Hence, Java is both compiled as well as interpreted language.


### In comparison to other compiler machines, Java may be slow

The two main reasons behind the slowness of Java are

- Dynamic Linking = Not like C Language, linking is done at runtime, at the execution time of program in Java.

- Runtime Interpreter = The conversion of bytecode into native machine code is done at runtime in Java which furthers slows down the speed 

However, the latest version of Java have addressed the performance bottlenecks to a great extent.


## Continue

Proceed to [Java Environment Setup](env_setup_overview.html).
