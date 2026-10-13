          list comprehension:
List comprehension is a short and simple way to create a new list from an existing sequence, such as a list, string, or range of numbers.
Normally, we use a for loop to create a list. List comprehension allows us to write that logic in a single line.
numbers = [1, 2, 3, 4, 5]
squares = [n * n for n in numbers]
print(squares)   # [1, 4, 9, 16, 25]
List comprehension makes the code shorter.
ex:
 [x**2 for x in [11,22,3,44,55,6,77]]
  out put: [121, 484, 9, 1936, 3025, 36, 5929] 
  another ex:
  
 [x+5 for x in [11,22,3,44,55,6,77]]
 output:[16, 27, 8, 49, 60, 11, 82]
 syntax of for loop in list comprehension 
 [expression for item in iterable]
 using of range()
 [x for x in range(1,6)]
 op:1,2,3,4,5
 range(1, 6) produces numbers from 1 to 5, because the ending value 6 is excluded.

 uppercase letters:

 To convert strings to uppercase, use the .upper() method.
 [x.upper() for x in ['apple','banana','mango']]
 ['APPLE', 'BANANA', 'MANGO']

another ex:
name=['ram','reddy','balireddy']
result=[x.upper() for x in name]
print(result)
['RAM', 'REDDY', 'BALIREDDY']
Explanation:

x represents each word.
x.upper() converts the word to uppercase.
The square brackets create a new list.
convert to the character of the string
re=[x.upper() for x in 'ram']
print(re)
['R', 'A', 'M']


     print the 1st index from python:
     
name=['ram','reddy','balireddy']
result=[x[0] for x in name]
print(result)
['r', 'r', 'b']  

and if i want 1st item in the list is 
name=['ram','reddy','balireddy']
result=[name[0]]
print(result) #'ram'

List comprehension using an if condition:
We use if when we want to select only items that satisfy a condition.
syntax:
new_list = [expression for item in iterable if condition]
ex:
nu=[5,10,15,20,15,33,5,6]
res=[x for x in nu if x>10]
print(res)
[15, 20, 15, 33]

even and odd numbers using list comprehension:

An even number is divisible by 2 with a remainder of 0.
The modulo operator % gives the remainder.
ex:
nu=[5,10,15,20,15,33,5,6]
res=[x for x in nu if x%2==0]
print(res)
[10, 20, 6]

An odd number has a remainder of 1 when divided by 2 (for positive integers).
ex:
nu=[5,10,15,20,15,33,5,6]
res=[x for x in nu if x%2!=0]
print(res)
[5, 15, 15, 33, 5]

if and else condision:
nu=[5,10,15,20,15,33,5,6]
res=["even" if x%2==0 else "odd" for x in nu]
print(res)
['odd', 'even', 'odd', 'even', 'odd', 'odd', 'odd', 'even']


 What is isdigit():

The .isdigit() method checks whether a string contains only digit characters.
It returns a Boolean value: True or False
a="1234"
b="139287rg3gyf"
print(a.isdigit())
print(b.isdigit())
 #True
  False
and in a is containing only digits means number so it's give to the true and b containing both strings also so its given to the false

To select only items containing digits, use if item.isdigit().
Important: isdigit() checks the characters in a string; it does not convert the string into an integer.

   What is isalpha():

   The .isalpha() method checks whether a string contains only alphabetic letters and has at least one character.
   ex:
   items = ["Python", "123", "Hello", "AI2026", "DataScience"]
   result = [item for item in items if item.isalpha()]
   print(result

   ['Python', 'Hello', 'DataScience']
   
 
