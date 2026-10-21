           1. What is a package in Python?
A package is a folder used to organize related Python modules and subpackages.

Think about it like this:
- Folder: A container for files.
- Module: A single Python file (.py).
- Function: A reusable block of code that performs a task.
- Package: A folder that organizes Python modules.
- Subpackage: A package inside another package.

-       2. What is a module?
A module is simply a Python file that contains code, such as variables and functions.

For example, create a file named calculator.py.
def add(a, b):  
return a + b
def subtract(a, b):  
return a - b
Here:
- calculator.py is the module.
- add() is a function.
- subtract() is another function.
- a and b are parameters.
 
You can use these functions from another Python file.
Create main.py in the same folder:
import calculatorprint(calculator.add(10, 5))print(calculator.subtract(10, 5))
Output:
15
5
Remember: A module is one Python file. A package is used to organize modules into folders.

       3. How to create a package and a folder
Let's create a package called mypackage.
You can do this in VS Code, or in another folder on your computer .
and step by step is 
python_project/
├── main.py
└── mypackage/
    ├── __init__.py
    ├── calculator.py
    └── greetings.py

    and using of pakage is 
    code:
from mypackage.calculator import add, multiply
from mypackage.greetings import say_hello

print(add(10, 20))
print(multiply(5, 4))
print(say_hello("Sriram"))

Run the program
Open the terminal in the python_project folder and run:
python main.py.
and then output is 
30
20
Hello, Sriram!

The __init__.py file can be empty. It traditionally marks a directory as a regular Python package and can also contain package initialization code. Modern Python also supports namespace packages without it.


    4. How to create a function inside a package
    
A function is a reusable block of code defined using the def keyword.

For example, inside mypackage/calculator.py:
def square(number):    
 return number * number
 def cube(number):    
 return number * number * number              # 16 an d27
 
Now use those functions in main.py:
from mypackage.calculator import square, cube
print(square(4))print(cube(3))
Output:
16
27

and mainly it can be worked to the 1. from identifies where the code is located.
2. mypackage.calculator identifies the module inside the package.
3. import square, cube imports the functions you want to use.
4. square(4) calls the square function with 4.
5. cube(3) calls the cube function with 3.
You don't need to copy the function code into main.py. You can reuse it by importing it.

  5. What is a subpackage?
A subpackage is a package inside another package. It helps organize a large project into smaller sections.
For example, imagine a company application that has separate modules for employees and payments.
Here is the folder structure:

ex: main.py 
from company.employees.details import employee_name, employee_id
from company.payments.salary import calculate_salary

print(employee_name())
print(employee_id())
print(calculate_salary(30000, 5000))
output:
Sriram
101
35000
