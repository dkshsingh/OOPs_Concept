# OOPs_Concepts
## Features of Object-Oriented programming
   there are 6 features of object-oriented programming
   1. Class
   2. Object
   3. Abstraction
   4. Polymorphism
   5. Encapsulation
   6. Inheritance
![oops](https://user-images.githubusercontent.com/78050476/180074669-4ac03cd6-1e74-43e7-a105-4c92fbb03fe8.png)

### 1. Class 
    A class is a collection of objects. A class contains the blueprints or the prototype from which the objects are being created. It is a logical entity that contains     some attributes and methods. 
    
#### some points on Python class    
    - classes are created by keyword class.
    - Attributes are the variables that belong to a class.
    - Attributes are always public and can be accessed using the dot (.) operator. Eg.: Myclass.Myattribute
    
### Class  definiton syntax:
    class Classname:
    #statement1
    .
    .
    .
    #statement2
    
    Example:
    class Dog:
        pass
### 2. Object
    The object is an entity that has a state and behavior associated with it. It may be any real-world object like a mouse, keyboard, chair, table, pen, etc. Integers, strings, floating-point numbers, even arrays, and dictionaries, are all objects.
     
 #### an object consists of    
     - State: It is represented by the attributes of an object. It also reflects the properties of an object.
     - Behavior: It is represented by the methods of an object. It also reflects the response of an object to other objects.
     - Identity: It gives a unique name to an object and enables one object to interact with other objects.
### The self
   - Class methods must have an extra first parameter in the method definition. We do not give a value for this parameter when we call the method, Python provides       it
   - If we have a method that takes no arguments, then we still have to have one argument.
   - This is similar to this pointer in C++ and this reference in Java.
### The __init__ method 
    The __init__ method is similar to constructors in C++ and Java. It is run as soon as an object of a class is instantiated. The method is useful to do any initialization you want to do with your object.
    
#### Example:  Creating Class and objects with methods
    code:
     class Dog:
 
    # class attribute
    attr1 = "mammal"
 
    # Instance attribute
    def __init__(self, name):
        self.name = name
         
    def speak(self):
        print("My name is {}".format(self.name))

    Rodger = Dog("Rodger")
    Tommy = Dog("Tommy")
    Rodger.speak()
    Tommy.speak()
    
### 3. polymorphism
     Polymorphism simply means having many forms. For example, we need to determine if the given species of birds fly or not, using polymorphism we can do this          using a single function.
     
code:
    class Bird:
   
    def intro(self):
        print("There are many types of birds.")
 
    def flight(self):
        print("Most of the birds can fly but some cannot.")
 
    class sparrow(Bird):
   
        def flight(self):
            print("Sparrows can fly.")
 
    class ostrich(Bird):
 
        def flight(self):
           print("Ostriches cannot fly.")
 
       obj_bird = Bird()
       obj_spr = sparrow()
       obj_ost = ostrich()
 
       obj_bird.intro()
       obj_bird.flight()
 
       obj_spr.intro()
       obj_spr.flight()
 
       obj_ost.intro()
       obj_ost.flight()
     
     
