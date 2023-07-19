# `Java`: History and Platform Independence

- **1991**: Java was created by James Gosling at Sun Microsystems.
- **1995**: Java Alpha and Beta versions were released. It was freely downloadable and open source.
- **1996**: Java 1.0, also known as Oak, was released as the first official version of Java.

Key Features of Java:
- **Object-Oriented**: Java is an object-oriented programming language, which means it follows the principles of encapsulation, inheritance, and polymorphism.
- **Platform Independent**: Java programs can run on any platform that has a Java Virtual Machine (JVM) installed, regardless of the underlying hardware and operating system. This is achieved through the compilation of Java code into bytecode, which is executed by the JVM.
- **Portability**: Java programs are highly portable because they can be written once and run anywhere (WORA). This is possible due to the platform independence provided by the JVM.
- **Internet Programming Language**: Java was designed with built-in networking capabilities, making it suitable for internet programming and web applications.

Platform and Portability:
- A platform consists of a combination of a processor and an operating system (e.g., Intel processor with Windows OS, Mac with macOS, Intel with Linux).
- For software engineers, the platform typically refers to the operating system they are working on, such as Windows, Mac, or Linux.

Platform Dependency and Portability:
- In platform-dependent programming languages, the platform of compilation and the platform of execution must be the same. This means that the compiled executable file can only run on the same platform for which it was compiled.
- Java, on the other hand, is platform-independent and portable. The Java code is compiled into bytecode, which is a platform-neutral representation of the code. The bytecode is executed by the JVM, which interprets and runs the code on any platform that has a compatible JVM installed.

Java Code Execution Process:
- Java code is written in a high-level language (HLL).
- The Java code is compiled by the Java compiler (`javac`), which translates it into bytecode.
- The bytecode is platform-independent and can be executed on any platform that has a JVM.
- The JVM interprets the bytecode and executes it as a machine-dependent low-level program (MLL).

By utilizing the JVM and bytecode, Java achieves platform independence, allowing Java programs to run on different operating systems without the need for recompilation. This portability is one of the key advantages of Java and has contributed to its widespread use in various domains, including web development, enterprise systems, and mobile applications.

<br/>
<br/>

# Here's a diagram illustrating the Java code execution process:

```
                    Java Code (HLL)
                         |
                         v
           +---------------------------+
           |   Java Compiler (javac)   |
           +---------------------------+
                         |
                         v
                   Bytecode
                         |
                         v
           +---------------------------+
           |   Java Virtual Machine    |
           |          (JVM)           |
           +---------------------------+
                         |
                         v
    +---------------------------------+
    |    JVM Internally Interprets   |
    |     and Executes Bytecode      |
    +---------------------------------+
                         |
                         v
          Machine-Dependent Code
```

Explanation:
1. **Java Code (HLL)**: This is the Java program written in a high-level language, which contains the source code written by the programmer.

2. **Java Compiler (javac)**: The Java compiler takes the Java code as input and compiles it into bytecode. Bytecode is a platform-independent representation of the Java program.

3. **Bytecode**: Bytecode is the intermediate code generated by the Java compiler. It is in a format that can be understood and executed by the Java Virtual Machine (JVM).

4. **Java Virtual Machine (JVM)**: The JVM is a virtual machine that interprets and executes the bytecode. It is responsible for translating the platform-independent bytecode into machine-specific instructions.

5. **JVM Internally Interprets and Executes Bytecode**: The JVM uses its internal interpreter to read and execute the bytecode instructions. The interpreter translates each bytecode instruction into machine-level instructions that the underlying hardware can understand.

6. **Machine-Dependent Code (MLL)**: After interpreting the bytecode, the JVM executes machine-dependent code that is specific to the underlying hardware and operating system. This machine-dependent code is executed on the actual machine, making it platform-specific.

Overall, this process of compilation and execution through the JVM allows Java to achieve platform independence and portability, making it possible to run Java programs on various platforms without the need for recompilation.

<br/>
<br/>

## **Compiler** and **interpreter** are two different approaches to execute programs:

**Compiler:**
- A compiler is a software tool that converts the entire source code of a program into machine code (or bytecode) before execution.
- The compilation process includes lexical analysis, syntax analysis, semantic analysis, optimization, and code generation.
- The resulting machine code or bytecode can be directly executed by the target machine or a virtual machine.
- Compilation is typically a one-time process, and the generated code can be executed multiple times without recompiling, providing faster execution.
- Examples of compiled languages include C, C++, Java (bytecode is compiled ahead of time), and Go.

**Interpreter:**
- An interpreter is a program that reads and executes the source code of a program line by line or statement by statement.
- The interpreter translates and executes each instruction or statement one at a time.
- It does not generate an executable output; instead, it directly executes the program by interpreting and executing the instructions on the fly.
- Interpreters are typically slower than compiled programs because they perform interpretation at runtime.
- Examples of interpreted languages include Python, JavaScript, Ruby, and Perl.

**Comparison:**
- Compilation is done before execution, whereas interpretation is done during execution.
- Compiled programs generally have faster execution speed, while interpreted programs may have slower execution due to the interpretation overhead.
- Compilation provides an opportunity for advanced optimizations, resulting in more efficient code.
- Interpreted programs are often easier to debug and modify since they can execute line by line.
- Compiled programs are usually more portable, as the compiled machine code can be executed on any compatible platform, while interpreters may need to be installed on each platform.

It's important to note that the line between compilation and interpretation can be blurred in some scenarios. For example, Just-In-Time (JIT) compilation used in Java and other languages combines elements of both compilation and interpretation, where bytecode is compiled into machine code at runtime for better performance.

<br/>
<br/>

# Java uses both Compiler and Interpreter

Java uses both a compiler and an interpreter in its execution process. Let's understand how Java utilizes both:

**1. Compiler:**
When you write Java source code, it is saved in `.java` files. The Java compiler, `javac`, translates these `.java` files into an intermediate form called **bytecode**. Bytecode is a platform-independent representation of the source code and is stored in `.class` files.

**2. Interpreter:**
Java uses an interpreter called the **Java Virtual Machine (JVM)** to execute the bytecode. The JVM reads the bytecode line by line and executes it on the host machine. The JVM is responsible for translating the bytecode into machine code specific to the underlying platform at runtime.

The overall process of running Java programs involves both compilation and interpretation:

1. Compilation: The Java compiler (`javac`) compiles the `.java` source files into bytecode (`.class` files).

2. Interpretation: The JVM interprets the bytecode and converts it into machine code for the specific platform on which the Java program is running.

Additionally, Java introduced a concept called **Just-In-Time (JIT) Compilation**, which further blurs the line between compilation and interpretation. The JVM can use JIT compilation to dynamically translate bytecode into native machine code at runtime, optimizing performance by detecting frequently executed code paths.

This combination of compilation to bytecode and interpretation (and JIT compilation) at runtime allows Java to achieve its key feature of platform independence, where Java programs can run on any platform with a suitable JVM implementation, regardless of the underlying hardware and operating system.

<br/>
<br/>

# Java Versions

1. **J2SE (1.2) - 1998:**
   - Introduced the Collection Framework, providing data structures like List, Set, Map, etc.
   - Introduced Swing GUI library, which allowed developers to create cross-platform graphical user interfaces.
   - Introduced JIT (Just-In-Time) compiler, improving the runtime performance of Java programs.

2. **J2SE (1.3) - 2000:**
   - Improved performance and stability over the previous version.

3. **J2SE (1.4) - 2002:**
   - Introduced Regular Expressions in the `java.util.regex` package.
   - Improved XML parsing with XML APIs (JAXP).
   - Added the assert keyword for assertions.

4. **J2SE (5.0) - 2004:**
   - Introduced Generics, enabling type-safe collections and classes.
   - Enhanced for-loop to iterate through collections more conveniently.
   - Autoboxing and Unboxing to automatically convert primitive types to wrapper classes and vice versa.
   - Annotations to provide metadata and support for annotations-based frameworks.

5. **Java SE 6 - 2006:**
   - Introduced support for scripting languages through the `javax.script` package.
   - Enhanced support for Web Services (JAX-WS).
   - Introduced the Java Compiler API (`javax.tools`) for programmatic access to Java compiler.

6. **Java SE 7 - 2011:**
   - Introduced String in Switch, allowing the use of strings in switch-case statements.
   - Try-with-resources, simplifying resource management by automatically closing resources.
   - Diamond Operator (`<>`) for simplifying generic type inference.

7. **Java SE 8 - 2014:**
   - Introduced Lambda Expressions, enabling functional programming in Java.
   - Date and Time API (`java.time`) for improved date and time manipulation.
   - Stream API (`java.util.stream`) for performing functional-style operations on collections.

8. **Java SE 9 - 2017:**
   - Introduced the Modular System (Project Jigsaw) to create more maintainable and scalable applications.
   - Reactive Streams to support reactive programming and asynchronous data processing.
   - JShell, a Read-Eval-Print Loop (REPL) for interactive Java programming.

9. **Java 10 - 2018:**
   - Introduced Local-Variable Type Inference (var) to allow the compiler to infer variable types.

10. **Java SE 11:**
    - Introduced the ability to run Java source code directly without explicitly compiling it.
    - 'var' can now be used with Lambda parameters.

11. **Java SE 12:**

12. **Java SE 13:**
    - Introduced Switch Expressions, a simplified and more concise form of switch statements.
    - Multiline Strings with the `"""` syntax for multiline string literals.

13. **Java SE 14:**
    - Introduced Records, a concise way to declare classes that are mainly used to store data.
    - Introduced the Packaging Tool (`jpackage`) for packaging Java applications into native installers.

14. **Java SE 15:**
15. **Java SE 16:**
16. **Java SE 17:**
    - Introduced Sealed Classes to restrict the inheritance hierarchy of a class.

17. **Java SE 18:**

18. **Java SE 19:**
    - Introduced Virtual Threads to improve the efficiency of multi-threaded applications.
    - Introduced the Vector API to provide a mechanism for SIMD (Single Instruction, Multiple Data) operations.

**LTS Versions:**
Java Long-Term Support (LTS) versions are versions of Java that receive extended support and updates for a longer period. The LTS versions mentioned in the provided list are Java 7, Java 8, Java 11, and Java 17. These versions are suitable for applications that require long-term stability and support.

<br/>
<br/>

# Some Important Notes

**MLL (Machine-Level Language):**
- MLL contains instructions in binary form, represented by 0's and 1's, which are specific to the architecture of the target machine.
- It is the lowest level of programming language that directly interacts with the hardware of the computer.
- MLL code is machine-dependent, meaning it can only run on the architecture it was compiled for.

**Bytecode:**
- Bytecode is an intermediate representation of code that is generated by the Java compiler (javac) when you compile a Java source code file (.java).
- Unlike MLL, bytecode is not specific to any particular machine architecture, making it platform-independent.
- Bytecode is not directly executable by the computer's hardware; it requires a Java Virtual Machine (JVM) to interpret and execute it.

**Architectural Neutral / Platform Independence / WORA (Write Once, Run Anywhere):**
- These terms all refer to the ability of Java to run on any platform without modification, thanks to its platform-independent bytecode.
- When you compile a Java source code file, it is converted into bytecode (.class files) that is not tied to any specific hardware or operating system.
- The JVM acts as an intermediary between the bytecode and the underlying hardware, translating the bytecode into native machine code that the host system can execute.

**Just-In-Time Compiler (JIT):**
- JIT is a component of the JVM that translates bytecode into native machine code at runtime, just before it is executed.
- When a Java application is launched, the JVM interprets the bytecode using an internal interpreter. However, to improve performance, the JVM may use the JIT compiler to convert frequently executed bytecode sequences into optimized native machine code.
- The JIT compiler helps to bridge the performance gap between interpreted languages (like Java bytecode) and natively compiled languages (like C), making Java applications faster over time.

**Java Language vs. C Language Compilation:**
- C language code is compiled into machine-specific object files (.obj), which are not portable across different architectures and operating systems. The object files need to be recompiled for each target platform.
- Java language code is compiled into platform-independent bytecode (.class files) by the Java compiler (javac). This bytecode can be executed on any platform with the help of a JVM, without the need for recompilation.

In summary, Java's architecture-neutral bytecode allows developers to write code once and run it on any platform with a compatible JVM, making Java a "Write Once, Run Anywhere" language. The JVM acts as an abstraction layer between the Java code and the underlying hardware, providing platform independence and allowing Java applications to be executed on various operating systems and architectures. Additionally, the JIT compiler further optimizes the performance of Java applications by translating frequently executed bytecode into native machine code.

<br/>
<br/>

**Q1: Does JVM contain the Java compiler, or is the Java compiler separate?**
- The JVM (Java Virtual Machine) and the Java compiler are separate components in the Java Development Kit (JDK).
- The Java compiler, represented by the `javac` command, is responsible for compiling Java source code files (with .java extension) into bytecode files (with .class extension).
- The JVM is responsible for executing the bytecode and providing a runtime environment for Java applications to run.

**Java Execution Flow:**
1. **Source Code (`.java` file):** A Java developer writes Java source code in a text file with the extension .java. This source code contains human-readable instructions written in the Java programming language.

2. **Compilation (Java Compiler `javac`):** The Java source code is compiled using the Java compiler (`javac`). The compiler reads the source code, checks for syntax errors, and translates it into platform-independent bytecode. This bytecode is saved in a separate file with the extension .class.

3. **Bytecode (`.class` file):** The `.class` file contains the bytecode, which is a low-level representation of the Java source code. Bytecode is not specific to any platform or architecture and can be executed on any system that has a compatible JVM.

4. **Java Virtual Machine (JVM - Interpreter):** When you run a Java application, the JVM (Java Virtual Machine) comes into play. The JVM is responsible for interpreting the bytecode and executing it line by line.

5. **Interpreter Execution:** The JVM uses an internal interpreter to execute the bytecode line by line. It reads each bytecode instruction, translates it into native machine code (for the host system), and executes it. This process is repeated for each bytecode instruction in the program.

**Key Points:**
- The JVM acts as an interpreter for Java bytecode, executing it line by line at runtime.
- The JVM is part of the Java Runtime Environment (JRE), which is included in the JDK along with the Java compiler.
- The JVM is platform-dependent, meaning it is specific to the hardware and operating system on which it runs. However, the bytecode it interprets is platform-independent.
- The interpreter allows Java applications to be "Write Once, Run Anywhere" since the same bytecode can be executed on any system with a compatible JVM.

In summary, the Java compiler (`javac`) is responsible for translating Java source code into platform-independent bytecode (.class files). The JVM, which is a part of the JRE, interprets this bytecode and executes it line by line, allowing Java applications to run on any platform with a compatible JVM. The JVM's interpreter provides the platform independence and portability that makes Java a cross-platform language.