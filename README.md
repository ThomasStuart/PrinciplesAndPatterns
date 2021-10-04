# Programming Principles && Design Patterns 

### UML review
arrows always point to the direction of dependency.  objDependent -> obj

### Principles:
0.)  Dont Repeat Yourself (DRY)

*The following principles make up the SOLID acronym*

1.)  [Single Responsibility Principle](#single-responsibility-principle)

2.)  Open Closed Principle 

3.)  Liskov Substitution Principle 

4.)  Interface Segregation Principle 

5.)  Dependency Inversion Principle 

### Patterns:

*behavioral patterns*

1.)  [Observer](#observer)

2.)  [Builder](#builder)

3.)  [Factory](#factory)

4.)  [Singleton](#singleton)

 
### Single Responsibility Principle
A class should have one and only one reason to change / purpose .   Following SRP will lead to high cohesion (degree to which elements inside a class belong together).  Thus the class will be (1) more readable (2) easier to change (3) easier to test


<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png" alt="bad example" height="300" width="400"/>

The reason the employee class violates SRP is due to the fact that if we change anything about the object, multiple functions will have to be changed within the same class. 

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/validSRP.png" alt="good example" height="300" width="600"/>

Decoupling the employee class and creating SRP classes allows for an application that can change cleaner and faster.

### Open Closed Principle
Software Modules should be open for extension and closed for modification.  The key point in this principle is to allow adding new functionality easily but without changing existing code. Often times inheritance and interfaces are used to achieve this.  


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
Builder - is a creational design pattern that lets you construct complex objects step by step. The pattern allows you to produce different types and representations of an object using the same construction code.

*do not mistaken this for the telescopic constructor*</br>
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderTelescopic.png" alt="builder tele" height="400" width="600"/>

*Important to note that you cannot build on after the object is created unless setters are included*

#### builder method candidate

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderBadExample.png" alt="builder bad" height="300" width="500"/>

##### Real world examples

1.) Vehicle Class</br>
<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/builderRWE1.png" alt="builder RWE 1" height="300" width="300"/>

### Factory

### Singleton