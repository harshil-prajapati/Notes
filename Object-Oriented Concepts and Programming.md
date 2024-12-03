
---
### Features of Java

1. **Object-Oriented**  
    Java follows the object-oriented programming paradigm, focusing on objects and classes, making code reusable and modular.
2. **Platform-Independent**  
    Java programs are compiled into bytecode, which can run on any platform with a Java Virtual Machine (JVM).
3. **Simple**  
    Java has a clean syntax, similar to C++, but without complex features like pointers and operator overloading.
4. **Secure**  
    Java provides built-in security features such as bytecode verification, exception handling, and lack of explicit pointers.
5. **Robust**  
    Java has strong memory management, exception handling, and features like garbage collection to prevent memory leaks.
6. **Multithreaded**  
    Java supports multithreading, allowing multiple tasks to run concurrently within a program.
---
---
---
### What is JDK, JRE, JVM, JIT, GC

1. **JDK (Java Development Kit)**  
    A software development kit used to develop Java applications. It includes tools like a compiler (javac), debugger, and the JRE.
2. **JRE (Java Runtime Environment)**  
    Provides the runtime environment to execute Java programs. It includes the JVM and libraries required for program execution.
3. **JVM (Java Virtual Machine)**  
    A virtual machine that executes Java bytecode. It provides platform independence by abstracting the underlying operating system.
4. **JIT (Just-In-Time Compiler)**  
    A component of the JVM that improves performance by compiling bytecode into native machine code at runtime.
5. **GC (Garbage Collection)**  
    An automated process in Java that frees memory by removing unused or unreferenced objects, ensuring efficient memory management.
---
---
---
### OOPs Concept

1. **Class and Object**
    - **Class**: A blueprint or template for creating objects.
    - **Object**: An instance of a class with real-world attributes and behaviors.
2. **Encapsulation**
    - Wrapping data (variables) and methods (functions) into a single unit (class).
    - Ensures data hiding and security by restricting direct access.
3. **Inheritance**
    - Enables a new class (child) to inherit properties and methods of an existing class (parent).
    - Promotes reusability of code.
4. **Polymorphism**
    - Allows a single entity to take multiple forms.
    - Achieved through method overloading (compile-time) and method overriding (runtime).
5. **Abstraction**
    - Hides implementation details and shows only essential features.
    - Achieved using abstract classes and interfaces.
---
### Advantages of OOPs

1. **Reusability**
    - Code can be reused through inheritance, saving time and effort.
2. **Scalability**
    - Easy to add new features or modify existing ones without affecting other parts of the program.
3. **Data Security**
    - Encapsulation protects sensitive data by controlling access.
4. **Modularity**
    - Dividing the program into objects or classes improves modularity and organization.
5. **Ease of Maintenance**
    - Clear structure and reusability make programs easier to debug, maintain, and update.
6. **Real-World Representation**
    - OOP maps real-world problems into classes and objects, making complex problems easier to solve.
---
---
---
### What is Class and Object? Differentiate it
### Class

- A **class** is a blueprint or template that defines properties (attributes) and methods (behaviors) for creating objects.
- It is a logical construct that does not occupy memory until objects are created from it.

**Example:**
```java
class Car {
    String brand;  // Attribute
    void drive() { // Method
        System.out.println("The car is driving.");
    }
}
```

---
### Object

- An **object** is an instance of a class that holds actual values for the attributes and allows access to the methods defined in the class.
- Objects occupy memory when created.

**Example:**
```java
Car myCar = new Car();  // Object creation
myCar.brand = "Toyota"; // Assign value
myCar.drive();          // Access method
```

---
### Difference Between Class and Object

| **Aspect**     | **Class**                           | **Object**                       |
| -------------- | ----------------------------------- | -------------------------------- |
| **Definition** | Blueprint for creating objects.     | Instance of a class.             |
| **Memory**     | Does not occupy memory.             | Occupies memory when created.    |
| **Usage**      | Defines attributes and methods.     | Accesses attributes and methods. |
| **Creation**   | Declared using the `class` keyword. | Created using the `new` keyword. |
| **Example**    | `class Car { ... }`                 | `Car myCar = new Car();`         |

---
---
---
### What is Inheritance?

Inheritance is a fundamental concept of object-oriented programming (OOP) that allows a class (child class) to acquire the properties and methods of another class (parent class). It promotes **code reuse**, extensibility, and modularity.

**Example:**
```java
class Parent {
    void display() {
        System.out.println("This is the parent class.");
    }
}

class Child extends Parent {
    void show() {
        System.out.println("This is the child class.");
    }
}

public class Main {
    public static void main(String[] args) {
        Child obj = new Child();
        obj.display();  // Access parent class method
        obj.show();     // Access child class method
    }
}
```

---
### Types of Inheritance

1. **Single Inheritance**
    - A child class inherits from a single parent class.  
        **Example:**
    ```java
    class Parent { ... }
    class Child extends Parent { ... }
    ```
2. **Multilevel Inheritance**
    - A child class inherits from a parent class, and another class inherits from the child class.  
        **Example:**
    ```java
    class GrandParent { ... }
    class Parent extends GrandParent { ... }
    class Child extends Parent { ... }
    ```
3. **Hierarchical Inheritance**
    - Multiple child classes inherit from a single parent class.  
        **Example:**
    ```java
    class Parent { ... }
    class Child1 extends Parent { ... }
    class Child2 extends Parent { ... }
    ```
4. **Hybrid Inheritance**
    - A combination of two or more types of inheritance (not directly supported in Java due to ambiguity but achieved using interfaces).  
        **Example:**
    ```java
    interface A { ... }
    class B { ... }
    class C extends B implements A { ... }
    ```
5. **Multiple Inheritance (via Interface)**
    - A class can implement multiple interfaces to achieve multiple inheritance.  
        **Example:**
    ```java
    interface A { ... }
    interface B { ... }
    class C implements A, B { ... }
    ```
---
---
---
### What is Polymorphism?

Polymorphism is an OOP concept that allows a single entity (method or object) to perform in multiple ways. It enables the same method name to behave differently depending on the context.

---
### Types of Polymorphism

1. **Compile-Time Polymorphism (Method Overloading)**
    
    - Achieved when multiple methods in the same class have the same name but different parameter lists (number, type, or order of parameters).
    - Determined during compilation.
    **Example:**
    ```java
    class Calculator {
        int add(int a, int b) {
            return a + b;
        }
        double add(double a, double b) {
            return a + b;
        }
    }
    public class Main {
        public static void main(String[] args) {
            Calculator calc = new Calculator();
            System.out.println(calc.add(5, 3));       // Calls int add
            System.out.println(calc.add(5.2, 3.3));  // Calls double add
        }
    }
    ```
---
2. **Runtime Polymorphism (Method Overriding)**
    - Achieved when a subclass provides its own implementation of a method already defined in the parent class.
    - Determined during runtime.
    **Example:**
    ```java
    class Animal {
        void sound() {
            System.out.println("Animal makes a sound");
        }
    }
    class Dog extends Animal {
        @Override
        void sound() {
            System.out.println("Dog barks");
        }
    }
    public class Main {
        public static void main(String[] args) {
            Animal a = new Dog();
            a.sound();  // Calls Dog's sound method
        }
    }
    ```
---
### Difference Between Method Overloading and Overriding

| **Aspect**            | **Method Overloading**                      | **Method Overriding**                                       |
| --------------------- | ------------------------------------------- | ----------------------------------------------------------- |
| **Definition**        | Same method name with different parameters. | Same method name and signature in child class.              |
| **Polymorphism Type** | Compile-Time Polymorphism.                  | Runtime Polymorphism.                                       |
| **Classes Involved**  | Happens within a single class.              | Involves parent and child classes.                          |
| **Access Modifiers**  | No restriction on modifiers.                | Cannot reduce the visibility of the parent method.          |
| **Annotations**       | Not required.                               | Requires `@Override` annotation (optional but recommended). |

---
---
---
### What is Wrapper Class?

A **Wrapper Class** in Java is a predefined class that provides an object representation for primitive data types. It wraps primitive values (e.g., `int`, `float`) into objects, allowing them to be used where objects are required, such as in **collections**.

---
### List of Wrapper Classes

|**Primitive Type**|**Wrapper Class**|
|---|---|
|`byte`|`Byte`|
|`short`|`Short`|
|`int`|`Integer`|
|`long`|`Long`|
|`float`|`Float`|
|`double`|`Double`|
|`char`|`Character`|
|`boolean`|`Boolean`|

---
### Example of Wrapper Class Usage

1. **Converting Primitive to Object (Autoboxing)**
    ```java
    int num = 10;
    Integer obj = num;  // Autoboxing
    System.out.println(obj);  // Output: 10
    ```
2. **Converting Object to Primitive (Unboxing)**
    ```java
    Integer obj = 20;
    int num = obj;  // Unboxing
    System.out.println(num);  // Output: 20
    ```
    
---
### Advantages of Wrapper Classes

1. **Use in Collections**  
    Collections like `ArrayList` store objects, not primitives, so wrapper classes are essential.
2. **Utility Methods**  
    Wrapper classes provide utility methods, such as `Integer.parseInt()` to convert a string to an integer.
3. **Default Values in Generics**  
    Allows primitives to be used in generics and other object-dependent features.
4. **Supports Autoboxing and Unboxing**  
    Simplifies conversion between primitives and objects automatically.
---
---
---
### Differentiate Between Constructor and Function

|**Aspect**|**Constructor**|**Function (Method)**|
|---|---|---|
|**Definition**|Special method used to initialize an object.|Block of code executed when called explicitly.|
|**Name**|Same as the class name.|Can have any valid name.|
|**Return Type**|No return type, not even `void`.|Must have a return type (`void` or any data type).|
|**Call**|Automatically called when an object is created.|Explicitly called using the object.|
|**Purpose**|Used to initialize object properties.|Used to define behavior or logic.|
|**Overloading**|Can be overloaded by defining multiple constructors with different parameters.|Can also be overloaded.|
|**Inheritance**|Not inherited by child classes.|Can be inherited by child classes.|
|**Example**|||
|**Constructor:**|||

```java
class Demo {
    int x;
    Demo() {  // Constructor
        x = 10;
    }
}
Demo obj = new Demo(); // Called automatically
```

**Function:**

```java
class Demo {
    void display() {  // Function
        System.out.println("This is a method.");
    }
}
Demo obj = new Demo();
obj.display(); // Called explicitly
```
---
---
---
### Use of Abstract Class:

An abstract class in Java is used to provide a common base for other classes. It allows you to define some methods with a default implementation, while other methods are left abstract, forcing subclasses to provide their own implementation. It helps in reducing code duplication and defining a contract for the subclasses.

### Restrictions of Abstract Class:

1. **Cannot be instantiated**: You cannot create an object of an abstract class directly.
2. **Must be subclassed**: An abstract class must be extended by a concrete subclass.
3. **Cannot be `final`**: It cannot be declared as `final` because it needs to be extended.
4. **Cannot have static abstract methods**: Abstract methods cannot be static.
5. **Abstract methods must be implemented**: Any non-abstract subclass must implement all abstract methods.
6. **Cannot have private abstract methods**: Abstract methods must be accessible to subclasses, so they cannot be private.
7. **Cannot have final or synchronized abstract methods**: These modifiers prevent overriding, which conflicts with the purpose of abstract methods.
---
---
---
### Difference Between String and StringBuffer:

| **Aspect**             | **String**                                                                  | **StringBuffer**                                                      |
| ---------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Immutability**       | Immutable (cannot be modified after creation).                              | Mutable (can be modified after creation).                             |
| **Performance**        | Slower for modifications due to immutability.                               | Faster for modifications (e.g., appending).                           |
| **Memory Consumption** | Consumes more memory because new objects are created for each modification. | More memory efficient since it modifies the existing object.          |
| **Usage**              | Best for fixed, constant strings.                                           | Ideal for dynamic string manipulation.                                |
| **Methods**            | Does not have methods for modification like append() or delete().           | Has methods like append(), insert(), delete(), etc. for modification. |
| **Thread Safety**      | Thread-safe (due to immutability).                                          | Not thread-safe unless explicitly synchronized.                       |
| **Example**            | `String str = "Hello";`                                                     | `StringBuffer sb = new StringBuffer("Hello");`                        |

---
---
---
### List out any 10 methods of String handling with return type, parameters of the method, and use of that method.

| **Method**                      | **Return Type** | **Parameters**       | **Use**                                                               |
| ------------------------------- | --------------- | -------------------- | --------------------------------------------------------------------- |
| `length()`                      | `int`           | None                 | Returns the length of the string.                                     |
| `charAt(int index)`             | `char`          | `int index`          | Returns the character at the specified index.                         |
| `substring(int start)`          | `String`        | `int start`          | Returns a new string starting from the specified index to the end.    |
| `substring(int start, int end)` | `String`        | `int start, int end` | Returns a new string from the specified start index to the end index. |
| `toLowerCase()`                 | `String`        | None                 | Converts all characters of the string to lowercase.                   |
| `toUpperCase()`                 | `String`        | None                 | Converts all characters of the string to uppercase.                   |
| `contains(CharSequence seq)`    | `boolean`       | `CharSequence seq`   | Returns `true` if the string contains the specified sequence.         |
| `indexOf(String str)`           | `int`           | `String str`         | Returns the index of the first occurrence of the specified string.    |
| `equals(String str)`            | `boolean`       | `String str`         | Returns `true` if the string is equal to the specified string.        |
| `trim()`                        | `String`        | None                 | Removes leading and trailing whitespace from the string.              |

---
---
---
### Explain any 3 methods that are available in StringBuffer class but not in String class.

1. **`append(String str)`**
    - **Return Type**: `StringBuffer`
    - **Parameters**: `String str`
    - **Use**: Adds the specified string to the end of the current `StringBuffer`. This method modifies the existing object.
2. **`insert(int offset, String str)`**
    - **Return Type**: `StringBuffer`
    - **Parameters**: `int offset, String str`
    - **Use**: Inserts the specified string at the given position (offset) in the `StringBuffer`.
3. **`delete(int start, int end)`**
    - **Return Type**: `StringBuffer`
    - **Parameters**: `int start, int end`
    - **Use**: Removes a substring from the `StringBuffer` starting at the specified `start` index and ending at the `end` index.

---
---
---
### What is Exception? Explain Errors and Exception in detail.

An **exception** in Java is an event that disrupts the normal flow of a program's execution. It occurs when a runtime error or abnormal condition arises, such as dividing by zero or accessing an invalid index in an array. Exceptions allow you to handle errors in a controlled way using mechanisms like `try-catch` blocks.

---

### Errors and Exception

1. **Errors**:
    - **Definition**: Errors are serious problems that typically occur due to system-level issues like hardware failures or resource exhaustion. These cannot be handled by the program.
    - **Examples**: `OutOfMemoryError`, `StackOverflowError`.
    - **Recovery**: Errors cannot be recovered from by the program and usually terminate the program.
2. **Exceptions**:
    - **Definition**: Exceptions occur due to logical problems in the program, such as invalid input or incorrect code. Unlike errors, exceptions can be caught and handled by the program.
    - **Examples**: `NullPointerException`, `ArrayIndexOutOfBoundsException`.
    - **Recovery**: Exceptions can be caught and handled using `try-catch` blocks to recover and allow the program to continue running.
---
---
---
### List out and purpose of any 10 predefined Exceptions in Java.

1. **`ArithmeticException`**
    - **Purpose**: Thrown when an exceptional arithmetic condition occurs, such as division by zero.
2. **`ArrayIndexOutOfBoundsException`**
    - **Purpose**: Thrown when an array has been accessed with an illegal index, i.e., an index outside its valid range.
3. **`NullPointerException`**
    - **Purpose**: Thrown when a method is invoked on a null object reference.
4. **`ClassNotFoundException`**
    - **Purpose**: Thrown when an application tries to load a class but cannot find its definition.
5. **`FileNotFoundException`**
    - **Purpose**: Thrown when attempting to open a file that does not exist or is inaccessible.
6. **`IOException`**
    - **Purpose**: Thrown when an I/O operation fails or is interrupted, such as reading or writing from a file.
7. **`NumberFormatException`**
    - **Purpose**: Thrown when an attempt is made to convert a string to a number, but the string does not have an appropriate format.
8. **`IllegalArgumentException`**
    - **Purpose**: Thrown when a method receives an illegal or inappropriate argument.
9. **`IndexOutOfBoundsException`**
    - **Purpose**: Thrown when an index is out of the range for a particular collection, such as a list or array.
10. **`SecurityException`**
- **Purpose**: Thrown when a security manager detects a security violation, such as attempting to access a restricted file.
---
---
---
### Explanation of `try`, `catch`, `finally`, `throw`, and `throws` in brief:

1. **`try`**:
    - **Purpose**: Defines a block of code in which exceptions might occur. It must be followed by one or more `catch` blocks or a `finally` block.
    - **Example**:
        ```java
        try {
            // code that may throw an exception
        }
        ```
2. **`catch`**:
    - **Purpose**: Used to handle exceptions that are thrown in the `try` block. It defines the type of exception it can catch.
    - **Example**:
        ```java
        catch (ExceptionType e) {
            // code to handle exception
        }
        ```
3. **`finally`**:
    - **Purpose**: A block of code that always runs, regardless of whether an exception is thrown or not. It's typically used to release resources like closing files or database connections.
    - **Example**:
        ```java
        finally {
            // code that will always execute
        }
        ```
4. **`throw`**:
    - **Purpose**: Used to explicitly throw an exception manually. It can be used to throw a new exception or an existing exception.
    - **Example**:
        ```java
        throw new IllegalArgumentException("Invalid argument");
        ```
5. **`throws`**:
    - **Purpose**: Used in method declarations to specify that a method can throw one or more exceptions. It notifies the caller to handle or propagate the exception.
    - **Example**        
        ```java
        public void method() throws IOException {
            // code that may throw IOException
        }
        ```
---
---
---
### Which are the ways to implement thread in Java? Explain with example.

There are two ways to implement threads in Java:

---
### 1. By Extending the `Thread` Class
- Create a class that extends `Thread` and override the `run()` method.
- Use `start()` to begin the thread.
#### Example:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t = new MyThread();
        t.start();
    }
}
```
---
### 2. By Implementing the `Runnable` Interface
- Implement the `Runnable` interface, override the `run()` method, and pass the `Runnable` object to a `Thread` object.
#### Example:
```java
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Thread is running using Runnable");
    }
}

public class Main {
    public static void main(String[] args) {
        MyRunnable r = new MyRunnable();
        Thread t = new Thread(r);
        t.start();
    }
}
```
---
### Difference:

- **Extending `Thread`**: Simple but less flexible.
- **Implementing `Runnable`**: More flexible, allows multiple inheritance.
---
---
---
### Explain Thread Life Cycle and its Prority.
---
### Thread Life Cycle
1. **New**: Thread is created but not started.
2. **Runnable**: Thread is eligible for execution after `start()`.
3. **Blocked/Waiting**: Thread is waiting for a resource or lock.
4. **Running**: state is when a thread is actively executing its code after being selected by the thread scheduler.
5. **Timed Waiting**: Thread is waiting for a specific time using `Thread.sleep()`.
6. **Terminated**: Thread finishes execution.
---
### Thread Priority
- Thread priorities range from `Thread.MIN_PRIORITY` (1) to `Thread.MAX_PRIORITY` (10), with the default priority being `Thread.NORM_PRIORITY` (5).
- Example of setting priority: `t.setPriority(Thread.MAX_PRIORITY);`

---
### Example:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread with priority: " + this.getPriority());
    }
}

public class ThreadExample {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
        
        t1.setPriority(Thread.MIN_PRIORITY);
        t2.setPriority(Thread.MAX_PRIORITY);
        
        t1.start();  // Low priority
        t2.start();  // High priority
    }
}
```
---
---
---
### Access Modifiers in Java (Within a Package)

|**Access Modifier**|**Description**|**Access within Same Package**|**Access outside Package**|
|---|---|---|---|
|**`public`**|The member is accessible from any other class in any package.|Yes|Yes|
|**`protected`**|The member is accessible within the same package or by subclasses.|Yes|Yes (in subclasses)|
|**`default`** (no modifier)|The member is accessible only within the same package.|Yes|No|
|**`private`**|The member is accessible only within the same class.|No|No|

---
---
---
### What is Generics? Explain bounded types, and generic hierarchies in detail.

Generics in Java allow you to write classes, interfaces, and methods that can work with any data type while providing compile-time type safety.

---
### Bounded Types

1. **Upper Bounded Wildcards (`? extends T`)**: Limits the type to `T` or its subtypes. Used for reading from a generic type.
    ```java
    public static void printList(List<? extends Number> list) { ... }
    ```
2. **Lower Bounded Wildcards (`? super T`)**: Limits the type to `T` or its supertypes. Used for writing to a generic type.
    ```java
    public static void addNumber(List<? super Integer> list) { ... }
    ```

---
### Generic Hierarchies

Generics support a hierarchy of types. You can restrict a generic class to a specific type or its subclasses.
```java
class Box<T extends Animal> { ... }
```

---
---
---
### What is a Hashtable?

A **Hashtable** is a collection class in Java that implements the **Map** interface. It stores key-value pairs, where each key is unique, and each key maps to exactly one value. The **Hashtable** uses a hash table data structure, which ensures that the retrieval of values based on keys is very fast (constant time complexity on average).

---
### Key Features of Hashtable:

- **Thread-Safety**: **Hashtable** is synchronized, meaning it is thread-safe and can be used in concurrent applications without the need for additional synchronization.
- **Key-Value Pair**: It stores elements in the form of key-value pairs. Both keys and values can be objects, and keys must be unique.
- **Null Values**: Unlike **HashMap**, **Hashtable** does not allow `null` for either keys or values.
- **Performance**: Due to its synchronization, **Hashtable** can be slower than other map implementations like **HashMap** when used in single-threaded environments.

---
### Example:
```java
import java.util.Hashtable;

public class Main {
    public static void main(String[] args) {
        Hashtable<Integer, String> ht = new Hashtable<>();
        
        // Adding elements
        ht.put(1, "Apple");
        ht.put(2, "Banana");
        ht.put(3, "Cherry");
        
        // Retrieving elements
        System.out.println(ht.get(1));  // Output: Apple
        
        // Removing elements
        ht.remove(2);
        
        // Printing the Hashtable
        System.out.println(ht);
    }
}
```

---
### Important Methods of Hashtable:
- **`put(K key, V value)`**: Adds a key-value pair to the hashtable.
- **`get(Object key)`**: Returns the value associated with the key.
- **`remove(Object key)`**: Removes the key-value pair.
- **`containsKey(Object key)`**: Checks if the hashtable contains the given key.
- **`size()`**: Returns the number of key-value pairs in the hashtable.
---
---
---
### Differentiate Vector and List

| **Aspect**        | **Vector**                                                        | **List**                                                     |
| ----------------- | ----------------------------------------------------------------- | ------------------------------------------------------------ |
| **Definition**    | A growable array of objects that implements the `List` interface. | An interface representing an ordered collection of elements. |
| **Thread Safety** | Synchronized (thread-safe).                                       | Not synchronized by default.                                 |
| **Resizing**      | Doubles in size when full.                                        | Increases size (e.g., 50%) when capacity is exceeded.        |
| **Usage**         | Legacy class, less preferred.                                     | Part of the modern Java Collections Framework.               |
| **Null Elements** | Allows `null` elements.                                           | Allows `null` elements.                                      |
| **Performance**   | Slower due to synchronization.                                    | Faster in single-threaded environments.                      |

---
---
---
### What is a Set?

A **Set** is a collection that does not allow duplicate elements. It implements the `Collection` interface. Common implementations include `HashSet`, `LinkedHashSet`, and `TreeSet`.
- **Characteristics**:
    - No duplicates.
    - Can maintain order (`LinkedHashSet`) or sort elements (`TreeSet`).
**Example**:
```java
Set<String> set = new HashSet<>();
set.add("Apple");
set.add("Banana");
set.add("Apple");  // Duplicate, won't be added
```
---
### What is Enumeration?

**Enumeration** is an interface that was used for iterating over elements in a collection. It is now considered outdated, with `Iterator` being the preferred method.
- **Methods**:
    - `hasMoreElements()`
    - `nextElement()`
---
### What is Map?

A **Map** is a collection that maps keys to values. It does not allow duplicate keys, but values can be duplicated. Common implementations include `HashMap`, `LinkedHashMap`, and `TreeMap`.
- **Characteristics**:
    - Stores key-value pairs.
    - `HashMap`: Does not maintain order.
    - `TreeMap`: Sorts keys in natural order.
**Example**:
```java
Map<Integer, String> map = new HashMap<>();
map.put(1, "Apple");
map.put(2, "Banana");
```
---
---
---
### What is Lambda Expression?

A **Lambda Expression** is a feature in Java introduced in **JDK 8** that allows you to write concise, functional-style code. It enables the creation of anonymous methods (i.e., methods without a name) that can be passed as parameters to other methods or used to implement functional interfaces. Lambda expressions simplify the syntax and improve the readability of the code.

**Syntax**:
```java
(parameter1, parameter2, ...) -> expression
```
**Example**:
```java
// Lambda expression to define the implementation of the 'run' method in Runnable
Runnable r = () -> System.out.println("Running...");
r.run();
```
---

### Advantages of Lambda Expressions

1. **Concise Code**: Reduces the boilerplate code required to define an anonymous class.
2. **Improved Readability**: Simplifies the code, making it more readable.
3. **Supports Functional Programming**: Makes it easier to work with functional programming constructs in Java.
4. **Better Use of Collections**: Lambda expressions work seamlessly with the Java Collections Framework, especially with methods like `forEach()`, `map()`, and `filter()`.
5. **Parallel Processing**: Enables easier parallelization, for example, using `Stream` API.

---
### Version Introduced
- Lambda expressions were introduced in **JDK 8**. This was part of the Java 8 release, which also included other features like the **Stream API**, **default methods**, and **Optional**.
---
---
---
### What is a Block Expression?

A **Block Expression** in lambda expressions is used when multiple statements are needed. It is defined using curly braces `{}` and requires an explicit `return` for returning values.

**Example**:
```java
Function<Integer, Integer> square = (x) -> {
    int result = x * x;
    return result;
};
```
---
### What is a Generic Function Interface?

A **Generic Function Interface** is a functional interface that uses generics, allowing flexibility to operate with any data type.

**Example**:
```java
@FunctionalInterface
interface MyFunction<T> {
    T apply(T t);
}

MyFunction<Integer> square = (x) -> x * x;
```
---
### How to Pass Parameters in Lambda Expression Function?

Parameters are passed inside the parentheses before the arrow `->`. The type can be inferred or explicitly specified.

**Example**:
```java
BinaryOperator<Integer> add = (a, b) -> a + b;  // Inferred type
BinaryOperator<Double> multiply = (Double a, Double b) -> a * b;  // Explicit type
```
---
---
---
### How to Implement Exception Handling in Lambda Expression?

In Java, **lambda expressions** don't directly support checked exceptions. However, you can implement exception handling inside lambda expressions using a `try-catch` block or by wrapping the lambda in another method that handles exceptions.

#### 1. **Using Try-Catch Inside Lambda Expression**

You can place a `try-catch` block inside the lambda expression to handle exceptions.
**Example**:
```java
@FunctionalInterface
interface MyFunction {
    void apply() throws Exception;
}

public class Main {
    public static void main(String[] args) {
        MyFunction myFunction = () -> {
            try {
                // Code that might throw an exception
                int result = 10 / 0;  // Division by zero
            } catch (Exception e) {
                System.out.println("Exception caught: " + e.getMessage());
            }
        };
        
        myFunction.apply();  // Output: Exception caught: / by zero
    }
}
```

#### 2. **Handling Checked Exceptions by Wrapping the Lambda**

Since lambdas don’t support checked exceptions directly, you can create a wrapper method or use a custom exception handler.
**Example**:
```java
@FunctionalInterface
interface ThrowingFunction {
    void apply() throws Exception;
}

public class Main {
    public static void main(String[] args) {
        // Wrapper to handle checked exceptions
        ThrowingFunction lambdaWithException = () -> {
            if (true) {
                throw new Exception("Custom Exception");
            }
        };

        // Handling exception
        handleException(lambdaWithException);
    }

    public static void handleException(ThrowingFunction function) {
        try {
            function.apply();
        } catch (Exception e) {
            System.out.println("Handled Exception: " + e.getMessage());
        }
    }
}
```

In this example, the lambda expression is wrapped inside a method that handles checked exceptions.

- Use a `try-catch` block inside the lambda expression for handling exceptions.
- Alternatively, wrap the lambda expression in a method to handle checked exceptions.
---
---
---
### Method References

**Method references** are a shorthand for calling methods directly, without using a lambda expression. There are four types:

1. **Static Method Reference**: Refers to a static method of a class. **Syntax**: `ClassName::methodName` **Example**:
    ```java
    BinaryOperator<Integer> add = Calculator::add;
    ```
    
2. **Instance Method Reference (Specific Object)**: Refers to an instance method of a particular object. **Syntax**: `instance::methodName` **Example**:
    ```java
    Printer printer = new Printer();
    Consumer<String> printerMethod = printer::print;
    printerMethod.accept("Hello!");  // Output: Hello!
    ```
    
3. **Instance Method Reference (Arbitrary Object)**: Refers to an instance method of any object of a particular class. **Syntax**: `ClassName::methodName` **Example**:
    ```java
    List<String> list = Arrays.asList("Apple", "Banana", "Cherry");
    list.forEach(System.out::println);  // Output: Apple, Banana, Cherry
    ```
    
4. **Constructor Reference**: Refers to a constructor to create objects. **Syntax**: `ClassName::new` **Example**:
    ```java
    Supplier<Animal> animalCreator = Animal::new;
    animalCreator.get();  // Output: Animal created!
    ```
---
### Constructor References

**Constructor references** are used to refer to a constructor directly. It is shorthand for creating objects using lambda expressions.

**Syntax**: `ClassName::new`
**Example**:
```java
Supplier<Animal> animalCreator = () -> new Animal("Dog");
animalCreator.get();  // Output: Dog created!

// Simplified constructor reference
Supplier<Animal> animalCreatorRef = Animal::new;
animalCreatorRef.get();  // Output: null created! (constructor requires an argument, so adjust accordingly)
```

- **Method references** refer to methods directly (static, instance, or constructor).
- **Constructor references** are used to create objects directly using a constructor.
---
---
---
### What is Synchronization?

**Synchronization** in Java ensures that only one thread can access a shared resource at a time, preventing data inconsistency and race conditions.
### Purpose:
- To avoid data inconsistency when multiple threads access shared data.
- To ensure that only one thread can execute a synchronized method/block at a time.
### How it Works:
- In Java, synchronization can be achieved by using the `synchronized` keyword.
- When a method or block is marked with `synchronized`, it locks the object or class, and only one thread can execute that synchronized method/block at any given time.
### Types:

1. **Method Synchronization**: Locks the entire method.
    ```java
    synchronized void method() { }
    ```
2. **Block Synchronization**: Locks a specific block of code.
    ```java
    synchronized(this) { }
    ```
### Example:
```java
class Counter {
    private int count = 0;

    synchronized void increment() {
        count++;
    }

    int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();
        t1.join();
        t2.join();
        
        System.out.println("Count: " + counter.getCount());  // Output: 2000
    }
}
```
---
---
---
### 1. **CountDownLatch**

A synchronization tool that allows one or more threads to wait until a set of operations performed by other threads completes.
- **Use Case**: Waiting for threads to finish before continuing.
- **Example**: Main thread waits for other threads to complete their tasks using `await()`.

### 2. **CyclicBarrier**

Synchronizes a set of threads to wait for each other to reach a common point. It can be reused.
- **Use Case**: Multiple threads must wait for each other at a specific point.
- **Example**: Threads perform work and wait at a barrier using `await()`.

### 3. **Semaphore**

Limits the number of threads accessing a resource by maintaining a set of permits.
- **Use Case**: Controlling access to a shared resource with a limit on concurrency.
- **Example**: Limiting access to critical sections using `acquire()` and `release()`.

### 4. **Exchanger**

Allows two threads to exchange objects. Both threads must call `exchange()` to swap data.
- **Use Case**: Two threads exchange data at a synchronization point.
- **Example**: Thread 1 sends data to Thread 2 and receives a reply in return.

### 5. **Phaser**

A flexible synchronization tool for multiple phases of synchronization, allowing threads to wait and proceed in different stages.
- **Use Case**: Multiple phases of synchronization for complex tasks.
- **Example**: Threads synchronize in multiple phases using `arriveAndAwaitAdvance()`.
---
---
---
### Fork/Join Framework in Parallel Programming

The **Fork/Join Framework** in Java is used for parallel execution of tasks, breaking them down into smaller subtasks and running them concurrently to take advantage of multi-core processors. It follows the **divide and conquer** approach, splitting tasks (forking) and combining results (joining).

### Key Components:
1. **ForkJoinPool**: Manages worker threads for parallel task execution.
2. **RecursiveTask**: Used for tasks that return a result.
3. **RecursiveAction**: Used for tasks that do not return a result.

### Working:
- **Fork**: The task is divided into smaller subtasks.
- **Join**: After completion of the subtasks, their results are combined.

### Example:
```java
import java.util.concurrent.RecursiveTask;
import java.util.concurrent.ForkJoinPool;

public class ForkJoinExample {
    static class SumTask extends RecursiveTask<Long> {
        private final long[] array;
        private final int start, end;
        
        SumTask(long[] array, int start, int end) {
            this.array = array;
            this.start = start;
            this.end = end;
        }

        @Override
        protected Long compute() {
            if (end - start <= 10) {
                long sum = 0;
                for (int i = start; i < end; i++) sum += array[i];
                return sum;
            } else {
                int middle = (start + end) / 2;
                SumTask leftTask = new SumTask(array, start, middle);
                SumTask rightTask = new SumTask(array, middle, end);
                leftTask.fork();
                rightTask.fork();
                return leftTask.join() + rightTask.join();
            }
        }
    }

    public static void main(String[] args) {
        long[] array = new long[100];
        for (int i = 0; i < array.length; i++) array[i] = i + 1;

        ForkJoinPool pool = new ForkJoinPool();
        SumTask task = new SumTask(array, 0, array.length);
        long result = pool.invoke(task);
        System.out.println("Sum: " + result);
    }
}
```
---
---
---
