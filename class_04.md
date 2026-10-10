    what is a loop ?

    > A loop is used to execute a block of code repeatedly.
    suppose u want to print a "hello"
    without a loop:
    
    print("hello")
    print("hello")
    print("hello")

    with a loop:
    for x in range(3)
     print("hello")

     for loop?

   > A for loop is used when you want to iterate over a sequence or collection.  
    ex: string ,list,tuple,dict etc.
> for i in range(5):
    print(i)              result: 0 to 4      positive indexing #i=0, i=1, i=2, .....i=4 (5 is not included)
> this continue until the sequence is finished        #negative indexing #-1 onwards start and divide each character one by one
> 
range is start , stop , step                                
for i in range(1, 11, 2):
    print(i)                result: 1,3,5,7,9


    for loop is a string
    
    name = "Python"

for x in name:
    print(x)    
    result :
    p  
    y
    t
    h
    o
    n
   for loop is a list
   
   fruits = ["apple", "banana", "mango"]
   
   for fruit in fruits:
      print(fruit)          result: apple, banana, mango

      while loop?
  A while loop executes code as long as a condition is True
  syntax:
  while condition:
    statement
    
    i = 1
while i <= 5:
    print(i)
    i += 1  result : 1 to 5
    mainly this condition can increase add +1 then until condition id false (6<=5)
    in while loop we use to the i+=1 otherwise its print infinite of 1's
    This creates an infinite loop because i never changes.
    > mainly we use for loop when Known number of repetitions → for
    > mainly we use while loop when Condition-based repetition → while
              what is string?
      A string is a sequence of characters enclosed inside quotes.
      name = "Sriram"
    city = 'Hyderabad'              #in string both double quotes and single quotes valid
    message = "Hello Python"

    in this each character has the index     print(name[0])  result: "h"         ("Hello Python")
    this is negative:
     P   y   t   h   o   n
     -6  -5  -4  -3  -2  -1
     this is positive :
      P   y   t   h   o   n
      0    1  2   3   4   5

         string slicing 

     > Slicing means extracting a portion of a string.  
     name = "Python"
      print(name[0:3])  result is pyt      #indexing 0,1,2 
      syntax:
      string[start:stop]
     the stop indexing is not included


     string methods

     upper 
     name="python
     print(name.upper())    #PYTHON
     name="python"
    print(name.lower())      #python

    strip()
    Removes extra spaces from beginning and end.
   name="     python    "
   print(name.strip())    result: python

   replace()

   text = "I like Java"
    print(text.replace("Java", "Python"))    #i like python

    split()
    text = "Python is easy"
    print(text.split())     #["python", "is", "easy"]
    
         break()

    break is used to stop the loop immediately.
    for i in range(1, 10):
    if i == 5:
        break
    print(i)  result: 1,2,3,4

    continue()
    continue skips the current iteration and moves to the next iteration.
    for i in range(1, 10):
    if i == 5:
        continue 
    print(i)           #1,2,3,4,6,7,8,9,10
      

    
