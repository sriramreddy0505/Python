                                  1. What is an iterator in Python?
An iterator is an object that allows you to access elements one at a time, rather than needing to access all the elements at once.
numbers = [10, 20, 30, 40, 50]
You can access all the elements using a for loop. Python internally uses an iterator to retrieve those elements one by one.
iter() — gets an iterator from an iterable object.
next() — retrieves the next item from an iterator.

and ex: iter() and next ()
numbers = [10, 20, 30]

my_iterator = iter(numbers)

print(next(my_iterator))
print(next(my_iterator))
print(next(my_iterator))
ex: 10
20
30
numbers is a list.
iter(numbers) creates an iterator for that list.
If you call next(my_iterator) again, Python raises StopIteration because there are no more elements.

            enumerate()
enumerate() gives you both the index and the value while iterating.
ex: names = ["Ravi", "Sita", "Raju"]

for index, name in enumerate(names):
    print(index, name)
    output: 0 Ravi
1 Sita
2 Raju

         2. What are the advantages of iterators?
Iterators are useful when working with large amounts of data or processing information step by step.
Important: Not every iterator is automatically memory-efficient. For example, creating a list from an iterator stores all its results in memory.
Memory efficiency: You can process items one at a time without creating another complete collection.
Lazy evaluation: The next value is produced only when requested.
Works with large datasets: You can process records without loading every processed result into a new list.
Simple iteration: Python's for loop handles the iterator protocol automatically.
Useful for streams: You can process data from files, database cursors, and other sources incrementally.
              3. What is a generator in Python?

   A generator is a special kind of iterator that produces values one at a time, usually using the yield keyword.
Generators make it easier to write custom iterators without manually implementing the __iter__() and __next__() methods.
ex: this is normal function 
def get_numbers():
    return [1, 2, 3]

result = get_numbers()
print(result)
output:
[1, 2, 3]

another ex: this is generator function 
def get_numbers():
    yield 1
    yield 2
    yield 3

result = get_numbers()

print(result)
output:
<generator object get_numbers at 0x...>

Why? Because calling a generator function creates a generator object. It does not immediately run the function to produce all its values.

To retrieve the values:
def get_numbers():
    yield 1
    yield 2
    yield 3

result = get_numbers()

print(next(result))
print(next(result))
print(next(result))
output:
1
2
3  
# in this we have to use to the step 1=
 call the generator function
 Call next()
 Reach yield
 Call next() again
 
     4.What is the yield keyword?
The yield keyword returns a value from a generator while pausing the function's execution state.
Unlike return, which ends a normal function call, yield lets the function resume later from the same point.
ex:
def my_generator():
    print("starting")
    yield 1

    print("ending")
    yield 2

result=my_generator()
print(next(result)) 
print(next(result)) 
starting
1
ending
2
explanation:
result = my_generator() creates the generator. The function body has not run yet.
The first next(result) starts execution, prints Starting, and pauses at yield 10.
The second next(result) resumes after the first yield, prints Continuing, and pauses at yield 20.

     5. Creating a generator function
Let's create a generator that produces numbers from 1 to 5.
ex:
def count_number():
  for number in range(1,6):
    yield number

for value in count_number():
  print(value)  
1
2
3
4
5

Example: generator expression
Just as Python has list comprehensions, it also has generator expressions.
The key difference is that a list comprehension creates a list immediately, while a generator expression computes values as they are requested.
             6. Using next() with generators
The next() function requests one value from a generator at a time.
ex:
def fruits():
  yield "mango"
  yield "banana"
  yield "apple"
result=fruits()
print(next(result))
print(next(result))
print(next(result))
print(next(result, "no more fruits is there"))
mango
banana
apple
no more fruits is there
and mainly The fourth call returns the default value because the generator is exhausted.
Remember: Once a generator is exhausted, calling next() with a default keeps returning that default; it does not restart the generator.

     Why use generators?
- They can reduce memory usage.
- They allow lazy evaluation.
- They make custom iteration simple.
- They are helpful for file processing, data pipelines, and large sequences.
- They can represent potentially infinite sequences, provided you consume them carefully.

        7. What is a decorator in Python?
A decorator is a function that takes another function and adds or changes behavior around it without requiring you to rewrite the original function's code.
Decorators are commonly used for:
- Logging function calls.
- Measuring execution time.
- Checking permissions.
- Authentication.
- Caching results.
- Validating inputs.

Add a wrapper function
A common decorator pattern uses an inner function called a wrapper.
ex:
def my_decorator(func):
    def wrapper():
        print("Before function execution")

        func()

        print("After function execution")

    return wrapper


         8. What is a higher-order function?
A higher-order function is a function that does at least one of the following:
1. Accepts another function as an argument.
2. Returns a function as its result.
In Python, functions are first-class objects. This means you can store them in variables, pass them to other functions, and return them from functions.



