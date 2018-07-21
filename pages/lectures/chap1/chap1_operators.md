---
title: Operators in Java
toc: false
sidebar: labs_sidebar
folder: lectures/chap1
permalink: /chap1_operators.html
summary: |-
    Java provides a rich set of operators to manipulate variables. We can divide Java operators into the groups.
    <br/><br/>
    In this section, you will learn how to use operators and the rules of precedence. 
applies_to: [lecture]
---

## Operators in Java

**Operators** are mainly symbols that is used to perform operations between two or more operands. 

**e.g:** `+ - * /`

We can divide Java operators into the following groups.

+    Arithmetic Operators
+    Relational Operators
+    Bitwise Operators
+    Logical Operators
+    Assignment Operators
+    Misc Operators

## The Arithmetic Operators

Arithmetic operators are used in mathematical expressions in the same way that they are used in algebra. The following table lists the arithmetic operators

![](./images/lectures/chap1/arithmetic.png)

## The Relational Operators

![](./images/lectures/chap1/relational.png)

## The Bitwise Operators

**Bitwise Operators** which can be applied to the integer types, long, int, short, char, and byte.

Bitwise operator works on bits and performs bit-by-bit operation. 

Assume if `a = 60` and `b = 13` now in binary format they will be as follows

   > **a** = 0011 1100
   >
   > **b** = 0000 1101

   > `a&b = 0000 1100`
   >
   > `a|b = 0011 1101`
   >
   > `a^b = 0011 0001`
   >
   > `~a  = 1100 0011`

![](./images/lectures/chap1/bitwise.png)

## The Logical Operators

![](./images/lectures/chap1/logical.png)

## The Assignment Operators

![](./images/lectures/chap1/assignment.png)

## The Misc Operators

There are few other operators supported by Java Language.

### Conditional Operator ( ? : )

Conditional operator is also known as the **ternary operator**. This operator consists of three operands and is used to evaluate Boolean expressions. 

The goal of the operator is to decide, which value should be assigned to the variable. The operator is written as −

{% include code.html lang="java" content="variable x = (expression) ? value if true : value if false" %}

## Continue

Proceed to [Chap 1 - What is Method ?](chap1_methods.html).
