---
layout: post
title: Java Virtual Machine (JVM)
---

**Java Virtual Machine** (JVM) is a core component of the **Java Runtime Environment** (JRE). The other component of the JRE is the Java API.
 
JVM is a specification of an abstract computing machine. A correct implementation of the Java Virtual Machine compiles a Java source file (*.java* file) to Java byte code (*.class* file) and reads this **class** file format through the Class Loader and compiles it into byte codes. These byte codes can then run on any computer with JRE installed on it. The emulated virtual machine is contained in the JRE. The JVM acts both as a compiler (*.class* file to byte code) and and the interpretor (byte code to machine
language)
 
The core functions of a JVM are handled by:

- A set of registers
  - It holds the state of the virtual machine
- A stack
  - JVM uses an **operand stack** which follows the **last-in first-out** (LIFO) terminology
  - It supplies parameters to methods and operations, and receives results back from them 
- An execution environment
  - It is maintained as a data set in the stack
  - It handles dynamic linking, normal method returns, and exception generation
- A garbage-collected heap
  - It is alternatively called **memory allocation pool** because class object instances are allocated from this heap
  - The heap can grow dynamically so unused objects are *automatically deallocated or garbage-collected* by the JVM
  - Garbage collection is performed as a background task
- A constant pool
  - It is associated with each class in the heap
  - It is typically created at compile time
- A method storage area
  - It stores byte code instructions associated with methods in the compiled code, and the symbol table used by the execution environment for dynamic linking
  - It also stores any debugging or additional information that might need to be associated with a method
- An instruction set
  - This is the byte code instructions used by JVM
 
The JVM ensures the **Write Once Run Anywhere** *(WORA)* principle because the it uses bytecode to execute Java programs and all JVM implementations must comply with the same specification.
 
For more detailed knowledge about how the JVM works, check Oracle's [Java Virtual Machine Specification](https://docs.oracle.com/javase/specs/jvms/se7/html/index.html) tutorial. There also excellent blogs on [cudrid](http://www.cubrid.org/blog/dev-platform/understanding-jvm-internals/) and [codeproject](http://www.codeproject.com/Articles/30422/How-the-Java-Virtual-Machine-JVM-Works).
