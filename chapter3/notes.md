# Chapter 3: Operators in Java

## Learning Objectives

In this chapter, you will learn:

* What are Operators?
* Arithmetic Operators
* Relational Operators
* Logical Operators
* Assignment Operators
* Real-world Examples
* Common Beginner Mistakes

---

# What is an Operator?

An **Operator** is a special symbol that performs an operation on one or more operands (values or variables).

Think of operators as the action performers in a program.

Example:

```java
int sum = 10 + 20;
```

Here:

```java
+
```

is an operator.

And:

```java
10 and 20
```

are operands.

---

# Why Do We Need Operators?

Suppose we want to:

* Add two numbers
* Compare two values
* Check multiple conditions
* Assign values to variables

Operators help us perform these tasks easily.

---

# Types of Operators

```text
Operators
│
├── Arithmetic
├── Relational
├── Logical
└── Assignment
```

---

# 1. Arithmetic Operators

Arithmetic operators are used to perform mathematical calculations.

| Operator | Meaning             |
| -------- | ------------------- |
| +        | Addition            |
| -        | Subtraction         |
| *        | Multiplication      |
| /        | Division            |
| %        | Modulus (Remainder) |

---

## Addition (+)

```java
int a = 10;
int b = 20;

System.out.println(a + b);
```

Output:

```text
30
```

---

## Subtraction (-)

```java
int a = 20;
int b = 10;

System.out.println(a - b);
```

Output:

```text
10
```

---

## Multiplication (*)

```java
int a = 5;
int b = 4;

System.out.println(a * b);
```

Output:

```text
20
```

---

## Division (/)

```java
int a = 20;
int b = 5;

System.out.println(a / b);
```

Output:

```text
4
```

---

### Important: Integer Division

```java
int a = 10;
int b = 3;

System.out.println(a / b);
```

Output:

```text
3
```

Why?

Because both operands are integers.

The decimal part gets discarded.

---

To get a decimal result:

```java
System.out.println(10.0 / 3);
```

Output:

```text
3.3333333333333335
```

---

## Modulus (%)

Returns the remainder after division.

```java
int a = 10;
int b = 3;

System.out.println(a % b);
```

Output:

```text
1
```

Because:

```text
10 ÷ 3 = 3 remainder 1
```

---

## Practical Example

Check whether a number is even or odd.

```java
int num = 8;

System.out.println(num % 2);
```

Output:

```text
0
```

If remainder is:

```text
0 → Even
1 → Odd
```

---

# 2. Relational Operators

Relational operators compare two values.

The result is always:

```java
true
or
false
```

---

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal To              |
| !=       | Not Equal To          |
| >        | Greater Than          |
| <        | Less Than             |
| >=       | Greater Than Equal To |
| <=       | Less Than Equal To    |

---

## Equal To (==)

```java
int a = 10;
int b = 10;

System.out.println(a == b);
```

Output:

```text
true
```

---

## Not Equal To (!=)

```java
System.out.println(10 != 5);
```

Output:

```text
true
```

---

## Greater Than (>)

```java
System.out.println(20 > 10);
```

Output:

```text
true
```

---

## Less Than (<)

```java
System.out.println(5 < 10);
```

Output:

```text
true
```

---

## Greater Than Equal To (>=)

```java
System.out.println(10 >= 10);
```

Output:

```text
true
```

---

## Less Than Equal To (<=)

```java
System.out.println(5 <= 10);
```

Output:

```text
true
```

---

## Real World Example

Age Verification

```java
int age = 20;

System.out.println(age >= 18);
```

Output:

```text
true
```

Meaning:

```text
Eligible to Vote
```

---

# 3. Logical Operators

Logical operators are used to combine multiple conditions.

Imagine:

```text
Condition 1
Condition 2
```

We want to check both together.

---

| Operator | Meaning     |   |            |
| -------- | ----------- | - | ---------- |
| &&       | Logical AND |   |            |
|          |             |   | Logical OR |
| !        | Logical NOT |   |            |

---

# Logical AND (&&)

Returns true only if both conditions are true.

```java
true && true
```

Output:

```text
true
```

---

Example:

```java
int age = 20;
boolean hasID = true;

System.out.println(age >= 18 && hasID);
```

Output:

```text
true
```

---

### Truth Table

| A     | B     | A && B |
| ----- | ----- | ------ |
| true  | true  | true   |
| true  | false | false  |
| false | true  | false  |
| false | false | false  |

---

# Logical OR (||)

Returns true if at least one condition is true.

Example:

```java
boolean hasPassport = false;
boolean hasAadhar = true;

System.out.println(hasPassport || hasAadhar);
```

Output:

```text
true
```

---

### Truth Table

| A     | B     | A || B |
| ----- | ----- | ------ |
| true  | true  | true   |
| true  | false | true   |
| false | true  | true   |
| false | false | false  |

---

# Logical NOT (!)

Reverses the result.

```java
boolean isLoggedIn = true;

System.out.println(!isLoggedIn);
```

Output:

```text
false
```

---

Example:

```java
boolean isStudent = false;

System.out.println(!isStudent);
```

Output:

```text
true
```

---

# Real World Example

Login System

```java
String username = "chai";
String password = "123";

boolean isValid =
        username.equals("chai")
        && password.equals("123");

System.out.println(isValid);
```

Output:

```text
true
```

---

# 4. Assignment Operators

Assignment operators are used to assign values to variables.

---

## Basic Assignment (=)

```java
int age = 21;
```

Here:

```java
=
```

assigns the value to the variable.

---

# Compound Assignment Operators

| Operator | Meaning             |
| -------- | ------------------- |
| +=       | Add and Assign      |
| -=       | Subtract and Assign |
| *=       | Multiply and Assign |
| /=       | Divide and Assign   |
| %=       | Modulus and Assign  |

---

## += Operator

```java
int x = 10;

x += 5;
```

Equivalent to:

```java
x = x + 5;
```

Output:

```text
15
```

---

## -= Operator

```java
int x = 10;

x -= 3;
```

Equivalent to:

```java
x = x - 3;
```

Output:

```text
7
```

---

## *= Operator

```java
int x = 10;

x *= 2;
```

Equivalent to:

```java
x = x * 2;
```

Output:

```text
20
```

---

## /= Operator

```java
int x = 20;

x /= 4;
```

Equivalent to:

```java
x = x / 4;
```

Output:

```text
5
```

---

## %= Operator

```java
int x = 10;

x %= 3;
```

Equivalent to:

```java
x = x % 3;
```

Output:

```text
1
```

---

# Complete Example

```java
public class OperatorsDemo {

    public static void main(String[] args) {

        int a = 10;
        int b = 5;

        System.out.println("Addition: " + (a + b));
        System.out.println("Subtraction: " + (a - b));
        System.out.println("Multiplication: " + (a * b));
        System.out.println("Division: " + (a / b));
        System.out.println("Modulus: " + (a % b));

        System.out.println(a > b);
        System.out.println(a == b);

        boolean result = a > b && b > 0;
        System.out.println(result);

        a += 10;
        System.out.println(a);

    }
}
```

Output:

```text
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
Modulus: 0
true
false
true
20
```

---

# Common Beginner Mistakes

## Using = instead of ==

Wrong:

```java
if(age = 18)
```

Correct:

```java
if(age == 18)
```

---

## Dividing Integers Expecting Decimal

```java
System.out.println(10 / 3);
```

Output:

```text
3
```

Not:

```text
3.33
```

---

## Confusing && and ||

```java
&& → Both conditions must be true

|| → At least one condition must be true
```

---

# Chapter Summary

* Operators perform actions on values and variables.
* Arithmetic operators perform mathematical calculations.
* Relational operators compare values and return boolean results.
* Logical operators combine multiple conditions.
* Assignment operators store and update values.
* Logical operators are heavily used in decision-making statements.

## Quick Revision

### Arithmetic

```java
+  -  *  /  %
```

### Relational

```java
==  !=  >  <  >=  <=
```

### Logical

```java
&&   ||   !
```

### Assignment

```java
=
+=
-=
*=
/=
%=
```

**Next Chapter: Input & Output in Java (System.out.print, println, printf, and Scanner Class).**
