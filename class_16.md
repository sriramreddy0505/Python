        1.  What is a function in Python?
A function is a reusable block of code that performs a particular task.
For example, suppose you want to print "Hello, Python!" five times. Instead of writing print() five times, you can create a function and call it whenever you need it.
Real-life example: A washing machine performs a specific task when you press its start button. Similarly, a Python function performs a task when you call it.

without a function :
print("Hello, Python!")
print("Hello, Python!")
print("Hello, Python!")

with function 
def greet():
    print("Hello, Python!")

greet()
greet()              # greet The name of the function.
greet()
output:
Hello, Python!
Hello, Python!
Hello, Python!

The function allows you to reuse the same code without rewriting it.

   2. What is def in Python?
The def keyword is used to define or create a function in Python.

Important: Defining a function does not automatically execute its body. You normally need to call it using greet().

3. What is my_function()?
my_function is simply an example of a function name. You can choose your own meaningful name, such as greet, calculate_sum, or my_details.
ex:def my_function():
    print("This is my first function")

my_function()
output:This is my first function
ef creates the function.
my_function is the function's name.
The indented print() statement belongs to the function.
my_function() calls the function.
Python executes the statements inside it.
and also u can call the function multiple times like 1
    4. What is return in Python?
The return statement sends a result from a function back to the code that called it.
This is one of the most important concepts in Python functions.

def add():
    return 10 + 20

result = add()
print(result)
output: 30
another ex:
[12]
0s
def multi():
  return 10*30
answer=multi()  
print(answer)
print(answer+10)
300
310
print() displays information on the screen.
return sends a value back to the caller.
A function stops executing when it reaches return.
    5. Returning multiple values
A Python function can return more than one value. You can separate the values with commas.
def student_details():
   name="sriram"
   age=22
   return name, age
result=student_details()
print(result)   
('sriram', 22)
Python returns these values together as a tuple.

6. What is addsub()?
addsub is a custom function name that can be used to perform addition and subtraction.

def addsub(a, b):
    addition = a + b
    subtraction = a - b

    return addition, subtraction
add_result, sub_result = addsub(20, 10)
print("Addition:", add_result)
print("Subtraction:", sub_result)
output:
Addition: 30
Subtraction: 10

 7. What are positional arguments?
A positional argument is a value passed to a function based on its position in the function call.
def student(name,age):
  print("name:", name)
  print("age:", age)
student("ravi", 20)  
name: ravi
age: 20
mainly it can work to the The first argument goes to the first parameter, and the second argument goes to the second parameter.
if we change the order na 
Python does not automatically understand that 21 is an age. It assigns values according to their positions.
Important: Positional arguments can cause mistakes if you pass values in the wrong order.

   What are keyword arguments?
A keyword argument is a value passed to a function by specifying the parameter name.
def student(name, age):
    print("Name:", name)
    print("Age:", age)

student(age=21, name="Ravi")
output:Name: Ravi
Age: 21
so in this Notice that we passed age first and name second. Python assigns the values using their parameter names, so the order does not matter here.
You can also combine them, but positional arguments must come before keyword arguments.

 What are default arguments?
A default argument is a parameter that already has a value assigned in the function definition.
If you do not pass a value for that parameter, Python uses the default value.
def greet(name="Guest"):
    print("Hello,", name)

greet()
greet("Sriram")
output:
Hello, Guest
Hello, Sriram   
explanation:
- name="Guest" sets the default value.
- greet() uses "Guest" because no argument was supplied.
- greet("Sriram") overrides the default and uses "Sriram".


