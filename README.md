# Programming Principles && Design Patterns 

### Principles:
0.)  Dont Repeat Yourself (DRY)

*The following principles make up the SOLID acronym*

1.)  [Single Responsibility Principle](#single-responsibility-principle)

2.)  [Open Closed Principle](#open-closed-principle)

3.)  [Liskov Substitution Principle](#liskov-substitution-principle) 

4.)  [Interface Segregation Principle](#interface-segregation-principle)

5.)  [Dependency Inversion Principle](#dependency-inversion-principle)

### Patterns:
1.)  [Observer](#observer)

2.)  [Builder](#builder)

3.)  [Factory](#factory)

4.)  [Singleton](#singleton)

### quick UML review
arrows always point to the direction of dependency.  objDependent -> obj

### Single Responsibility Principle
**A class should have one and only one reason to change / purpose.**   Following SRP will lead to high cohesion (degree to which elements inside a class belong together).  Thus the class will be (1) more readable (2) easier to change (3) easier to test


<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png" alt="bad example" height="300" width="400"/>

The reason the employee class violates SRP is due to the fact that if we change anything about the object, multiple functions will have to be changed within the same class. 

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/validSRP.png" alt="good example" height="400" width="900"/>

Decoupling the employee class and creating SRP classes allows for an application that can change cleaner and faster.



### Open Closed Principle
**Software Modules should be open for extension and closed for modification.**  The key point in this principle is to allow adding new functionality easily but without changing existing code. Often times inheritance and interfaces are used to achieve this.  


### Liskov Substitution Principle 
**Objects of the superclass shall be replacebale with objects of its subclass without breaking the application.**

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/liskovThumbnail.png" alt="liskov thumb" height="600" width="900"/>

##### Real world examples

1.) Birds and extending with fly feature

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/liskovE1.png" alt="liskov e1" height="400" width="800"/>

2.) Shapes ( Square and Rect)
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/liskovE2.png" alt="liskov e2" height="400" width="800"/>

##### Quiz questions
We have a class called Animals. A method called move() is defined in this Animal class. We also have 2 child classes that extend the Animal class. The child classes are, Boat, and Car. Since both Boat and Car have the capability of moving, the liskov substitution principle is not being violated. False

We have a class called ElectronicDevice. There is one method defined in this class called turnOffDevice(). We also have 2 sub-classes that extend the ElectronicDevice class. These child classes are Television, and Laptop. So far there is no apparent violation of the Liskov Substitution Principle.  True.



### Interface Segregation Principle
**States that no client should be forced to depend on methods it does not use.**

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/IspThumbnail.png" alt="isp thumb" height="600" width="600"/>

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/IspGood.png" alt="isp e1" height="900" width="500"/>

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/IspBad.png" alt="isp e1" height="900" width="500"/>



### Dependency Inversion Principle 
**The principle states:**</br>
1. **High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).**
2. **Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.**

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/dipThumbnail.png" alt="dip thumb" height="600" width="600"/>

* Dependency Injection is an implementation of Dependency Inversion Principle.
* One of the ways to achieve Open-Close Principle is to use Dependency Inversion Principle.
* High-level modules in DIP are modules that appear on the higher part of the UML diagram and depends on the abstraction layer. Abstractions are the ones in the center of the diagram. Low-level modules are the ones in the lower level of the diagram and are the actual implementations of the abstraction layer.

### Observer
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/observerThumbnail.png" alt="observer thumb" height="600" width="600"/>

Observer Pattern – is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods (usually called notify).

##### general UML diagram

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/observerUML.png" alt="observer UML" height="300" width="600"/>

##### Real world examples

1.) employee management system
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/observerRWE1.png" alt="observer RWE 1" height="600" width="800"/>

2.) coffee shop
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/observerRWE2.png" alt="observer RWE 2" height="600" width="800"/>

### Builder
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderThumbnail.png" alt="builder thumb" height="600" width="600"/>
Builder - is a creational design pattern that lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.</br>

*do not mistaken this for the telescopic constructor*</br>
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderTelescopic.png" alt="builder tele" height="300" width="900"/>

*Important to note that you cannot build on after the object is created unless setters are included*

#### builder method candidate

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderBadExample.png" alt="builder bad" height="300" width="500"/>

##### Real world examples

1.) Vehicle Class</br>
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderRWE1.png" alt="builder RWE 1" height="300" width="300"/>

### Factory

Factory (creational design pattern) – useful when we want to use another class to crate objects for us.  Client does not need to know the details and delegates the creation to another class.</br></br>

##### factory structure 

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/factoryUML.png" alt="factory UML" height="600" width="900"/>

##### Real world examples

1.) Vehicle Engine factory </br>
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/factoryRWE1.png" alt="factory RWE 1" height="400" width="800"/>

### Singleton
Singleton - is a creational design pattern that lets you ensure that a class has only one instance, while providing a global access point to this instance.  Don’t want the constructor to be public as we want to restrict the client from creating multiple objects. </br></br>

##### singleton structure 

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/singletonStructure.png" alt="singleton RWE 1" height="400" width="500"/>