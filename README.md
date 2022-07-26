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
     
<img width="552" alt="img2" src="https://user-images.githubusercontent.com/78050476/180130695-e88d3b00-39f3-46d0-9650-09929740237f.png">

#### Example     
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
     
 #### output
      There are many types of birds.
      Most of the birds can fly but some cannot.
      There are many types of birds.
      Sparrows can fly.
      There are many types of birds.
      Ostriches cannot fly.

### 4. Inheritance
     Inheritance is the capability of one class to derive or inherit the properties from another class. The class that derives properties is called the derived class or child class and the class from which the properties are being derived is called the base class or parent class.
     
#### The benefits of inheritance are:

   - It represents real-world relationships well.
   - It provides the reusability of a code. We don’t have to write the same code again and again. Also, it allows us to add more features to a class without              modifying it.
   - It is transitive in nature, which means that if class B inherits from another class A, then all the subclasses of B would automatically inherit from class A.
   
### types of inheritance
<img width="267" alt="img3" src="https://user-images.githubusercontent.com/78050476/180131395-b62078e3-578b-441e-8526-223f96f9e317.png">

### I. Single inheritance
      Single inheritance enables a derived class to inherit properties from a single parent class, thus enabling code reusability and the addition of new features   to existing code.
 ### Code:
       class Parent:
       def func1(self):
           print("This function is in parent class.")
        
       class Child(Parent):
       def func2(self):
           print("This function is in child class.")
   
   
 ### II. Multiple inheritance
          When a class can be derived from more than one base class this type of inheritance is called multiple inheritances. In multiple inheritances, all the     features of the base classes are inherited into the derived class.   
 ### Code:
            class Mother:
         mothername = ""
 
         def mother(self):
            print(self.mothername)
           
           class Father:
        fathername = ""
 
         def father(self):
             print(self.fathername)
             
           class Son(Mother, Father):
         def parents(self):
            print("Father :", self.fathername)
            print("Mother :", self.mothername)
            
### III. Multilevel inheritance
      In multilevel inheritance, features of the base class and the derived class are further inherited into the new derived class. This is similar to a    relationship representing a child and a grandfather. 
            
             
### code:
            class Grandfather:
 
            def __init__(self, grandfathername):
                 self.grandfathername = grandfathername
                 
            class Father(Grandfather):
                def __init__(self, fathername, grandfathername):
                    self.fathername = fathername
             Grandfather.__init__(self, grandfathername)
             
            class Son(Father):
                def __init__(self, sonname, fathername, grandfathername):
                    self.sonname = sonname
             Father.__init__(self, fathername, grandfathername)
             
             def print_name(self):
                 print('Grandfather name :', self.grandfathername)
                 print("Father name :", self.fathername)
                 print("Son name :", self.sonname)
### IV. Hierarchical inheritance
     When more than one derived class are created from a single base this type of inheritance is called hierarchical inheritance. In this program, we have a parent (base) class and two child (derived) classes.

### code:
         class Parent:
            def func1(self):
               print("This function is in parent class.")
 

         class Child1(Parent):
             def func2(self):
               print("This function is in child 1.")
 

         class Child2(Parent):
            def func3(self):
               print("This function is in child 2.")
             
  ### V. Hybrid inheritance
       Inheritance consisting of multiple types of inheritance is called hybrid
      
  ### code:
           class School:
               def func1(self):
               print("This function is in school.")
 
 
         class Student1(School):
            def func2(self):
               print("This function is in student 1. ")
 
 
         class Student2(School):
            def func3(self):
            print("This function is in student 2.")
 
 
         class Student3(Student1, School):
            def func4(self):
               print("This function is in student 3.")
             
### 5. Encapsulation
       Encapsulation is one of the fundamental concepts in object-oriented programming (OOP). It describes the idea of wrapping data and the methods that work on   data within one unit. This puts restrictions on accessing variables and methods directly and can prevent the accidental modification of data. 
### code:
          
         class Base:
              def __init__(self):
 
        # Protected member
        self._a = 2
 
        # Creating a derived class
         class Derived(Base):
            def __init__(self):
 
        # Calling constructor of
        # Base class
        Base.__init__(self)
        print("Calling protected member of base class: ",
              self._a)
 
        # Modify the protected variable:
        self._a = 3
        print("Calling modified protected member outside class: ", self._a)
             
### 6. Abstraction
       Abstraction is the concept of object-oriented programming that "shows" only essential attributes and "hides" unnecessary information.
             
             
             
