# java interview questions (basic)

+ [1. What is Java? What are the features of Java?](#1-what-is-java-what-are-features-of-java)
+ [2. What are the OOPs concepts?](#2-what-are-the-oops-concepts)
+ [3. What are different access modifiers in Java?](#3-what-are-different-access-modifiers-in-java)
+ [4. What is the meaning of SOLID?](#4-what-is-the-meaning-of-solid)

## 1 What is Java. What are features of Java.
Java is a high-level programming language and is platform-independent.
+ Java is also an object-oriented language. However, everything (except fundamental types) is an object in Java
+ Platform independent: A single program works on different platforms without any modification.
+ High Performance: JIT (Just In Time compiler) enables high performance in Java. 
JIT converts the bytecode into machine language and then JVM starts the execution.
+ Multi-threaded. We can write Java programs that deal with many tasks at once by defining multiple threads.
+ Java doesn't support multiple inheritance through class. It can be achieved by interfaces in java.
+ Secured: Java is secured because it doesn't use explicit pointers.
+ Java is a strong programming language as it uses strong memory management. The concepts like Automatic garbage collection.

## 2 What are the OOPs concepts
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
   
## 3 What are different access modifiers in Java
+ **Default** access modifier is without any access specifier data members, class and methods, and are accessible within the same package.
+ **Private** access modifiers are marked with the keyword private, and are accessible only within class, and not even accessible by class from the same package.
+ **Protected** access modifiers can be accessible within the same package or subclasses from different packages.
+ **Public** access modifiers are accessible from everywhere.

## 4 What is the meaning of SOLID
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