                      1.What is a lambda function?
A lambda function is a small, anonymous function that is written in a single expression without using the def keyword.
Normally, we create a function using def.
ex: def square(n):
    return n * n

print(square(5))
# 25
We can write the same logic using lambda.
ex:square = lambda n: n * n

print(square(5))
# 25
and another ex:
multiply = lambda a, b: a * b

print(multiply(4, 5))
20
Important: A lambda function contains one expression, but that expression can perform a calculation or call another function. For larger tasks involving multiple statements, use def.
                   2. What is map()?
       The map() function applies a function to every item in an iterable, such as a list.
syntax:
map(function, iterable)

function: the operation you want to perform.
iterable: the collection of items to process.
map() returns a map iterator, which you can convert into a list using list().
ex: numbers = [1, 2, 3, 4, 5]
result = map(lambda n: n * n, numbers)
print(list(result))
output: [1, 4, 9, 16, 25]

Convert names to uppercase
names = ["sriram", "ram", "krishna"]
result = list(map(lambda name: name.upper(), names))
print(result)
output:
['SRIRAM', 'RAM', 'KRISHNA']

           3. When should you use map()?
Use map() when you want to transform every item into a new value, such as:
- Squaring numbers.
- Converting strings to uppercase.
- Converting numeric strings to integers.
- Applying a calculation to every price.

map() with multiple lists
Python's map() can work with multiple iterables at the same time.
When you provide multiple lists, the function receives one item from each list on each call.
ex: add 2 lists
list1 = [10, 20, 30, 40]
list2 = [1, 2, 3, 4]
result = list(map(lambda a, b: a + b, list1, list2))
print(result)
output:
[11, 22, 33, 44]

    4. What is filter()?
The filter() function selects items from an iterable based on a condition.
map() transforms items.
filter() selects items that satisfy a condition.
syntax: filter(function, iterable)
    Filter even numbers
    ex:
    numbers = [1, 2, 3, 4, 5, 6, 7, 8]

result = list(filter(lambda n: n % 2 == 0, numbers))
print(result)
output:
[2, 4, 6, 8]
another ex:
names = ["Anil", "Sriram", "Arjun", "Ravi", "Anusha"]
result = list(filter(lambda name: name.startswith("A"), names))
print(result)
output:
['Anil', 'Arjun', 'Anusha']
startswith("A") checks whether each name begins with the uppercase letter A.
another ex:
items = ["Python", "", "Java", "", "SQL", ""]

result = list(filter(None, items))

print(result)
output:
['Python', 'Java', 'SQL']
explanation:
list() converts the filtered iterator into a list.
filter() keeps the strings that satisfy the condition.

Here, None tells filter() to keep items that evaluate to True.
Important distinction: filter(None, items) removes all falsy values, not just empty strings. For example, it also removes 0, False, and None from a mixed list.

i am using list comprehension  for simple way and one line code for remove extra space
               result = [item for item in items if item.strip()]
strip() removes whitespace from both ends of a string. This makes it useful when cleaning data that contains blank or whitespace-only entries.



    When should you use filter()?
Use filter() when your goal is to keep some items and discard others, based on a condition.
marks = [35, 80, 22, 65, 90]
result = list(filter(lambda m: m >= 35, marks))

Use filter() when you need to select values based on conditions, such as eligible students, positive numbers, matching names, or valid records.

 What is reduce()?
The reduce() function applies an operation to items repeatedly, combining them into one final result.
ex code:
from functools import reduce
reduce(function, iterable)
The sum of all numbers.
The product of all numbers.
The largest value, using a suitable comparison function.
A single combined result from a sequence of values.

  How does reduce() work?
  reduce() starts with the first two values, combines them, and then uses the result with the next value.

  When should you use reduce()?
Use it when you need to combine a sequence into one accumulated result and the operation is naturally expressed that way. For a simple sum, however, Python's built-in sum() is normally more readable.

 Map = Transform
Filter = Select
Reduce = Combine


