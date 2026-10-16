   1. Mutable objects and append()
 A mutable object is an object whose contents can be changed after it is created.
For example, a Python list is mutable. You can add, remove, or modify its items without creating a new list.

ex:
numbers = [10, 20, 30]
numbers.append(40)
print(numbers)
output:
[10, 20, 30, 40]
The append() method adds one item at the end of a list.

       2.Mutable objects inside functions
 this is important when working with functions.
 ex:
 def add_item(items):
    items.append("Python")

languages = ["Java", "C"]
add_item(languages)
print(languages)
output: ['Java', 'C', 'Python']

Why did the original list change?
The function parameter items refers to the same list object as languages. Therefore, appending an item inside the function changes the original list.

and mainly a function can modify a mutable object passed to it.
Remember: Mutable means the object can be modified. It does not mean the variable itself can never be reassigned.

      2. Variable-length arguments — *args
Sometimes, we don't know how many values a user will pass to a function.
For example, you might want to add two numbers today, five numbers tomorrow, or ten numbers later.
Python allows this using *args.
ex:
def student(*args):
     print(args)
student(10,20,30,40)
student(365,563,6)    
(10, 20, 30, 40)
(365, 563, 6) 
explanation :*args accepts any number of positional arguments.
Inside the function, args is a tuple.
The name args is conventional; the * is what matters.

            Using *args to calculate a sum;
       ex:
def add_numbers(*args):
  total=0
  for number in args:
   total=total+ number
  return total
print(add_numbers(10,20,30))
print(add_numbers(12,44,55))  
60
111     

Using normal parameters with *args;
You can combine regular parameters and variable-length arguments.
ex:
def student_marks(name, *marks):
  print("student:", name)
  print("marks:", marks)

student_marks("ram", 10,20,30,40)
student: ram                  #in this ex can accept to the lot of marks because of we put the "*" other wise this not accepted
marks: (10, 20, 30, 40)
Here, "Ram" is assigned to name, and the remaining positional arguments are collected into marks.
mainly we can Use it when a function should accept a flexible number of positional values.

3. Keyword variable-length arguments — **kwargs

Keyword arguments pass values using parameter names.
ex:
def student(name, age):
  print(name)
  print(age)
student("ravi", 21)  
ravi
21
             and  What is **kwargs?
Sometimes, you don't know which or how many named values will be supplied. Python's **kwargs collects extra keyword arguments into a dictionary.
ex:
def values(**kwargs):
  print(kwargs)
values(name="ram", age=27, job="software")  
{'name': 'ram', 'age': 27, 'job': 'software'}
and mainly **kwargs collects keyword arguments.
kwargs is a dictionary inside the function.
Each argument name becomes a dictionary key.
                               # mainly *args (Collects extra positional arguments into a tuple)
                               #**kwargs (Collects extra keyword arguments into a dictionary)
4. Scope and lifetime of a variable
These two concepts are very important for understanding Python functions.
   What is scope?
Scope means the part of a program where a variable can be accessed by its name.
ex:
name="ravi"

def show():
  message="hello"
  print(name)
  print(message)
show()  
  
ravi
hello
explain:
name is a global variable, accessible inside the function.
message is a local variable, accessible inside greet().

What is the lifetime of a variable?
Lifetime means how long a variable or its associated object remains available during program execution.
ex: def show():
    number = 100
    print(number)

show()
output: 100

The local name number is available while the function executes. When the function returns, that local name is no longer accessible from outside the function.
Important: the object itself may continue to exist if another reference keeps it alive.


What is a local variable?

A local variable is a variable defined inside a function. Normally, it can be accessed only inside that function.
ex: def show():
  message="hello"
  print(message)
show()  
  
hello
and here is a local variable 
and it is always include in the inside scope  Because age belongs to the local scope of my_function(). It is not defined in the outer scope.

What is a global variable?
A global variable is defined outside functions, at the module level.
ex: name = "Ravi"

def display():
    print(name)

display()
print(name) output: ravi 
                    ravi 
 Both the function and the outer code can read name.

 What is a nested function?
A nested function is a function defined inside another function.
ex:
def outer():
  print("this is outer function")


  def inner():
    print("this is inner function")

  inner()
outer()  

this is outer function
this is inner function
and explanation of :
- outer() is the outer function.
- inner() is defined inside outer().
- Calling inner() inside outer() executes the inner function.
- Calling outer() starts the process.
- 
