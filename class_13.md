 what is enumerate in python?

 The enumerate() function lets you access both the index and the item while looping through a sequence.
 Index = the position of an item.
 Item = the actual value stored at that position.
ex:
name=['ram','reddy','balireddy']
for index, item in enumerate(name):
 print(index, item)
0 ram
1 reddy
2 balireddy  # so when we are using index, item in this output was can came to the some gap is there between  index and item other wise if using x instead of index, item
if def it will be form like tuple (0,'ram') like this
        How does enumerate() work internally:

   Conceptually, it produces pairs like these
   (0, "apple")
  (1, "banana")
  (2, "mango")

  ex:
name=['ram','reddy','balireddy']
for x in enumerate(name):
 print(x)
(0, 'ram')
(1, 'reddy')
(2, 'balireddy')
   Difference between a normal for loop and enumerate()

 Normal for loop
 names = ["Ravi", "Sita", "Ram"]
 for name in names:
     print(name) #ravi, Sita , ram
 for loop with enumerate()

 names = ["Ravi", "Sita", "Ram"]
 for index, name in enumerate(names):
     print(index, name)

     When should you use enumerate()?

   Use it when you need to know the position of an item while processing it.
   For example, when displaying numbered student names or identifying which item caused an error.  
     enumerate() with items
   Suppose you have a list of student names and want to display each student with a number.
  students = ["Sriram", "Ramesh", "Kiran", "Priya"]
   for number, student in enumerate(students, start=1):
    print(number, student) 
    output:
    1 Sriram
    2 Ramesh
    3 Kiran
    4 Priya

    and also try this 
    colors = ["red", "green", "blue"]
    for index, color in enumerate(colors, start=1):
        print(f"{index}. {color}")
        1. red
         2. green
         3. blue
        # f can use to the it allows us  to insert variables directly into the string.


        What is zip() in Python?
        The zip() function combines corresponding items from two or more iterables.
Think of it as matching items by their positions.
ex:
name=['ram','reddy','balireddy']
marks=[11,22,33]
for name, marks in zip(name, marks):
  print(name,marks) output:
ram 11
reddy 22
balireddy 33

syntax of zip():
for item1, item2 in zip(sequence1, sequence2):
    print(item1, item2)

   #and you can also combine the 3 lists also as similarly

   What happens if the lists have different lengths?
ex:
name=['ram','reddy','balireddy']
marks=[11,22]
for name, marks in zip(name, marks):
  print(name,marks)
ram 11
reddy 22
   By default, zip() stops when the shortest iterable runs out of items. So Ram is not included.

   Using enumerate() and zip() together:
   You can combine both functions when you want a row number and matching values from two lists.
  ex:
name=['ram','reddy','balireddy']
marks=[11,22]
for index,(name, marks) in enumerate(zip(name, marks), start=1):
  print(index,name,marks)
  output:
1 ram 11
2 reddy 22

        

   
