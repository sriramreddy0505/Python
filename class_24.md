                     1. What is a class in Python?
A class is a blueprint or template used to create objects.
For example, imagine you want to create details for 100 sheep. Every sheep has a name, age, and weight. 
Instead of writing separate code for every sheep, you can create one class and use it to create many objects.
syntax: class ClassName:
    # Attributes
    # Methods
    pass

    2. What is an object?
An object is an instance of a class.
The class is the blueprint, and the object is an actual item created from that blueprint
      ex:
      class Sheep:
    pass

sheep1 = Sheep()
sheep2 = Sheep()

print(sheep1)
print(sheep2)
output:
<__main__.Sheep object at 0x...>
<__main__.Sheep object at 0x...>

The memory addresses will differ.

Understanding the code
- Sheep() creates a new object.
- sheep1 refers to the first object.
- sheep2 refers to the second object.
- Both objects are created from the same class, but they are separate objects.

   3. What are attributes?
Attributes are variables that store information about a class or an object.
For a sheep, attributes could include its name, age, weight, and price.
There are two important types of attributes:
- Instance attributes
- Class attributes

- ex: instance atributes code
class sheep:
  def __init__ (self, weight,colour, age, name):
      self.age=age
      self.name=name
      self.colour=colour
      self.weight=weight
sheep1=sheep(25, "red",2,"black sheep")
print(sheep1.age)
print(sheep1.colour)
print(sheep1.weight)
print(sheep1.name)

#output
2
red
25
black sheep

Remember: Instance attributes can have different values for different objects.
              4. What are methods?
A method is a function defined inside a class. It describes an action that an object or class can perform.
For example, a sheep-related class might have methods to display its details or calculate its estimated value.
 ex: #method
class sheep:
  def show_details(self):
    print("this is a good sheep and healthy sheep")

 def eat(self):
    print("this sheep can eat its own way ") 

sheep1=sheep()
sheep1.show_details()
sheep1.eat()
output:
this is a good sheep and healthy sheep
this sheep can eat its own way 

- show_details() is a method.
- eat() is a method.
- sheep1 is the object calling those methods.


    5. What is the __init__() method?
The __init__() method is a special method that Python calls automatically when a new object is initialized.
It is commonly used to assign initial values to an object's attributes.
What does self mean?
self refers to the current object on which an instance method is operating.
ex:  class Student:
    def __init__(self, name):
        self.name = name

student1 = Student("Ravi")
student2 = Student("Priya")

print(student1.name)
print(student2.name)
output:
Ravi
Priya

When student1 is initialized, self refers to student1. When student2 is initialized, self refers to student2.
Important: self is a convention, not a reserved keyword, but you should use it for normal instance methods.

           6. What is a constructor in Python?
A constructor is the mechanism used to create an object. In Python, __new__() is responsible for creating the object, while __init__() initializes the newly created object.
For beginner-level Python, you will often hear __init__() informally called the constructor because it is where you typically initialize attributes.

ex:class Employee:
    def __init__(self):
        print("Employee object initialized")

employee1 = Employee()
# Employee object initialized
When Employee() is called, Python creates the object and automatically calls __init__() to initialize it.
You generally do not need to define __new__() in everyday Python programs.
                           7. What is a parameterized constructor?
A parameterized constructor, commonly called a parameterized initializer in Python, accepts arguments so you can give each object different initial values.
 class Employee:
    def __init__(self, name, salary, department):
in name, salary, department are parameters 
Without a parameterized initializer, you would have to assign the attributes separately or use some other initialization approach.
                     8. What is a class variable?
A class variable is defined inside the class but outside its instance methods. It is associated with the class and can be accessed through the class itself or through its instances.
Use class variables for information shared by all instances, such as a company name.
 and company is a class variable.
 name is an instance variable.
 Both employees can access the shared company name.

     9. What is an instance method?
An instance method works with an individual object. It takes self as its first parameter by convention and can read or modify that object's attributes.
          10. What is a static method?
A static method is a function placed inside a class that does not automatically receive the instance (self) or class (cls) as its first argument.
You define it using the @staticmethod decorator.
Use a static method when the operation logically belongs to the class but does not need instance-specific or class-specific data.
ex: class Calculator:
    @staticmethod
    def add(a, b):
        return a + b

    @staticmethod
    def multiply(a, b):
        return a * b

print(Calculator.add(10, 20))
print(Calculator.multiply(5, 4))
output:
30
20


          
