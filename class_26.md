              1. What is polymorphism in Python?
The word polymorphism has two parts:
- Poly = many
- Morphism = forms
So, polymorphism means one interface or method name can be used in different forms to perform different actions.
Real-world example
Think about the speak() action:
- A dog barks.
- A cat meows.
- A cow moos.
- For example, a payment application can use a common pay() operation for credit cards, UPI and digital wallets.
ex:
  class Dog:
    def speak(self):
        print("Dog barks")
class Cat:
    def speak(self):
        print("Cat meows")
class Cow:
    def speak(self):
        print("Cow moos")
dog = Dog()
cat = Cat()
cow = Cow()

dog.speak()
cat.speak()
cow.speak()
output:
Dog barks
Cat meows
Cow moos

     2. What is method overriding?
Method overriding happens when a child class provides its own implementation of a method already defined in its parent class.
It is commonly used to achieve runtime polymorphism.
Real-world example
Suppose a parent class defines a general work() method. Different employees can perform different kinds of work.
 Why use method overriding?
- To customize inherited behavior.
- To allow different child classes to behave differently.
- To implement specialized behavior without rewriting the entire parent class.

 Method overriding is a feature in which a subclass provides a new implementation of an inherited method, using the same method name and a compatible signature.
           3. What is method overloading?
Method overloading means using the same method name for different parameter lists or different numbers/types of arguments.
 In languages such as Java, you can define several methods with the same name but different parameter lists. Python does not support traditional method overloading in the same way. 
 If you define the same method name multiple times in one class, the last definition replaces the earlier ones.
 
Why traditional overloading does not work in Python
 ex:
 class Calculator:
    def add(self, a, b):
        return a + b

    def add(self, a, b, c):
        return a + b + c
calc = Calculator()
print(calc.add(10, 20, 30))  # 60


   Why use operator overloading?
   Operator overloading defines what operators do for custom objects.
- To make custom objects easier to work with.
- To make mathematical classes, such as vectors and matrices, intuitive.
- To define meaningful comparisons between objects.
Important: Operator overloading should have a sensible meaning. In a real financial application, for example, you should carefully define how currencies and different account types can be combined.

 5. What is duck typing?
Duck typing means Python focuses on what an object can do rather than strictly checking its class or type.
The common expression is:
If it walks like a duck and quacks like a duck, treat it like a duck.
In programming, if an object provides the method or behavior your code needs, you can often use it without requiring it to belong to a particular class.
            Why use duck typing?
- It makes code flexible.
- It allows unrelated classes to work with the same function.
- It reduces the need for strict inheritance relationships.
- It is common in Python's file handling, iterables and other object interfaces.

    6. What is abstraction in Python?
Abstraction means exposing essential functionality while hiding unnecessary implementation details.
You use abstraction every day without needing to understand how the internal system works.
per ex: When you withdraw money from an ATM:
1. You insert your card.
2. You enter your PIN.
3. You select an amount.
4. You receive money if the transaction is approved.
You do not need to understand how the bank verifies your account, communicates with its server, checks your balance or updates its database.
The ATM exposes the operations you need while hiding much of the internal process.
That is the central idea of abstraction.


 How do we implement abstraction in Python?
Python provides the abc module, which supports abstract base classes.

The two important tools are:
- ABC — a base class for defining an abstract interface.
- @abstractmethod — marks a method that concrete subclasses must implement.
