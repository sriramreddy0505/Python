                             1. Decorator with a function argument
Our previous wrapper accepted no arguments. What if the original function needs arguments?
Use *args and **kwargs to support different kinds of function arguments.
             1.Chaining Multiple Decorators
Decorator chaining means applying multiple decorators to the same function.
Each decorator adds its own behavior.

ex: def first_decorator(func):
    def wrapper():
        print("First decorator: Start")
        func()
        print("First decorator: End")
    return wrapper


def second_decorator(func):
    def wrapper():
        print("Second decorator: Start")
        func()
        print("Second decorator: End")
    return wrapper


@first_decorator
@second_decorator
def greet():
    print("Hello!")
    output:
  First decorator: Start
Second decorator: Start
Hello!
Second decorator: End
First decorator: End

and mainly chaining works to the Python applies decorators from the bottom upwards.
When you call greet(), the outer wrapper starts first, then the inner wrapper, then the original function. The messages after the original function run in reverse order.
Important: Decorator order matters because changing the order can change the program's behavior.
                    2.What are decorators with arguments?
A decorator with arguments lets you configure the behavior of a decorator.
For example, you might want to specify how many times a function should run.

     3. What Are Docstrings in Python?
A docstring is a string used to document what a module, class, or function does.
It explains the purpose of your code so that other developers — and your future self — can understand it easily.
A docstring is usually written inside triple quotes:
 """This is a docstring."""
You can access the docstring using the __doc__ attribute.
   4.Errors and Exceptions in Python
   An error is a problem that prevents your program from behaving as intended.
   ex: print(10 / 0)
Python raises:
ZeroDivisionError: division by zero
The program cannot complete that division because division by zero is not defined.
and another ex of error :
number = int("hello")
    5.What is an exception?
An exception is an event that occurs during program execution and interrupts the normal flow of the program.
Python raises exceptions for problems such as:
- Dividing by zero.
- Converting invalid text into a number.
- Accessing a missing dictionary key.
- Opening a file that does not exist.
Exceptions can often be handled so that the program can respond gracefully instead of terminating unexpectedly.
      6.What is exception handling?
Exception handling means detecting and managing exceptions using try, except, else, and finally.
syntax: try:
    # Code that might raise an exception
    pass

except Exception:
    # Handle an exception
    pass
    and explanation:
try: Contains code that might fail.
except: Handles a matching exception.
else: Runs if the try block finishes without an exception.
finally: Runs whether an exception occurs or not, usually for cleanup.

Best practice: Catch specific exceptions instead of using a bare except:. This makes bugs easier to identify and prevents you from accidentally hiding unexpected problems.
     7: Raising an Exception Using raise
     What does raise mean?
The raise keyword allows you to raise an exception deliberately when your program detects an invalid condition.
Python raises some exceptions automatically, but sometimes you need to define your own validation rules.
For example, a person cannot be accepted into an age-restricted service if they do not meet its minimum age requirement.
ex: age = 15

if age < 18:
    raise ValueError("Age must be at least 18")

print("Access granted")
output: ValueError: Age must be at least 18
        8.Raising exceptions to validate data
Let's create a function that validates a bank withdrawal amoun
ex:def withdraw(balance, amount):
    if amount <= 0:
        raise ValueError("Withdrawal must be greater than zero")

    if amount > balance:
        raise ValueError("Insufficient balance")

    return balance - amount


try:
    remaining = withdraw(5000, 6000)
    print("Remaining balance:", remaining)

except ValueError as error:
    print("Transaction failed:", error)
    output:Transaction failed: Insufficient balance
    
    9.What is file handling?
File handling means creating, opening, reading, writing, and closing files using Python.
Files are useful for storing information permanently, even after your program finishes.
Common examples include:
- .txt — text files.
- .csv — comma-separated data.
- .json — structured data.
- .log — application logs.
- .xlsx — Excel workbooks, which typically require a library such as pandas or openpyxl to read their contents.

- Reading an entire file with read()
- Reading one line with readline()
The readline() method reads one line at a time.
Reading all lines with readlines()
The readlines() method returns the lines as a list of strings.
