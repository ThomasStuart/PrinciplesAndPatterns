# Programming Principles && Design Patterns 


### Principles:
0.)  Dont Repeat Yourself (DRY)

1.)  Single Responsibility Principle 

2.)  Open Closed Principle 

3.)  Liskov Substitution Principle 

4.)  Interface Segregation Principle 

5.)  Dependency Inversion Principle 

### UML review
arrows always point to the direction of dependency.  objDependent -> obj
 
#### Single Responsibility Principle
A class should only have a single reason to CHANGE.  

![bad example](https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png)

<img src="https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png" alt="drawing" height="200" width="200"/>

![good example](https://github.com/ThomasStuart/PrinciplesAndPatterns/blob/master/images/violatesSRP.png)

Employee DAO (Data Access Object) is responsibile for the database.  