# Chapter 0: Introduction to Java

## What is Java?

Java is a high-level, object-oriented, platform-independent programming language developed by **James Gosling** in 1995.

Java follows the principle:

> **WORA (Write Once, Run Anywhere)**

This means Java code can run on any operating system that has a JVM installed.

---

# Why Java?

### 1. Portability

Java programs are compiled into **Bytecode**, which can run on any platform having a JVM.

```java
Windows ✅
Linux ✅
macOS ✅
```

Write code once and run it anywhere.

---

### 2. Simple

Java removes many complex features from C/C++ such as:

* Pointer arithmetic
* Multiple inheritance through classes
* Manual memory management

This makes Java easier to learn and maintain.

---

### 3. Secure

Java provides security through:

#### PSS Properties

**P → Platform Independent**

* Code runs on different operating systems.

**S → Secure**

* No direct memory access through pointers.
* Bytecode verification.
* Sandbox execution model.

**S → Stable**

* Automatic Garbage Collection.
* Strong type checking.
* Exception handling.

---

# Introduction to Bytecode

When Java code is compiled, it is not converted directly into machine code.

Instead:

```text
Source Code (.java)
        ↓
     Compiler
      (javac)
        ↓
 Bytecode (.class)
```

Example:

```text
Hello.java
    ↓
javac Hello.java
    ↓
Hello.class
```

The generated `.class` file contains **Bytecode**.

---

# JVM Architecture

```text
Hello.java
     ↓
  Compiler
   (javac)
     ↓
Hello.class
(Bytecode)
     ↓
     JVM
     ↓
Machine Code
     ↓
 Execution
```

---

# JVM (Java Virtual Machine)

The JVM is responsible for executing Java programs.

### Responsibilities of JVM

#### 1. Bytecode Execution

Converts Bytecode into Machine Code.

---

#### 2. Security

Uses a **Sandbox Model** to safely execute code.

Features:

* Bytecode Verification
* Class Loader Security
* Runtime Checks

---

#### 3. Garbage Collection (GC)

Automatically removes unused objects from memory.

Benefits:

* Prevents memory leaks
* No manual memory management

---

#### 4. Performance Optimization

Uses:

* Interpreter
* JIT Compiler

---

# JIT Compiler (Just-In-Time Compiler)

Initially JVM interprets bytecode line by line.

Frequently executed code is identified as **Hot Code**.

The JIT Compiler converts hot code into native machine code for faster execution.

```text
Bytecode
    ↓
Interpreter
    ↓
Frequently Used Code
    ↓
JIT Compiler
    ↓
Machine Code
```

### Benefits

* Faster execution
* Better performance
* Runtime optimization

---

# JDK, JRE, and JVM

## JDK (Java Development Kit)

Used for developing Java applications.

```text
JDK
 ├── JRE
 ├── Compiler (javac)
 ├── Debugger
 ├── Java Docs
 └── Development Tools
```

### Used By:

Developers

---

## JRE (Java Runtime Environment)

Used to run Java applications.

```text
JRE
 ├── JVM
 └── Class Libraries
```

### Used By:

End Users

---

## JVM (Java Virtual Machine)

Executes Java Bytecode.

```text
JVM
 ├── Class Loader
 ├── Memory Areas
 ├── Garbage Collector
 └── Execution Engine
```

### Used By:

JRE

---

# Relationship

```text
JDK
 └── JRE
      └── JVM
```

Or

```text
JDK = JRE + Development Tools

JRE = JVM + Libraries
```

---

# First Java Program

```java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

### Output

```text
Hello World
```

---

# How Java Program Executes

```text
1. Write Code
   HelloWorld.java

2. Compile
   javac HelloWorld.java

3. Generate Bytecode
   HelloWorld.class

4. JVM Loads Bytecode

5. Interpreter + JIT Compiler

6. Machine Code Generated

7. Program Executes
```

---

# Java Editions

## 1. JSE (Java Standard Edition)

Used for:

* Core Java
* Desktop Applications
* Utilities

Examples:

* Collections Framework
* Multithreading
* JDBC

---

## 2. JEE (Java Enterprise Edition)

Used for:

* Enterprise Applications
* Web Applications
* Distributed Systems

Examples:

* Servlets
* JSP
* Enterprise APIs

---

## 3. JME (Java Micro Edition)

Used for:

* Embedded Devices
* IoT Devices
* Mobile Devices (older generation)

Examples:

* Smart Cards
* Set-top Boxes

---

# Quick Revision

### WORA

```text
Write Once Run Anywhere
```

### Compilation Flow

```text
.java
  ↓
javac
  ↓
.class
  ↓
JVM
  ↓
Machine Code
```

### Components

```text
JDK = JRE + Development Tools

JRE = JVM + Libraries
```

### JVM Responsibilities

* Execute Bytecode
* Security
* Garbage Collection
* JIT Compilation

### Java Editions

* JSE → Standard Applications
* JEE → Enterprise Applications
* JME → Embedded Systems

---

## Chapter 0 Summary

Java is a platform-independent, secure, and object-oriented language that achieves portability through **Bytecode** and the **JVM**. The **JDK** is used to develop applications, the **JRE** is used to run them, and the **JVM** executes Bytecode using an Interpreter and **JIT Compiler** while providing security and garbage collection. Java follows the famous principle of **WORA (Write Once, Run Anywhere)**.
