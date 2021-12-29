# Basic Java Interview Questions

+ [1. What is Java? What are the features of Java?](#1-what-is-java-what-are-features-of-java)
+ [2. What are the OOPs concepts?](#2-what-are-the-oops-concepts)
+ [3. What are different access modifiers in Java?](#3-what-are-different-access-modifiers-in-java)
+ [4. What is the meaning of SOLID?](#4-what-is-the-meaning-of-solid)
+ [5. What are primitive data types?](#5-what-are-primitive-data-types)
+ [6. Order of execution of Initialization blocks and Constructors in Java](#6-order-of-execution-of-initialization-blocks-and-constructors-in-java)
+ [7. Differences between Lambda Expressions and Closures in Java?](#7-differences-between-lambda-expressions-and-closures-in-java)
+ [8. Give the list of Java Object class methods](#8-give-the-list-of-java-object-class-methods)
+ [9. What is the difference between atomic, volatile, synchronized?](#9-what-is-the-difference-between-atomic-volatile-synchronized)
+ [10. Explain object finalization](#10-explain-object-finalization)
+ [11. What is Serialization in Java?](#11-what-is-serialization-in-java)
+ [12. Concept of Java Cloning](#12-concept-of-java-cloning)
+ [13. StringBuffer vs StringBuilder](#13-stringbuffer-vs-stringbuilder)
+ [14. Name some of the parsers which are commonly used to parse XML documents](#14-name-some-of-the-parsers-which-are-commonly-used-to-parse-xml-documents)
+ [15. What New Features Were Added in Java 8?](#15-what-new-features-were-added-in-java-8)
+ [16. What New Features Were Added in Java 11?](#16-what-new-features-were-added-in-java-11)
+ [17. What Is a Lambda Expression and What Is It Used For?](#17-what-is-a-lambda-expression-and-what-is-it-used-for)
+ [18. What Is an Exception?](#18-what-is-an-exception)
+ [19. How to Generate OutOfMemoryError and StackOverflowException?](#19-how-to-generate-outofmemoryerror-and-stackoverflowexception)
+ [20. What Are Annotations? What Are Their Typical Use Cases?](#20-what-are-annotations-what-are-their-typical-use-cases)
+ [21. What is immutable class?](#21-what-is-immutable-class)

## 1. What is Java. What are features of Java?
Java is a high-level programming language and is platform-independent.
+ Java is also an object-oriented language. However, everything (except fundamental types) is an object in Java
+ Platform independent: A single program works on different platforms without any modification.
+ High Performance: JIT (Just In Time compiler) enables high performance in Java. 
JIT converts the bytecode into machine language and then JVM starts the execution.
+ Multi-threaded. We can write Java programs that deal with many tasks at once by defining multiple threads.
+ Java doesn't support multiple inheritance through class. It can be achieved by interfaces in java.
+ Secured: Java is secured because it doesn't use explicit pointers.
+ Java is a strong programming language as it uses strong memory management. The concepts like Automatic garbage collection.

[back to the top](#basic-java-interview-questions)

## 2. What are the OOPs concepts?
OOPs concepts include:
+ **Inheritance** 
    + Inheritance means one class can extend to another class. 
    So that the codes can be reused from one class to another class. 
    The existing class is known as the Super class whereas the derived class is known as a sub class.
    Inheritance is only applicable to the public and protected members only. Private members can’t be inherited.
+ **Encapsulation**
    + Protects the code from others.
      Code maintainability.
      For encapsulation, we need to make all the instance variables private and create setter and getter for those variables. 
      Which in turn will force others to call the setters rather than access the data directly.
+ **Polymorphism**
    + A single object can refer to the super-class or sub-class depending on the reference type which is called polymorphism.
    Polymorphism is applicable for overriding
+ **Abstraction**
    + Abstraction in object-oriented programming means hiding complex internals but to expose only 
    essential characteristics and behavior with respect to context.
+ **Interface**
    + Multiple inheritances cannot be achieved in java. To overcome this problem the Interface concept is introduced.
   An interface is a template which has only method declarations and not the method implementation.
   
[back to the top](#basic-java-interview-questions)
   
## 3. What are different access modifiers in Java?
+ **Default** access modifier is without any access specifier data members, class and methods, and are accessible within the same package.
+ **Private** access modifiers are marked with the keyword private, and are accessible only within class, and not even accessible by class from the same package.
+ **Protected** access modifiers can be accessible within the same package or subclasses from different packages.
+ **Public** access modifiers are accessible from everywhere.

[back to the top](#basic-java-interview-questions)

## 4. What is the meaning of SOLID?
Solid represents five principles of java which are:

+ **S**: Single responsibility principle. One class should have only one and only responsibility.
+ **O**: Open-closed principle. Software components should be open for extension, but closed for modification. 
Hence, the browser is a perfect example of functionality that is open for extension but is closed for modification.
+ **L**: Liskov substitution principle. Types must be completely substitutable for their base types.
+ **I**: Interface segregation principle. 
Clients should not be forced to implement unnecessary methods which they will not use.
+ **D**: Dependency inversion principle. it depends on abstractions not on concretions. 
According to it, the high-level module must never rely on any low-level module.
You go to a local store to buy something, and you decide to pay for it by using your debit card. 
So, when you give your card to the clerk for making the payment, 
the clerk doesn’t bother to check what kind of card you have given.
The type of credit card or debit card that you have for paying does not even matter; they will simply swipe it.

[back to the top](#basic-java-interview-questions)

## 5. What are primitive data types?

+ byte - 1 byte (8 bits). Min -2^7 Max 2^7-1
+ short - 2 byte (16 bits). Min -2^15 Max 2^15-1
+ char - 2 byte (16 bits). 2^16-1
+ int - 4 byte (32 bits). Min -2^31-1 Max 2^31
+ long - 8 byte (64 bits). Min -2^63-1 Max 2^63
+ float - 4 byte (32 bits). Min -2^31-1 Max 2^31
+ double - 8 byte (64 bits). Min -2^63-1 Max 2^63
+ boolean - NA usualy 1 byte

[back to the top](#basic-java-interview-questions)

## 6. Order of execution of Initialization blocks and Constructors in Java.

+ Static initialization blocks will run whenever the class is loaded first time in JVM
+ Initialization blocks run in the same order in which they appear in the program.
+ Instance Initialization blocks are executed whenever the class is initialized and before constructors are invoked. 
They are typically placed above the constructors within braces.

[back to the top](#basic-java-interview-questions)

## 7. Differences between Lambda Expressions and Closures in Java.
Java supports lambda expressions but not the Closures. 
A lambda expression is an anonymous function and can be defined as a parameter. 
The Closures are like code fragments or code blocks that can be used without being a method or a class. 
It means that Closures can access variables not defined in its parameter list and also assign it to a variable.

[back to the top](#basic-java-interview-questions)

## 8. Give the list of Java Object class methods.

+ clone() - Creates and returns a copy of this object.
+ equals() - Indicates whether some other object is "equal to" this one.
+ finalize() - Called by the garbage collector on an object when garbage collection determines that there are 
no more references to the object.
+ getClass() - Returns the runtime class of an object.
+ hashCode() - Returns a hash code value for the object.
+ notify() - Wakes up a single thread that is waiting on this object's monitor.
+ notifyAll() - Wakes up all threads that are waiting on this object's monitor.
+ toString() - Returns a string representation of the object.
+ wait() - Causes current thread to wait until another thread invokes the notify() method 
or the notifyAll() method for this object.

[back to the top](#basic-java-interview-questions)

## 9. What is the difference between atomic, volatile, synchronized?

It basically reads value from memory, increments it and puts back to memory. 
This works in single thread but nowadays, in the era of multi-core, multi-CPU, multi-level caches it won't work correctly. 
First of all it introduces race condition (several threads can read the value at the same time), 
but also visibility problems. The value might only be stored in "local" CPU memory (some cache) and not be visible 
for other CPUs/cores (and thus - threads).
**Volatile**
Declaring a variable as volatile means that modifying its value immediately affects the actual memory storage 
for the variable. The compiler cannot optimize away any references made to the variable. 
This guarantees that when one thread modifies the variable, all other threads see the new value immediately.

**AtomicInteger** 
```java
private AtomicInteger counter = new AtomicInteger();

public int getNextUniqueIndex() {
  return counter.getAndIncrement();
}
```
The AtomicInteger class uses CAS (compare-and-swap) low-level CPU operations (no synchronization needed!) 
Declaring an atomic variable guarantees that operations made on the variable occur in an atomic fashion, 
i.e., that all of the substeps of the operation are completed within the thread they are executed and 
are not interrupted by other threads.

**Synchronizing**
all accesses to a variable allows only a single thread at a time to access the variable, 
and forces all other threads to wait for that accessing thread to release its access to the variable.

Synchronization occurs on an object. This means that calling a synchronized method of a class will lock the this object of the call. Static synchronized methods will lock the Class object itself.

Likewise, entering a synchronized block requires locking the this object of the method.

Synchronized access to a variable is usually implemented using a monitor or semaphore. 
These are low-level mutex (mutual exclusion) mechanisms that allow a thread to acquire control 
of a variable or block of code exclusively, forcing all other threads to wait if they also attempt to acquire the same mutex.

This means that a synchronized method (or block) can be executing in multiple threads at the same time if they are 
locking on different objects, but only one thread can execute a synchronized method (or block) 
at a time for any given single object.

[back to the top](#basic-java-interview-questions)

## 10. Explain object finalization

Called by the garbage collector on an object when garbage collection determines that 
there are no more references to the object. If an object can not be accessed from any live object, 
this means that it can be safely garbage collected.

[back to the top](#basic-java-interview-questions)

## 11. What is Serialization in Java?

Object Serialization in Java is a process used to convert Object into a binary format which can be persisted into 
a disk or sent over the network to any other running Java virtual machine; 
the reverse process of creating object from the binary stream is called deserialization in Java. 
Java provides Serialization API for serializing and deserializing object which includes java.io.Serializable, 
java.io.Externalizable, ObjectInputStream and ObjectOutputStream etc. 

Serializable is marker interface.Marker interface in Java is interfaces with no field or methods or in 
simple word empty interface in java is called marker interface.

Making a class Serializable in Java is very easy, Your Java class just needs to implements java.io.Serializable 
interface and JVM will take care of serializing objects in the default format.

If you don't explicitly declare SerialVersionUID then JVM generates it based upon the structure of class 
which depends upon interfaces a class implements and several other factors which is subject to change

serialVersionUID is used to ensure that same class(That was used during Serialization) is loaded during 
Deserialization.serialVersionUID is used for version control of object.

You can customize Serialization process by defining writeObject and readObject method.

To avoid serialization some variable, you can mark that variable as either static or transient.

Externalizable interface has more control over serialization process and it is mandatory 
to override writeExternal and readExternal.

[back to the top](#basic-java-interview-questions)

## 12. Concept Of Java Cloning

Java supports two type of cloning: - Deep and shallow cloning. By default shallow clone is used in Java. 
Object class has a method clone() which does shallow cloning. Shallow copies duplicate as little as possible. 
The memory usage is lower.
1) If the class has only primitive data type members then a completely new copy of the object will be created 
and the reference to the new object copy will be returned.
2) If the class contains members of any class type then only the object references to those members are copied 
and hence the member references in both the original object as well as the cloned object refer to the same object.

In deep copy is the copy of object itself. A new memory is allocated for the object and contents are copied.
When a deep copy of the object is done new references are created.
One solution is to simply implement your own custom method (e.g., deepCopy()) that returns 
a deep copy of an instance of one of your classes. 
Other common solution to the deep copy problem is to use Java Object Serialization.

[back to the top](#basic-java-interview-questions)

## 13. StringBuffer vs StringBuilder

StringBuffer is synchronized, StringBuilder is not. 
StringBuilder is faster than StringBuffer because it's not synchronized.

[back to the top](#basic-java-interview-questions)

## 14. Name some of the parsers which are commonly used to parse XML documents.

+ **Dom** Parser - Parses the document by loading the complete contents of the document and creating its complete 
hiearchical tree in memory. Using DOM parser, we can parse, modify or create a XML document.                           
+ **SAX** Parser - Parses the document on event based triggers. 
Does not load the complete document into the memory. You are processing a very large XML document 
whose DOM tree would consume too much memory. We have no random access to an XML document since it is processed 
in a forward-only manner. Using SAX parser, we can only parse or modify a XML document.
+ **StAX** Parser - Parses the document in similar fashion to SAX parser does,
but StAX is a PULL API where as SAX is a PUSH API. It means in case of StAX parser, 
client application need to ask StAX parser to get information from XML whenever 
it needs but in case of SAX parser, client application is required to get information 
when SAX parser notifies the client application that information is available.
Using StAX parser, we can parse, modify and create a XML document.

[back to the top](#basic-java-interview-questions)

## 15. What New Features Were Added in Java 8?

Java 8 ships with several new features, but the most significant are the following:

+ Lambda Expressions − a new language feature allowing us to treat actions as objects
+ Method References − enable us to define Lambda Expressions by referring to methods directly using their names
+ Optional − special wrapper class used for expressing optionality
+ Functional Interface – an interface with maximum one abstract method; implementation can be provided using a Lambda Expression
+ Default methods − give us the ability to add full implementations in interfaces besides abstract methods
+ Nashorn, JavaScript Engine − Java-based engine for executing and evaluating JavaScript code
+ Stream API − a special iterator class that allows us to process collections of objects in a functional manner
+ Date API − an improved, immutable JodaTime-inspired Date API

[back to the top](#basic-java-interview-questions)

## 16. What New Features Were Added in Java 11?

Java 11 ships with several new features, but the most significant are the following:

+ New methods to the String class: isBlank, lines, strip, stripLeading, stripTrailing, and repeat.
+ New File Methods − readString and writeString static methods from the Files class.
+ The new HTTP client − improves overall performance and provides support for both HTTP/1.1 and HTTP/2
+ Modular System – since Java 9

[back to the top](#basic-java-interview-questions)

## 17. What Is a Lambda Expression and What Is It Used For?

In very simple terms, a lambda expression is a function that we can reference and pass around as an object.

Moreover, lambda expressions introduce functional style processing in Java, and facilitate 
the writing of compact and easy-to-read code.

As a result, lambda expressions are a natural replacement for anonymous classes such as method arguments. 
One of their main uses is to define inline implementations of functional interfaces.

[back to the top](#basic-java-interview-questions)

## 18. What Is an Exception?

An exception is an abnormal event that occurs during the execution of a program 
and disrupts the normal flow of the program's instructions.
The throws keyword is used to specify that a method may raise an exception during its execution.
The throw keyword allows us to throw an exception object to interrupt the normal flow of the program.
We can handle exception by using a try-catch-finally statement.
The block of code in which an exception may occur is enclosed in a try block. This block is also called “protected” or “guarded” code.
If an exception occurs, the catch block that matches the exception being thrown is executed, if not, all catch blocks are ignored.
The finally block is always executed after the try block exits, whether an exception was thrown or not inside it.
A checked exception must be handled within a try-catch block or declared in a throws clause; 
whereas an unchecked exception is not required to be handled nor declared.
An exception is an event that represents a condition from which is possible to recover, 
whereas error represents an external situation usually impossible to recover from.

[back to the top](#basic-java-interview-questions)

## 19. How to Generate OutOfMemoryError and StackOverflowException?

OutOfMemoryError
```java
List<long[]> list = new LinkedList<long[]>();
while (true) {
  list.add(new long[65536]); // an arbitrary number
  // sleep(1) perhaps?
}
```
StackOverflowException
```java
public class StackOverflowErrorExample {

    public static void recursivePrint(int num) {
        System.out.println("Number: " + num);

        if(num == 0)
            return;
        else
            recursivePrint(++num);
    }

    public static void main(String[] args) {
        StackOverflowErrorExample.recursivePrint(1);
    }
}
```
[back to the top](#basic-java-interview-questions)

## 20. What Are Annotations? What Are Their Typical Use Cases?

Annotations are metadata bound to elements of the source code of a program and have no effect on the operation of the code they operate.

Their typical uses cases are:
+ Information for the compiler – with annotations, the compiler can detect errors or suppress warnings
+ Compile-time and deployment-time processing – software tools can process annotations and generate code, configuration files, etc.
+ Runtime processing – annotations can be examined at runtime to customize the behavior of a program

Annotations are a form of an interface where the keyword interface is preceded by @, and whose body contains annotation type element declarations that look very similar to methods:
```java
public @interface SimpleAnnotation {
    String value();

    int[] types();
}
```
After the annotation is defined, yon can start using it in through your code:
```java
@SimpleAnnotation(value = "an element", types = 1)
public class Element {
    @SimpleAnnotation(value = "an attribute", types = { 1, 2 })
    public Element nextElement;
}
```

[back to the top](#basic-java-interview-questions)

## 21. What is immutable class?

Immutable objects are those objects whose state can not be changed once created. 
Class whose objects possess this characteristic can be termed as immutable class.
For example : String , Integer.
Immutable classes are thread safe because you can not change state of immutable objects, 
so even if two thread access immutable object in parallel, it won’t create any issue.

To create an immutable class in java, you have to do following steps.
+ Declare the class as final so it can’t be extended.
+ Make all fields private so that direct access is not allowed.
+ Don’t provide setter methods for variables
+ Make all mutable fields final so that it’s value can be assigned only once.
+ Initialize all the fields via a constructor performing deep copy.
+ Perform cloning of objects in the getter methods to return a copy rather than returning the actual object reference.

[back to the top](#basic-java-interview-questions)
