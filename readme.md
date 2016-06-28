---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class? Class variables (with keyword 'static') are associated with the class rather than the object. It is common to all objects and is in a fixed location in memory. Member variables are for the object. 

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables? Yes it makes sense for a public member variable but not a private variable because the computer will be confused because its contradicting each other. 

3. What are some benefits of making member variables `private`? They are only accessible inside the class they are declared in. Also, no one will be able to use it. You also cannot override private methods. 

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child? Class A is the sub class and class B is the super class. Parent is class B and child is Class A.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class? It means that class is a subclass of the parent class and therefore will have all variables and methods that were declared in the parent class. 

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue? Because you are calling this method in the Main class and because Refrigerator is a subclass of Appliance, the method needs to be in Appliance as well. Thats what casting would solve. 

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class? Yes, if the concrete class is extending an abstract class you do need to implement all methods but you do not need to do that in an abstract class or a normal class that does not extend an abstract class. 

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface? You can delcare any methods in an interface but you cannot implement the methods. You have to implement them in the class. 

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`. You cannot create an instance of an abstract class. You will have to make an instance of a subclass. If you want to call a method that was implemented in the abstract method you need to instantiate the subclass and then call the method. A final class cannot be modified at all. If we have methods in the final class, we can call it but if we have methods in the abstract class, we need to use subclass. 

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?  The child method will override it. 

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful? A list is a type of an ArrayList. You use LinkedList if you have a lot of data that is constantly changing. An Array List is used when the data is mostly concrete and is changed minimally. ArrayList and LinkedList inherit from List so the compiler knows. 

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
