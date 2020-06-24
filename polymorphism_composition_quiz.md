# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the **_word_** 'polymorphism' mean?

It is a Greek word meaning “many forms” or strictly speaking “many” and “change”. This occurs when you have multiple classes related to one (or more if using interfaces) parents. It is one of the four pillars of OO alongside Encapsulation, Abstraction and Inheritance.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

In Java an object has the ability to take many forms. A PaintingBuyer and a CarBuyer are both buyers for specific items. You could great an abstract parent class called Buyer and have the two children inherit from it. It could have a method called “public double buyItem(double itemPrice)” that takes in a double of item price and returns the amount of money the buyer has left after buying that item. Bother classes could inherit that method from their parent and override it to give different outcomes for instance the car buyer could add a discount to the purchase in the return statement so you have 1 an identically called method giving back different responses.

3. What can we use to implement polymorphism in Java?

Interfaces and Abstract classes can be used to implement this. You could use a parent class but its generally better practice to use a variety of class you’d never want to instantiate.

4. How many 'forms' can an object take when using polymorphism?

There are in theory an unlimited amount of forms an object can take.

5. Give an example of when you could use polymorphism.

If you have multiple classes doing incredibly similar things you’d want the methods put either in an abstract or interface class then have the child classes extend or implement them. Whilst you can have as many interfaces as you like they can’t have properties. Java forbids multiple inheritance however interfaces and polymorphism is the safer way of utilizing the advantages of multiple inheritance that exist in some other languages.

# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

Composition is a question of does the Class “Has A” nature relevant to a specific Class rather than Inheritance where a Class “Is A” child of specific class. A dog Is An animal, A dog Has A master.

7. When would you use composition? Provide a simple example in Java.

If you had a Car class you would have an Engine class that a Car class would have since ALL cars have engines. You could then reuse the Engine class for other things that have engines such as motorbikes providing your engine class was generic enough (eg all engines have names and fuel holding amounts).

8. What is/are the advantage(s) of using composition?

Your code is a great deal more scalable; you can add more and more features among common Classes. Unlike inheritance you don’t have to worry about providing features for numerous subclasses that won’t be relevant to them where they to inherit them from a parent.

With composition you are implementing the SOLID principal of Dependency Inversion.
So high-level modules should not depend on low-level modules. Both should depend on abstractions and abstractions should not depend on details. Details should depend on abstractions. Were it the other way round changes to a low level class would utterly ruin the parent.

Any class can behave as if it is any of its super classes as well as follow its own but a super class can’t behave the way its children behave.

9. When an object is destroyed, what happens to all the objects it is composed of?

They get destroyed as well and eventually get picked up by Java’s garbage collection (the fate of any object that is no longer referenced anywhere).
