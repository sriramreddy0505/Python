                             1. Nonlocal keyword in Python
  The nonlocal keyword is used inside a nested function to modify a variable that belongs to an enclosing function.          
  nonlocal allows an inner function to change a variable created in its outer function
  ex: without non local
  def outer():
    x = 10
     def inner():
        x = 20
        print("Inner x:", x)
    inner()
    print("Outer x:", x)

outer() 
output:Inner x: 20
Outer x: 10

explanation : = x=10 belongs to outer().
x = 20 creates a separate local variable inside inner().
Therefore, the outer variable remains 10.

and with non local ex:
def outer():
    x = 10

    def inner():
        nonlocal x
        x = 20
        print("Inner x:", x)

    inner()
    print("Outer x:", x)

outer()
output:
Inner x: 20
Outer x: 20

explanation:
outer() creates x = 10.
inner() uses nonlocal x.
Python finds x in the enclosing function.
The inner function changes its value to 20.
Both print statements show 20
nonlocal does not refer to a global variable. For a variable defined at the module level, use global when reassignment is needed.

                2. Recursive function in Python
A recursive function is a function that calls itself to solve a problem.
ex:
def show_number(n):
    if n == 0:
        return

    print(n)
    show_number(n - 1)

show_number(5)
output:
5
4
3
2
1
and in this 2 important points is there 
1. Base case: the condition that stops the recursion.
2. Recursive case: the function calling itself with a smaller or simpler problem.
Without a proper stopping condition, recursion may continue until Python raises a RecursionError.

    3.Factorial function in Python

   The factorial of a non-negative integer \(n\) is the product of all positive integers from \(1\) to \(n\).
It is represented by \(n!\).
per example : \[
5! = 5 \times 4 \times 3 \times 2 \times 1 = 120           #5x4x3x2x1=120

\] 
Factorial using a recursive function
ex:
def factorial(n):
    if n < 0:
        raise ValueError("Factorial is not defined for negative integers")

    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)

print(factorial(5))
print(factorial(3))
print(factorial(0))
output:
120
6
1

Factorial using a for loop

ex:
def factorial(n):
    if n < 0:
        raise ValueError("Enter a non-negative integer")

    result = 1

    for i in range(1, n + 1):
        result *= i

    return result

print(factorial(5))
output:
120
                             3. Function aliasing in Python

Function aliasing means assigning a function to another variable so that you can call the same function using a different name.
ex: 
def greet():
  print("hello, python")

student=greet
greet()
student() #
hello, python
hello, python

explanation :
def greet(): creates the function.
student() = greet assigns the same function object to another name.
greet() calls the function using its original name.
student() calls that same function using its alias.

