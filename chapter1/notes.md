# Chapter 1: Setting Up Java & Your First Program

## Learning Objectives

By the end of this chapter, you will understand:

* Prerequisites for Java Development
* Installing Java
* Setting Up VS Code / IDE
* Writing Your First Java Program
* Compilation & Execution Process
* Understanding the `main()` Method
* Program Execution Flow

---

# Prerequisites to Work with Java

Before writing Java programs, we need a few tools.

## 1. Install JDK

Java programs require the **JDK (Java Development Kit)**.

The JDK contains:

* JVM
* JRE
* Java Compiler (`javac`)
* Debugging Tools
* Development Utilities

Without JDK, we cannot compile Java code.

---

## 2. Verify Installation

Open Terminal / Command Prompt and run:

```bash
java -version
```

Example Output:

```bash
java version "21"
```

Check compiler:

```bash
javac -version
```

Example:

```bash
javac 21
```

If both commands work, Java is installed successfully.

---

## 3. Install a Code Editor

You can use:

* VS Code
* IntelliJ IDEA
* Eclipse
* NetBeans

For beginners, VS Code is a great choice.

Useful Extensions:

* Extension Pack for Java
* Java Debugger
* Java Test Runner

---

# Creating Our First Java Program

Create a file:

```text
HelloWorld.java
```

Write the following code:

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }

}
```

---

# Understanding File Name & Class Name

Notice:

```java
public class HelloWorld
```

The class name is:

```java
HelloWorld
```

Therefore the file name must be:

```text
HelloWorld.java
```

Rule:

> If a class is public, the file name must match the class name.

Correct:

```text
HelloWorld.java
```

```java
public class HelloWorld
```

Wrong:

```text
Main.java
```

```java
public class HelloWorld
```

This will cause a compilation error.

---

# Compiling the Program

Java source files cannot execute directly.

They must first be compiled.

```bash
javac HelloWorld.java
```

Output:

```text
HelloWorld.class
```

The `.class` file contains Bytecode.

---

# Running the Program

Execute the class using JVM:

```bash
java HelloWorld
```

Output:

```text
Hello World
```

Notice:

```bash
java HelloWorld
```

NOT

```bash
java HelloWorld.class
```

Java expects the class name, not the file name.

---

# Program Execution Flow

```text
HelloWorld.java
        ↓
      javac
        ↓
HelloWorld.class
     (Bytecode)
        ↓
        JVM
        ↓
 Machine Code
        ↓
    Output
```

---

# Breaking Down the Program

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }

}
```

Let's understand each piece.

---

## public class HelloWorld

```java
public class HelloWorld
```

### public

Means the class can be accessed from anywhere.

### class

A blueprint for creating objects.

### HelloWorld

The name of the class.

---

# The main() Method

```java
public static void main(String[] args)
```

This is the most important line in every beginner Java program.

The JVM starts execution from this method.

Think of it as:

> The entry point of the program.

Without a valid `main()` method, JVM doesn't know where to start execution.

---

# How JVM Finds main()

When you run:

```bash
java HelloWorld
```

JVM:

1. Loads the class
2. Searches for `main()`
3. Starts execution from there

```text
JVM
 ↓
Load Class
 ↓
Find main()
 ↓
Execute Statements
```

---

# Understanding Each Keyword

## 1. public

```java
public static void main(String[] args)
```

Means:

> JVM should be able to access this method from outside the class.

If it is not public, JVM cannot call it.

---

## 2. static

```java
static
```

Normally methods belong to objects.

But JVM needs to execute `main()` before creating any object.

Because of `static`, JVM can call it directly using the class name.

Without creating an object.

Example:

```java
ClassName.methodName();
```

---

## 3. void

```java
void
```

Means:

> This method does not return anything.

Unlike:

```java
int add()
```

which returns an integer value.

`main()` simply starts program execution.

---

## 4. main

```java
main
```

Special method name recognized by the JVM.

The JVM specifically looks for a method called:

```java
main
```

No other name works.

Wrong:

```java
start()
```

```java
run()
```

JVM will not recognize them.

---

## 5. String[] args

```java
String[] args
```

Used for Command Line Arguments.

It is an array of strings.

Example:

```bash
java HelloWorld ChaiCode Java
```

Values received:

```java
args[0] = "ChaiCode"
args[1] = "Java"
```

Program:

```java
public class HelloWorld {

    public static void main(String[] args) {

        System.out.println(args[0]);
        System.out.println(args[1]);

    }
}
```

Output:

```text
ChaiCode
Java
```

---

# Visualizing main()

```java
public static void main(String[] args)
```

Read it as:

> A public method named `main`, belonging to the class itself (`static`), returning nothing (`void`), and accepting an array of strings (`String[] args`).

---

# Execution Example

```java
public class HelloWorld {

    public static void main(String[] args) {

        System.out.println("Step 1");
        System.out.println("Step 2");
        System.out.println("Step 3");

    }

}
```

Output:

```text
Step 1
Step 2
Step 3
```

Execution occurs from top to bottom.

---

# Common Beginner Mistakes

### Forgetting Semicolon

Wrong:

```java
System.out.println("Hello")
```

Correct:

```java
System.out.println("Hello");
```

---

### Wrong File Name

Wrong:

```text
Main.java
```

```java
public class HelloWorld
```

---

### Missing Curly Braces

Wrong:

```java
public class HelloWorld
    public static void main(String[] args)
```

Always use:

```java
{
}
```

for classes and methods.

---

### Wrong Main Signature

Wrong:

```java
public void main(String[] args)
```

Correct:

```java
public static void main(String[] args)
```

---

# Chapter Summary

* JDK is required to develop Java applications.
* Java source files have a `.java` extension.
* Java code is compiled using `javac`.
* Compilation generates Bytecode (`.class` file).
* JVM executes the Bytecode.
* The program starts from the `main()` method.
* `public static void main(String[] args)` is the standard entry point of a Java application.
* `String[] args` is used for command-line arguments.

## Quick Revision

```text
Write Code (.java)
        ↓
Compile (javac)
        ↓
Bytecode (.class)
        ↓
JVM
        ↓
Execution
```

```java
public static void main(String[] args)
```

* public → Accessible by JVM
* static → No object required
* void → Returns nothing
* main → Entry point
* String[] args → Command-line arguments

**In the next chapter, we'll learn about Java Syntax, Variables, Data Types, and Naming Conventions.**
