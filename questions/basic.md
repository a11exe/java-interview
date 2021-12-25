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
+ [11. Describe the Collections Type Hierarchy. What Are the Main Interfaces, and What Are the Differences Between Them?](#11-describe-the-collections-type-hierarchy-what-are-the-main-interfaces-and-what-are-the-differences-between-them)
+ [12. Describe Various Implementations of the Map Interface and Their Use Case Differences.](#12-describe-various-implementations-of-the-map-interface-and-their-use-case-differences)
+ [13. Explain the Difference Between Linkedlist and Arraylist.](#13-explain-the-difference-between-linkedlist-and-arraylist)
+ [14. What Is the Difference Between Hashset and Treeset?](#14-what-is-the-difference-between-hashset-and-treeset)
+ [15. How Is Hashmap Implemented in Java?](#15-how-is-hashmap-implemented-in-java)
+ [16. What Is the Purpose of the Initial Capacity and Load Factor Parameters of a Hashmap?](#16-what-is-the-purpose-of-the-initial-capacity-and-load-factor-parameters-of-a-hashmap)
+ [17. Describe Special Collections for Enums.](#17-describe-special-collections-for-enums)
+ [18. What Is the Difference Between Fail-Fast and Fail-Safe Iterators?](#18-what-is-the-difference-between-fail-fast-and-fail-safe-iterators)
+ [19. How Can You Use Comparable and Comparator Interfaces to Sort Collections?](#19-how-can-you-use-comparable-and-comparator-interfaces-to-sort-collections)
+ [20. What is Serialization in Java?](#20-what-is-serialization-in-java)
+ [21. Concept of Java Cloning](#21-concept-of-java-cloning)
+ [22. StringBuffer vs StringBuilder](#22-stringbuffer-vs-stringbuilder)
+ [23. Name some of the parsers which are commonly used to parse XML documents](#23-name-some-of-the-parsers-which-are-commonly-used-to-parse-xml-documents)
+ [24. What New Features Were Added in Java 8?](#24-what-new-features-were-added-in-java-8)
+ [25. What New Features Were Added in Java 11?](#25-what-new-features-were-added-in-java-11)
+ [26. What Is a Lambda Expression and What Is It Used For?](#26-what-is-a-lambda-expression-and-what-is-it-used-for)
+ [27. What Is an Exception?](#27-what-is-an-exception)
+ [28. How to Generate OutOfMemoryError and StackOverflowException?](#28-how-to-generate-outofmemoryerror-and-stackoverflowexception)
+ [29. What Are Annotations? What Are Their Typical Use Cases?](#29-what-are-annotations-what-are-their-typical-use-cases)
+ [30. What is immutable class?](#30-what-is-immutable-class)

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

[back to the table of contents](#basic-java-interview-questions)

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
   
[back to the table of contents](#basic-java-interview-questions)
   
## 3. What are different access modifiers in Java?
+ **Default** access modifier is without any access specifier data members, class and methods, and are accessible within the same package.
+ **Private** access modifiers are marked with the keyword private, and are accessible only within class, and not even accessible by class from the same package.
+ **Protected** access modifiers can be accessible within the same package or subclasses from different packages.
+ **Public** access modifiers are accessible from everywhere.

[back to the table of contents](#basic-java-interview-questions)

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

[back to the table of contents](#basic-java-interview-questions)

## 5. What are primitive data types?

+ byte - 1 byte (8 bits). Min -2^7 Max 2^7-1
+ short - 2 byte (16 bits). Min -2^15 Max 2^15-1
+ char - 2 byte (16 bits). 2^16-1
+ int - 4 byte (32 bits). Min -2^31-1 Max 2^31
+ long - 8 byte (64 bits). Min -2^63-1 Max 2^63
+ float - 4 byte (32 bits). Min -2^31-1 Max 2^31
+ double - 8 byte (64 bits). Min -2^63-1 Max 2^63
+ boolean - NA usualy 1 byte

[back to the table of contents](#basic-java-interview-questions)

## 6. Order of execution of Initialization blocks and Constructors in Java.

+ Static initialization blocks will run whenever the class is loaded first time in JVM
+ Initialization blocks run in the same order in which they appear in the program.
+ Instance Initialization blocks are executed whenever the class is initialized and before constructors are invoked. 
They are typically placed above the constructors within braces.

[back to the table of contents](#basic-java-interview-questions)

## 7. Differences between Lambda Expressions and Closures in Java.
Java supports lambda expressions but not the Closures. 
A lambda expression is an anonymous function and can be defined as a parameter. 
The Closures are like code fragments or code blocks that can be used without being a method or a class. 
It means that Closures can access variables not defined in its parameter list and also assign it to a variable.

[back to the table of contents](#basic-java-interview-questions)

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

[back to the table of contents](#basic-java-interview-questions)

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

[back to the table of contents](#basic-java-interview-questions)

## 10. Explain object finalization

Called by the garbage collector on an object when garbage collection determines that 
there are no more references to the object. If an object can not be accessed from any live object, 
this means that it can be safely garbage collected.

[back to the table of contents](#basic-java-interview-questions)

## 11. Describe the Collections Type Hierarchy. What Are the Main Interfaces, and What Are the Differences Between Them?

The **Iterable** interface represents any collection that can be iterated using the for-each loop. 
The **Collection** interface inherits from Iterable and adds generic methods for checking if an element is in a collection, adding and removing elements from the collection, determining its size etc.

The List, Set, and Queue interfaces inherit from the Collection interface.

+ **List** is an ordered collection, and its elements can be accessed by their index in the list.
+ **Set** is an unordered collection with distinct elements, similar to the mathematical notion of a set.
+ **Queue** is a collection with additional methods for adding, removing and examining elements, 
useful for holding elements prior to processing.
+ **Map** interface is also a part of the collection framework, yet it does not extend Collection. 
This is by design, to stress the difference between collections and mappings which are hard to gather 
under a common abstraction. The Map interface represents a key-value data structure with unique keys and no more 
than one value for each key.

[back to the table of contents](#basic-java-interview-questions)

## 12. Describe Various Implementations of the Map Interface and Their Use Case Differences.

One of the most often used implementations of the Map interface is the **HashMap**. 
It is a typical hash map data structure that allows accessing elements in constant time, or O(1), 
but does not preserve order and is not thread-safe.

To preserve insertion order of elements, you can use the **LinkedHashMap** class which extends 
the HashMap and additionally ties the elements into a linked list, with foreseeable overhead.

The **TreeMap** class stores its elements in a red-black tree structure, 
which allows accessing elements in logarithmic time, or O(log(n)). 
It is slower than the HashMap for most cases, but it allows keeping the elements in order according to some Comparator.

The **ConcurrentHashMap** is a thread-safe implementation of a hash map. 
It provides full concurrency of retrievals (as the get operation does not entail locking) and high expected concurrency of updates.

The **Hashtable** class has been in Java since version 1.0. It is not deprecated but is mostly considered obsolete. 
It is a thread-safe hash map, but unlike ConcurrentHashMap, all its methods are simply synchronized, 
which means that all operations on this map block, even retrieval of independent values.

[back to the table of contents](#basic-java-interview-questions)

## 13. Explain the Difference Between Linkedlist and Arraylist.

**ArrayList** is an implementation of the List interface that is based on an array. 
ArrayList internally handles resizing of this array when the elements are added or removed. 
You can access its elements in constant time by their index in the array. 
However, inserting or removing an element infers shifting all consequent elements which may be slow if the array 
is huge and the inserted or removed element is close to the beginning of the list.

**LinkedList** is a doubly-linked list: single elements are put into Node objects 
that have references to previous and next Node. This implementation may appear more efficient than ArrayList 
if you have lots of insertions or deletions in different parts of the list, especially if the list is large.

In most cases, however, ArrayList outperforms LinkedList. Even elements shifting in ArrayList, 
while being an O(n) operation, is implemented as a very fast System.arraycopy() call. 
It can even appear faster than the LinkedList‘s O(1) insertion which requires instantiating a Node object and updating 
multiple references under the hood. LinkedList also can have a large memory overhead due to a creation 
of multiple small Node objects.

[back to the table of contents](#basic-java-interview-questions)

## 14. What Is the Difference Between Hashset and Treeset?

Both HashSet and TreeSet classes implement the Set interface and represent sets of distinct elements. 
Additionally, TreeSet implements the NavigableSet interface. 
This interface defines methods that take advantage of the ordering of elements.

**HashSet** is internally based on a HashMap, and **TreeSet** is backed by a TreeMap instance, 
which defines their properties: HashSet does not keep elements in any particular order. 
Iteration over the elements in a HashSet produces them in a shuffled order. 
TreeSet, on the other hand, produces elements in order according to some predefined Comparator.

[back to the table of contents](#basic-java-interview-questions)

## 15. How Is Hashmap Implemented in Java?

The HashMap class represents a typical hash map data structure with certain design choices.

The HashMap is backed by a resizable array that has a size of power-of-two. 
When the element is added to a HashMap, first its hashCode is calculated (an int value). 
Then a certain number of lower bits of this value are used as an array index. 
This index directly points to the cell of the array (called a bucket) where this key-value pair should be placed. 
Accessing an element by its index in an array is a very fast O(1) operation, which is the main feature of a hash map structure.

A hashCode is not unique, however, and even for different hashCodes, we may receive the same array position. 
This is called a collision. There is more than one way of resolving collisions in the hash map data structures. 
In Java's HashMap, each bucket actually refers not to a single object, but to a red-black tree of all objects 
that landed in this bucket (prior to Java 8, this was a linked list).

So when the HashMap has determined the bucket for a key, it has to traverse this tree to put the key-value pair 
in its place. If a pair with such key already exists in the bucket, it is replaced with a new one.

To retrieve the object by its key, the HashMap again has to calculate the hashCode for the key, 
find the corresponding bucket, traverse the tree, call equals on keys in the tree and find the matching one.

HashMap has O(1) complexity, or constant-time complexity, of putting and getting the elements. 
Of course, lots of collisions could degrade the performance to O(log(n)) time complexity in the worst case, 
when all elements land in a single bucket. This is usually solved by providing a good hash function with a uniform distribution.

When the HashMap internal array is filled (more on that in the next question), 
it is automatically resized to be twice as large. This operation infers rehashing (rebuilding of internal data structures), 
which is costly, so you should plan the size of your HashMap beforehand.

[back to the table of contents](#basic-java-interview-questions)

## 16. What Is the Purpose of the Initial Capacity and Load Factor Parameters of a Hashmap?

The initialCapacity argument of the HashMap constructor affects the size of the internal data structure of the HashMap, 
but reasoning about the actual size of a map is a bit tricky. The HashMap‘s internal data structure is an array with 
the power-of-two size. So the initialCapacity argument value is increased to the next power-of-two 
(for instance, if you set it to 10, the actual size of the internal array will be 16).

The load factor of a HashMap is the ratio of the element count divided by the bucket count (i.e. internal array size). 
For instance, if a 16-bucket HashMap contains 12 elements, its load factor is 12/16 = 0.75. 
A high load factor means a lot of collisions, which in turn means that the map should be resized to the next power of two. 
So the loadFactor argument is a maximum value of the load factor of a map. 
When the map achieves this load factor, it resizes its internal array to the next power-of-two value.

The initialCapacity is 16 by default, and the loadFactor is 0.75 by default, so you could put 12 elements in a HashMap 
that was instantiated with the default constructor, and it would not resize. 
The same goes for the HashSet, which is backed by a HashMap instance internally.

Consequently, it is not trivial to come up with initialCapacity that satisfies your needs. 
This is why the Guava library has Maps.newHashMapWithExpectedSize() and Sets.newHashSetWithExpectedSize() methods 
that allow you to build a HashMap or a HashSet that can hold the expected number of elements without resizing.

[back to the table of contents](#basic-java-interview-questions)

## 17. Describe Special Collections for Enums.

**EnumSet** and **EnumMap** are special implementations of Set and Map interfaces correspondingly. 
You should always use these implementations when you're dealing with enums because they are very efficient.

An EnumSet is just a bit vector with “ones” in the positions corresponding to ordinal values of enums present in the set. 
To check if an enum value is in the set, the implementation simply has to check if the corresponding bit 
in the vector is a “one”, which is a very easy operation. 
Similarly, an EnumMap is an array accessed with enum's ordinal value as an index. In the case of EnumMap, 
there is no need to calculate hash codes or resolve collisions.

[back to the table of contents](#basic-java-interview-questions)

## 18. What Is the Difference Between Fail-Fast and Fail-Safe Iterators?

Iterators for different collections are either fail-fast or fail-safe, 
depending on how they react to concurrent modifications. 
The concurrent modification is not only a modification of collection from another thread but also modification from 
the same thread but using another iterator or modifying the collection directly.

+ **Fail-fast** iterators (those returned by HashMap, ArrayList, and other non-thread-safe collections) 
iterate over the collection's internal data structure, and they throw ConcurrentModificationException 
as soon as they detect a concurrent modification.
+ **Fail-safe** iterators (returned by thread-safe collections such as ConcurrentHashMap, CopyOnWriteArrayList) 
create a copy of the structure they iterate upon. 
They guarantee safety from concurrent modifications. Their drawbacks include excessive memory consumption and iteration 
over possibly out-of-date data in case the collection was modified.

[back to the table of contents](#basic-java-interview-questions)

## 19. How Can You Use Comparable and Comparator Interfaces to Sort Collections?

The Comparable interface is an interface for objects that can be compared according to some order. 
Its single method is compareTo, which operates on two values: the object itself and the argument object of the same type. 
For instance, Integer, Long, and other numeric types implement this interface. 
String also implements this interface, and its compareTo method compares strings in lexicographical order.

The Comparable interface allows to sort lists of corresponding objects with the Collections.sort() method 
and uphold the iteration order in collections that implement SortedSet and SortedMap. 
If your objects can be sorted using some logic, they should implement the Comparable interface.

The Comparable interface usually is implemented using natural ordering of the elements. 
For instance, all Integer numbers are ordered from lesser to greater values. 
But sometimes you may want to implement another kind of ordering, for instance, to sort the numbers in descending order. 
The Comparator interface can help here.

The class of the objects you want to sort does not need to implement this interface. 
You simply create an implementing class and define the compare method which receives 
two objects and decides how to order them. You may then use the instance of this class to override the natural ordering 
of the Collections.sort() method or SortedSet and SortedMap instances.

[back to the table of contents](#basic-java-interview-questions)

## 20. What is Serialization in Java?

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

[back to the table of contents](#basic-java-interview-questions)

## 21. Concept Of Java Cloning

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

[back to the table of contents](#basic-java-interview-questions)

## 22. StringBuffer vs StringBuilder

StringBuffer is synchronized, StringBuilder is not. 
StringBuilder is faster than StringBuffer because it's not synchronized.

[back to the table of contents](#basic-java-interview-questions)

## 23. Name some of the parsers which are commonly used to parse XML documents.

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

[back to the table of contents](#basic-java-interview-questions)

## 24. What New Features Were Added in Java 8?

Java 8 ships with several new features, but the most significant are the following:

+ Lambda Expressions − a new language feature allowing us to treat actions as objects
+ Method References − enable us to define Lambda Expressions by referring to methods directly using their names
+ Optional − special wrapper class used for expressing optionality
+ Functional Interface – an interface with maximum one abstract method; implementation can be provided using a Lambda Expression
+ Default methods − give us the ability to add full implementations in interfaces besides abstract methods
+ Nashorn, JavaScript Engine − Java-based engine for executing and evaluating JavaScript code
+ Stream API − a special iterator class that allows us to process collections of objects in a functional manner
+ Date API − an improved, immutable JodaTime-inspired Date API

[back to the table of contents](#basic-java-interview-questions)

## 25. What New Features Were Added in Java 11?

Java 11 ships with several new features, but the most significant are the following:

+ New methods to the String class: isBlank, lines, strip, stripLeading, stripTrailing, and repeat.
+ New File Methods − readString and writeString static methods from the Files class.
+ The new HTTP client − improves overall performance and provides support for both HTTP/1.1 and HTTP/2
+ Modular System – since Java 9

[back to the table of contents](#basic-java-interview-questions)

## 26. What Is a Lambda Expression and What Is It Used For?

In very simple terms, a lambda expression is a function that we can reference and pass around as an object.

Moreover, lambda expressions introduce functional style processing in Java, and facilitate 
the writing of compact and easy-to-read code.

As a result, lambda expressions are a natural replacement for anonymous classes such as method arguments. 
One of their main uses is to define inline implementations of functional interfaces.

[back to the table of contents](#basic-java-interview-questions)

## 27. What Is an Exception?

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

[back to the table of contents](#basic-java-interview-questions)

## 28. How to Generate OutOfMemoryError and StackOverflowException?

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
[back to the table of contents](#basic-java-interview-questions)

## 29. What Are Annotations? What Are Their Typical Use Cases?

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

[back to the table of contents](#basic-java-interview-questions)

## 30. What is immutable class?

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

[back to the table of contents](#basic-java-interview-questions)
