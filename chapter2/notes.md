# Chapter 2: Variables, Data Types & Identifiers

## Learning Objectives

In this chapter, you will learn:

* What is a Variable?
* Variable Analogy
* What is an Identifier?
* What is a Data Type?
* Java Variable Syntax
* What is a Statically Typed Language?
* Primitive Data Types
* Non-Primitive Data Types
* Literals
* Declaration vs Definition (Initialization)
* Keywords in Java

---

# What is a Variable?

A variable is a named memory location used to store data.

Think of a variable as a container that holds some value which can be used later in the program.

Example:

```java
int age = 21;
```

Here:

* `age` → Variable Name
* `21` → Value stored inside the variable

---

# Variable Analogy

Imagine you have labeled boxes in your room.

```text
┌─────────────┐
│ Age Box     │
│     21      │
└─────────────┘
```

The label on the box is the variable name.

The item inside the box is the value.

Example:

```java
String name = "Suraj";
int age = 22;
double salary = 500000.50;
```

```text
Name Box   → Suraj
Age Box    → 22
Salary Box → 500000.50
```

Variables help us store and reuse information throughout the program.

---

# What is an Identifier?

An Identifier is the name given to:

* Variables
* Classes
* Methods
* Packages
* Interfaces

Example:

```java
int age = 21;
```

`age` is an identifier.

```java
class Student {
}
```

`Student` is an identifier.

```java
void display() {
}
```

`display` is an identifier.

---

# Rules for Naming Identifiers

### Valid

```java
int age;
int marks;
int studentAge;
int _count;
int $price;
```

### Invalid

```java
int 123age;
int student-name;
int class;
```

Reasons:

* Cannot start with a number.
* Cannot contain special characters like `-`.
* Cannot use reserved keywords.

---

# Naming Conventions

### Variables

Use camelCase

```java
int studentAge;
double accountBalance;
```

---

### Classes

Use PascalCase

```java
class StudentDetails {
}
```

---

### Constants

Use UPPER_CASE

```java
final double PI = 3.14159;
```

---

# What is a Data Type?

A Data Type tells Java:

1. What kind of data is being stored.
2. How much memory is required.
3. What operations can be performed.

Example:

```java
int age = 21;
```

Here:

* `int` tells Java that age stores an integer.

---

# Why Do We Need Data Types?

Imagine storing:

```text
21
95.5
'A'
true
```

All these values are different.

Java needs to know:

* Is it a number?
* Is it a decimal?
* Is it a character?
* Is it true/false?

That's why data types exist.

---

# Syntax of Creating a Variable

General Syntax:

```java
datatype variableName = value;
```

Example:

```java
int age = 21;
String name = "Suraj";
double price = 99.99;
```

---

# What is a Statically Typed Language?

Java is a Statically Typed Language.

This means:

> The data type of a variable must be declared before compilation.

Example:

```java
int age = 21;
```

Java already knows that `age` is an integer.

---

### Correct

```java
int age = 21;
```

---

### Wrong

```java
int age = "Suraj";
```

Error because:

```text
Expected → Integer
Given    → String
```

---

# Data Types in Java

Java Data Types are divided into two categories:

```text
Data Types
│
├── Primitive
│
└── Non Primitive
```

---

# Primitive Data Types

Primitive types are built into Java.

They store actual values.

There are 8 Primitive Data Types.

---

## Integer Types

Used for whole numbers.

### byte

Size: 1 Byte

Range:

```text
-128 to 127
```

Example:

```java
byte age = 25;
```

---

### short

Size: 2 Bytes

Example:

```java
short population = 30000;
```

---

### int

Size: 4 Bytes

Most commonly used integer type.

Example:

```java
int marks = 95;
```

---

### long

Size: 8 Bytes

Used for very large numbers.

Example:

```java
long worldPopulation = 8000000000L;
```

Notice:

```java
L
```

at the end.

---

# Real Number Types

Used for decimal values.

---

## float

Size: 4 Bytes

Example:

```java
float price = 99.99f;
```

Notice:

```java
f
```

must be added.

---

## double

Size: 8 Bytes

More precise than float.

Example:

```java
double salary = 500000.75;
```

---

# Character Type

Stores a single character.

### char

Size: 2 Bytes

Example:

```java
char grade = 'A';
```

Use single quotes.

```java
'A'
```

Correct

```java
"A"
```

Wrong (String)

---

# Boolean Type

Stores only:

```text
true
false
```

Example:

```java
boolean isLoggedIn = true;
boolean isAdmin = false;
```

---

# Primitive Data Types Summary

| Type    | Example     |
| ------- | ----------- |
| byte    | 100         |
| short   | 2000        |
| int     | 500000       |
| long    | 9000000000L |
| float   | 99.99f      |
| double  | 99.99       |
| char    | 'A'         |
| boolean | true        |

---

# Non-Primitive Data Types

These are created using classes.

Examples:

```java
String name = "Suraj";
```

```java
int[] marks = {10, 20, 30};
```

```java
Student student = new Student();
```

Common Non-Primitive Types:

* String
* Arrays
* Classes
* Interfaces
* Enums

---

# What are Literals?

A Literal is the actual value written in code.

Example:

```java
int age = 21;
```

`21` is a literal.

---

## Integer Literal

```java
int age = 21;
```

---

## Floating Literal

```java
double price = 99.99;
```

---

## Character Literal

```java
char grade = 'A';
```

---

## String Literal

```java
String name = "Suraj";
```

---

## Boolean Literal

```java
boolean isActive = true;
```

---

# Declaration vs Initialization

Many beginners confuse these concepts.

---

## Declaration

Creating a variable.

```java
int age;
```

Here:

* Variable is created.
* No value assigned.

---

## Initialization

Assigning a value.

```java
age = 21;
```

---

## Declaration + Initialization

```java
int age = 21;
```

This is the most common form.

---

# Visual Representation

```java
int age;
```

```text
Memory Created
Value Not Assigned
```

---

```java
age = 21;
```

```text
Memory Created
Value Assigned
```

---

# Keywords in Java

Keywords are reserved words that have predefined meanings in Java.

You cannot use them as identifiers.

Example:

```java
int class = 10;
```

Invalid because:

```java
class
```

is a keyword.

---

# Commonly Used Keywords

```java
class
public
private
protected
static
void
new
return
if
else
switch
case
break
continue
for
while
do
try
catch
finally
throw
throws
this
super
final
abstract
interface
extends
implements
package
import
enum
instanceof
```

Java has around **68 reserved and contextual keywords** in modern versions, though beginners usually work with only a small subset initially.

---

# Complete Example

```java
public class Student {

    public static void main(String[] args) {

        String name = "Rohit";
        int age = 21;
        double marks = 95.5;
        char grade = 'A';
        boolean isPlaced = true;

        System.out.println(name);
        System.out.println(age);
        System.out.println(marks);
        System.out.println(grade);
        System.out.println(isPlaced);

    }

}
```

### Output

```text
Rohit
21
95.5
A
true
```

---

# Chapter Summary

* Variables are named memory locations used to store data.
* Identifiers are names given to variables, classes, methods, etc.
* Data Types tell Java what kind of value is being stored.
* Java is a statically typed language.
* Primitive types store actual values.
* Non-Primitive types store references to objects.
* Literals are fixed values written directly in code.
* Declaration creates a variable.
* Initialization assigns a value.
* Keywords are reserved words that cannot be used as identifiers.

## Quick Revision

```java
int age = 21;
```

* `int` → Data Type
* `age` → Identifier
* `=` → Assignment Operator
* `21` → Literal

```text
Variable = Named Container
Identifier = Name
Datatype = Type of Data
Literal = Actual Value
Keyword = Reserved Word
```

**Next Chapter: Operators in Java (Arithmetic, Relational, Logical, Assignment, Unary, and Ternary Operators).**
