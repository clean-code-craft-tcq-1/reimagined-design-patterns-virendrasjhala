# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.
<!------------------------------------------------------------------------Desing Patterns-------------------------------------------------------------------------------------->	


1. Builder Design Pattern:

Problem statement:

There are 3 cars (Tesla, Honda, Jaguar), if we want to check funtionality like (Stering, Wheels, Gear, Air bag, Auto brake, padestrian detection)
* Points: 
	1. some functionalities are mandatory (Stering, Wheels, Gear) and some optional ( Air bag, Auto brake, padestrian detection) for some cars.
	2. if we want to cover all the functionalities then we need to create saparate calsses with specification leads to hight complexity or interdepandancy. 
	
Solution statement:
	1. we can create object of the subject class like car and pass the object of car to the other car companies(Tesla, Honda, Jaguar) object to check the depandancies with one builder class    which will take care of all the specification Interfaces for class car.
	
Advantages:
	1. Builder design pattern allow us to manage complexity by build complex objects step by step.
	2. useful in creating objects with many optional properties.
	3. managiable code as the number of oject increases for the same functionality.
	
Disadvantages:
	1. redundent code.
	2. no reusability of code.
	3. any change in concrete class leads to change in builder class.

<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->	

2. Observer Desing Pattern:

Problem statment:

suppose there is sell on amazon.com and we want to buy one mobile and for that every day we check if the mobile is available or not.
* Points:
	1. we can check everyday on the website.

Solution statement:
	1. Instead of going every time on the website we can register once for remainder notification if the product is available or not.
	2. we can create one observer for the subject(observable) which will inform or nofity to other depandent objects(observers) if there is any change in subject(observable).
	
Advantages:
	1. There is no need to modigy subject if we want to add or remove obervers.
	2. It creates one to many depandancy so depandent objects never miss the subject depandent task.
	3. It provides decoupling between subject and observer.

Disadvantages:
	1. other concreteobservers have to implement the interface of observer if not implemented then can create issues.
	2. memory misuse becaus of the pointer because the registratin and deregistration.
	
<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->	

3. State Design Pattern:

Problem statment:

Suppose we want to apply for loan in bank and there are three types(Silver, gold, platinum), we can get the loan bassed on the amount available in the our bank account.

Solution statement:
	1. we can create state class and its object behaviour depands on the amount available in the bank means if the amount sufficient to take silver type then state object will 
	   point towards the silver class loan requirment documents and vise versa.
	2. we can create specific indepandent state also in case client is already running with some other parallel loan.
	
Advantages:
	1. reduces conditional complexity means remove the much more use of if-else stament with object behaviour.
Disadvantages:
	1. large code means code increases as the state transition and methods increase.
	
<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->	

4. Prototype Desing Pattern:

Problem statment:

Suppose we created chess game and initialized all the objects (setup for king, queen... etc) but in between if some one wants to start new game then again we have to initialize
all the required objects.This will repeat for each new game start request. 

Solution statement:
we will intialize all the required objects(intial setup before start), now we will clone the object because if someone request for new game play then we can again start
from the initial(first) stage.

Advantages:
	1. objects are clone so no need to initialize object again.
	2. cloned object is not class depandent.

Disadvantages:
	1. more use can leads to perfomance issue.
<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->	





