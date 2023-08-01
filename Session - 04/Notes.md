```java
class FirstCode{
    public static void Main(String args[]){
        System.out.println("Hello World");
    }
}
```

```java
class FirstCode {
```
This line begins the declaration of a Java class named `FirstCode`. In Java, a class is a blueprint or a template for creating objects that encapsulate data and behavior.

```java
public static void Main(String args[]) {
```
This line is the starting point of the Java program. In Java, the entry point of any program is the `main` method, which should be declared exactly like this to be recognized by the Java Virtual Machine (JVM). The `main` method is declared as `public` (accessible from other classes), `static` (belongs to the class rather than an instance of the class), and `void` (does not return any value).

The `String args[]` is the parameter to the `main` method. It represents the command-line arguments passed to the program when it is executed. `args` is an array of strings, where each element of the array corresponds to a command-line argument.

```java
System.out.println("Hello World");
```
This line is used to print the string "Hello World" to the console. In Java, the `System` class provides access to various system resources, and `out` is a static member of the `System` class representing the standard output stream. The `println` method is used to print a string to the console, followed by a new line.

```java
}
```
This closing curly brace marks the end of the `main` method.

```java
}
```
This closing curly brace marks the end of the `FirstCode` class.

In summary, this Java program defines a class called `FirstCode` with a `main` method that prints "Hello World" to the console. When you run this program, you'll see the output:

```
Hello World
```

This is a basic "Hello World" program, often used as a starting point for learning a new programming language. It confirms that you have set up your development environment correctly and can run a simple program.

<br/>
<br/>

# Notes

1. `<fileName>.java`: This is a placeholder representing the name of your Java source code file. In Java, the source code files have a `.java` extension. When you write your Java code, you should save it with a meaningful name and the `.java` extension. For example, if your file contains a class named `MyProgram`, you would save it as `MyProgram.java`.

2. `javac` - Compile the code: `javac` is the Java compiler, a program that translates your human-readable Java source code into an intermediate form called bytecode. Bytecode is a platform-independent representation of your Java program and is executed by the Java Virtual Machine (JVM). To compile your Java source code, open your terminal (command prompt or PowerShell on Windows, or a terminal on macOS/Linux) and navigate to the directory where your `MyProgram.java` file is located. Then, execute the following command:

   ```
   javac MyProgram.java
   ```

   This command will invoke the Java compiler (`javac`) and instruct it to compile `MyProgram.java`. If there are no syntax errors in your code, the compiler will generate a bytecode file named `MyProgram.class`. The `.class` file contains the compiled bytecode.

3. `java` - Run the code: `java` is the Java Virtual Machine (JVM), an interpreter that executes the Java bytecode. Once you have successfully compiled your Java code and obtained the `.class` file, you can run your program using the `java` command. In the terminal, execute the following command:

   ```
   java MyProgram
   ```

   This command tells the JVM to execute the bytecode in the `MyProgram.class` file. The JVM will load the necessary classes, initialize the program, and start the `main` method, which serves as the entry point of your Java program.

Important Notes:

- Make sure that you have Java Development Kit (JDK) installed on your system. JDK includes the Java compiler (`javac`) and the Java Virtual Machine (`java`). If you haven't installed JDK, you can download it from the official Oracle website or use a package manager on macOS or Linux.
- Ensure that you set up the `JAVA_HOME` environment variable correctly to point to the JDK installation directory. Additionally, add the JDK's `bin` directory to your system's `PATH` environment variable. This allows you to run `javac` and `java` commands from any directory in the terminal.

In summary, Java source code files have a `.java` extension, and the Java compiler (`javac`) is used to compile them into bytecode (`.class` files). The Java Virtual Machine (`java`) then interprets and executes the bytecode, running your Java program. By following these steps, you can write, compile, and run your Java programs effectively.

<br/>
<br/>

In Java, the `String args[]` is a parameter in the `main` method and represents the command-line arguments passed to the program when it is executed. Let's explain it in detail and provide a coding example to illustrate its usage.

```java
public static void main(String args[]) {
    // Your code goes here
}
```

Explanation:

- `public`: This is an access modifier, which means that the `main` method can be accessed from other classes. It allows the JVM to call the `main` method from outside the class.

- `static`: This keyword indicates that the `main` method belongs to the class itself rather than an instance of the class. The `main` method must be declared as static because the JVM can call it without creating an object of the class.

- `void`: The return type of the `main` method is `void`, which means the method does not return any value.

- `main`: This is the name of the method. The JVM looks for this exact method signature to start the execution of the program.

- `String args[]`: This is the parameter of the `main` method. It is an array of strings (`String[]`) and is used to pass command-line arguments to the program. When you run a Java program from the command line, you can pass additional information to the program through these command-line arguments.

Coding Example:

Let's create a simple Java program that demonstrates how to use the `args` parameter to access command-line arguments:

```java
public class CommandLineArgumentsExample {
    public static void main(String args[]) {
        // Check if any command-line arguments are provided
        if (args.length > 0) {
            System.out.println("Command-line arguments passed:");
            // Loop through the arguments and print them one by one
            for (int i = 0; i < args.length; i++) {
                System.out.println("Argument " + (i + 1) + ": " + args[i]);
            }
        } else {
            System.out.println("No command-line arguments provided.");
        }
    }
}
```

In this example, we have created a class named `CommandLineArgumentsExample`. Inside the `main` method, we first check if any command-line arguments are passed by using `args.length > 0`. If there are arguments, we loop through the `args` array and print each argument along with its index. If no arguments are provided, the program prints a message indicating that no command-line arguments were passed.

To run this program with command-line arguments, follow these steps:

1. Open your terminal or command prompt.
2. Compile the Java file (`CommandLineArgumentsExample.java`) using `javac`:

   ```
   javac CommandLineArgumentsExample.java
   ```

3. After a successful compilation, run the program using `java`, and provide some command-line arguments:

   ```
   java CommandLineArgumentsExample arg1 arg2 arg3
   ```

   Replace `arg1`, `arg2`, and `arg3` with the arguments you want to pass. For example:

   ```
   java CommandLineArgumentsExample apple banana cherry
   ```

Output:
```
Command-line arguments passed:
Argument 1: apple
Argument 2: banana
Argument 3: cherry
```

If you run the program without providing any command-line arguments:

```
java CommandLineArgumentsExample
```

Output:
```
No command-line arguments provided.
```

This demonstrates how you can use the `String args[]` parameter to access command-line arguments and use them in your Java programs.

<br/>
<br/>

# All possible situations related to the `public static void main(String args[])` method (often abbreviated as `psvm`), which serves as the entry point of a Java program.

**1. Standard `main` method with command-line arguments:**
```java
public static void main(String[] args) {
    // Code to be executed when the program is run
    // using command-line arguments.
}
```
In this common scenario, the program is executed from the command line, and any command-line arguments are passed through the `args` parameter. You can access and process these arguments inside the `main` method.

Example execution:
```
java MyProgram arg1 arg2 arg3
```

**2. Standard `main` method without command-line arguments:**
```java
public static void main(String[] args) {
    // Code to be executed when the program is run
    // without any command-line arguments.
}
```
If the program is run without any command-line arguments, the `args` array will be empty. You can handle this case and execute appropriate logic inside the `main` method.

Example execution:
```
java MyProgram
```

**3. Invalid `main` method signature:**
```java
public static void main() {
    // This is not a valid main method signature.
    // The method must have a single parameter of type String[] (String array).
}
```
The `main` method should always have a single parameter of type `String[]` to receive command-line arguments. If you define the `main` method without this parameter, it won't be recognized as the entry point of the program.

**4. Incorrect array parameter name:**
```java
public static void main(String[] arguments) {
    // This is still a valid main method, but it is better to use 'args' as the parameter name for consistency.
}
```
While you can use any valid identifier as the parameter name for the `main` method, it is a common convention to use `args`, which stands for "arguments." Using a different name, like `arguments`, is technically valid but not recommended for readability and consistency.

**5. Overloaded `main` method:**
```java
public static void main(String[] args) {
    // Main method for command-line arguments
}

public static void main() {
    // Overloaded main method without command-line arguments
}
```
Java allows method overloading, which means you can have multiple `main` methods within the same class. However, only the one with the correct signature (`String[] args`) will be recognized as the entry point when executing the program from the command line.

**6. `main` method in inner classes:**
```java
public class MyClass {
    public static void main(String[] args) {
        // Main method inside the outer class
    }

    public static class InnerClass {
        public static void main(String[] args) {
            // Main method inside the inner class
        }
    }
}
```
You can have `main` methods in both the outer and inner classes. When running the program, only the `main` method in the outer class will serve as the entry point.

**7. Using `String...` instead of `String[]`:**
```java
public static void main(String... args) {
    // This is a valid alternative to using String[]
}
```
Java allows using the `String...` syntax (varargs) instead of `String[]` for the `main` method's parameter. It has the same effect, and you can access command-line arguments in the same way.

These are the various possible situations related to the `psvm` method in Java. Keep in mind that the `main` method is essential for running Java applications and serves as the starting point for program execution. It is where you put the logic that should be executed when your Java program is launched.

<br/>
<br/>

## FAQ's 

**Q: WHy static keyword in main method?**<br/>
The `static` keyword in the `main` method is essential for the Java Virtual Machine (JVM) to locate and execute the method without creating an instance of the class. There are specific reasons why the `main` method needs to be declared as `static`:

1. **Entry Point:** In Java, when you run a program using the `java` command, the JVM looks for a specific method signature to start the execution. The required method signature is `public static void main(String[] args)`. If the `main` method were not static, the JVM would have to create an instance of the class containing the `main` method to execute it, but it wouldn't know how to create the instance without first executing the `main` method. This creates a circular dependency that cannot be resolved. By making `main` static, the JVM can call it directly without creating an instance of the class.

2. **Class-level Scope:** Static methods belong to the class rather than to any specific instance of the class. Since the `main` method is the entry point of the program, it should be accessible even before any objects are created. This ensures that the method can be called even before any instances of the class are created.

3. **No `this` Reference:** Inside a static method, you cannot access instance-level members (fields or non-static methods) directly using the `this` keyword because `this` refers to the current instance, which doesn't exist in the static context. Since the `main` method is static, it doesn't have access to instance-specific data, which is reasonable because the entry point should be independent of any object state.

4. **Avoiding Ambiguity:** If `main` were allowed to be non-static, it could be overridden in subclasses. This would lead to ambiguity for the JVM, as it wouldn't know which subclass's `main` method to call when starting the program.

Given these reasons, the `main` method in Java must always be declared as `public static void main(String[] args)`. When you run a Java program, the JVM searches for this exact signature to start the execution and runs the code inside the `main` method to launch your application.