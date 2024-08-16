# QC Questions that may be asked

## Java Basics
* What is Java? / Why Java?
 

* What is JRE / JDK / JVM?


* What is an object / class?
 

* What is the root class from which every class extends?

* What are the primitive data types in Java?
 

* Where are Strings stored?
 

* Explain stack vs heap?
 

* What are annotations?
 

* What is a POJO? What is a bean?
 

* How can you force garbage collection in Java?
 

* Why are strings immutable in java?


* What is the difference between `String`, `StringBuilder`, and `StringBuffer`?
 

* What are the access modifiers in Java? Explain them.
 

* What are the non-access modifiers in Java?
  

* What is the difference between `static` and `final` variables?


* What are the default values for all data types in Java?


* What is a wrapper class?
 

* What is autoboxing?
 

* Is Java pass-by-value or pass-by-reference?


* What makes a class immutable?


* If two objects are equal, do they have the same hashcode? If not equal?
  

* What data types are supported in switch statements?
 

* List all non-access modifiers?


* How to pass multiple values with a single parameter into a method?
 
  
*  Can we access static/non-static variables from static/non-static methods (see example)?

<br>

```java
public class A {
  public static int x = 1;
  public int y = 2;

  public static void doStuff() {
    System.out.println(y);
  }

  public void doMoreStuff() {
    System.out.println(x);
  }
}
```
<br>

* What is static block?
 

* What is static imports?
 

* What methods are available in the Object class?
 

* How would you clone an object?


* What is the difference between `==` and `.equals()`?
 

* What is an enhanced for loop and what is a `forEach` loop?
 

* What are 3 usages of `super` keyword?
 
  
  <br>
  
## OOP (Freebie)
* What are the 4 pillars of OOP / Explain each?
  * **Abstraction** - Hiding implementation details
  * **Polymorphism** - Subclasses of a class can define their own unique behaviors and yet share some of the same functionality of the parent class. An object can also be referenced by its supertype "parent" class, for example `ParentClass obj = new SubClass()`;
  * **Inheritance** - A class that is derived from another class is called a subclass (also a derived class, extended class, or child class). The class from which the subclass is derived is called a superclass (also a base class or a parent class).
  * **Encapsulation** can be described as a protective barrier that prevents the code and data being randomly accessed by other code defined outside the class. Access to the data and code is tightly controlled by an interface.

* Is this allowed? Is this an example of method overloading or overriding?
  * Overriding. This is an example of covariant return types: a method is allowed to return objects that are child classes of the return type. Also, when overriding a method, the return type of the new method can be a child class of the original return type

<br>

```java
public abstract class Super {
  public abstract Collection getCollection();
}

public abstract class Sub extends Super {
  public abstract List getCollection();
}
```

<br>

* What is the difference between an abstract class and an interface?
  * An abstract class can have both concrete and abstract methods whereas an interface must have only abstract methods if any (unless the default keyword is used). Interface methods are implicitly public and abstract, interface variables are implicitly public, static, and final, but these do not apply in abstract classes. Neither can be instantiated

* What are the implicit modifiers for interface variables?
 

* What is the difference between method overloading and overriding?
  * Method overriding - In a subclass when one declares an identical method from the superclass, this method overrides the one in the superclass.
  * Method overloading - Within the same class when one declares more than method with the same name but different signature (parameters).

* Can you overload / override a main method? static method? a private method? a default method? a protected method?
  * Main method - overload, cannot override b/c is static method.
  * Static method - overload, cannot override b/c belongs to class (not inherited).
  * Private method - overload, cannot override b/c doesn't get inherited.
  * Default method - both.
  * Protected method - both (override if inherited). 

*  Explain the difference

<br>

```java
List<String> mylist = new ArrayList<>();
ArrayList<String> list2 = new ArrayList<>();
```

<br>

* Difference between extends and implements?
  

* What are enumerations (enums)?


* What are the implicit modifiers for interface variables / methods?
 

* First line of constructor?
 

* Can you instantiate this class? Why or why not?
```java
public class Hello {

}
```

<br>

## Collections / Generics
* What are collections in Java?
  

* What are the interfaces in the Collections API?


* What is the difference between a `Set` and a `List`?
 

* What is the difference between a `Array` and an `ArrayList`?
 

* What is the difference between `ArrayList` and `Vector`?
 

* What is the difference between `TreeSet` and `HashSet`?
 

* What is the difference between HashTable and HashMap?
 

* Are Maps in the Collections API?
 

* What happens here?

<br>

```java
List<String> mylist = new ArrayList<>();
mylist.add("hello");
mylist.add(new Person()); // what happens?
```
<br>

* What are generics? What is the diamond operator (`<>`)?
  * A way of specifying a type within a data structure - they enforce type safety. `<>` operator lets you infer generic types from the LHS of assignment operation

<br>

## Exceptions
* What is the difference between `final`, `.finalize()`, and `finally`?
  * `final`: final keyword can be used for class, method and variables. A final class cannot be subclassed and it prevents other programmers from subclassing a secure class to invoke insecure methods. A final method can't be overridden. A final variable can't change from its initialized value.
  * `finalize()`: finalize method is used just before an object is destroyed and called just prior to garbage collection.
  * `finally`: finally, a key word used in exception handling, creates a block of code that will be executed after a `try/catch` block has completed and before the code following the `try/catch` block. The `finally` block will execute whether or not an exception is thrown. For example, if a method opens a file upon exit, then you will not want the code that closes the file to be bypassed by the exception-handling mechanism. This finally keyword is designed to address this contingency.

* `throw` vs `throws` vs `Throwable`?
  

* What is try-with-resources? What interface must the resource implement to use this feature?
 

* Do you need a catch block? Can have more than 1? Order of them?


* What is base class of all exceptions? 
 

* List some checked and unchecked exceptions?


* Multi-catch block - can you catch more than one exception in a single catch block?
 

* Is this an example of a checked or unchecked exception?
```java
public class MyException extends RuntimeException {}
```

<br>

## JUnit
* What is JUnit?
 

* What is TDD?


* What are the annotations in JUnit? Order of execution?
  

* Give an example of a test case?
  

<br>


## IO / Serialization (Freebie)
* How do you serialize / deserialize an object in Java?
  * Step 1: An object is marked serializable by implementing the `java.io.Serializable` interface, which signifies to the underlying API that the object can be flattened into bytes and subsequently inflated in the future.
  * Step 2: The next step is to actually persist the object. That is done with the `java.io.ObjectOutputStream` class. That class is a filter stream--it is wrapped around a lower-level byte stream (called a node stream) to handle the serialization protocol for us. Node streams can be used to write to file systems or even across sockets. That means we could easily transfer a flattened object across a network wire and have it be rebuilt on the other side!
  * To restore the object back, you use `ObjectInputStream.readObject()` method call. The method call reads in the raw bytes that we previously persisted and creates a live object that is an exact replica of the original. Because `readObject()` can read any serializable object, a cast to the correct type is required. With that in mind, the class file must be accessible from the system in which the restoration occurs. In other words, the object's class file and methods are not saved; only the object's state is saved.
