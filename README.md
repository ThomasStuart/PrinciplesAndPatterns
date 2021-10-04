# Programming Principles && Design Patterns 

### UML review
arrows always point to the direction of dependency.  objDependent -> obj

### Principles:
0.)  Dont Repeat Yourself (DRY)

*The following principles make up the SOLID acronym*

1.)  Single Responsibility Principle <a name="SRP"></a>

2.)  Open Closed Principle 

3.)  Liskov Substitution Principle 

4.)  Interface Segregation Principle 

5.)  Dependency Inversion Principle 


 
### Single Responsibility Principle
[SRP](#SRP)
A class should have one and only one reason to change / purpose .   Following SRP will lead to high cohesion (degree to which elements inside a class belong together).  Thus the class will be (1) more readable (2) easier to change (3) easier to test


<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png" alt="bad example" height="300" width="400"/>

The reason the employee class violates SRP is due to the fact that if we change anything about the object, multiple functions will have to be changed within the same class. 

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/validSRP.png" alt="good example" height="300" width="600"/>

Decoupling the employee class and creating SRP classes allows for an application that can change cleaner and faster.

### Open Closed Principle
Software Modules should be open for extension and closed for modification.  The key point in this principle is to allow adding new functionality easily but without changing existing code. Often times inheritance and interfaces are used to achieve this.  
