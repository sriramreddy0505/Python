 tuple in python?

A tuple is a collection of multiple values stored together.
mytuple = (10, 20, 30, 40) 
here is the mytuple is the variable name and numbers is the values
and tuple can store the multiple values in the single variable
  duplicate
  
  mytuple = (10, 20, 10, 30, 10)
  mainly tuple can allow to the duplicate values 
  Immutable
  
  Once a tuple is created, we cannot directly change its elements.
  mytuple = (10, 20, 30)
   mytuple[0] = 100   # type error 
   Because tuples are immutable and once created the tuple that individual value cann't change in directly

   Allows Different Data Types
   mytuple = (10, "Python", 3.14, True) 
   and a tuple can contain different data types
   
   how to create a tuple?
   
   Use parentheses:
   mytuple = (10, 20, 30)
   and mainly we have to use the type then only we can identify easily print(type(mytuple))
   Single-Element Tuple
 mainly when u use mytuple = (10) then python can consider the integer 
 so when u use only single value u have to put the comma(,) 
 mytuple = (10,) so this is type of tuple can identify easily    #(10) this is int
   #(10,) this is  tuple

   Tuple Packing

Tuple packing means putting multiple values into one tuple.
name = "Sriram"
age = 25
city = "Hyderabad"
person = name, age, city
print(person) # ('Sriram', 25, 'Hyderabad')
another ex:
mytuple = 10, 20, 30 #(10, 20, 30)
this is called paking and if the multiple values add to the one tuple that is called tuple paking

Tuple Unpacking?
this is opposite of the paking 
person = ("Sriram", 25, "Hyderabad")
print(name)
print(age)
print(city)
in this tuple values can take to separate variable this is called unpaking 
Number of variables should normally match number of values.
person = ("Sriram", 25, "Hyderabad")
name, age, city = person
   in this format can match the all the values and variables and 
   name, age = person "in this one error is there so values and variables should match same  "

   We Add/Edit Tuple Items?


   Because tuples are immutable, we cannot directly add, remove, or edit individual elements.
   mytuple = (10, 20, 30)
   mytuple[1] = 200  # error is there
   so mainly tuple is immutable we can't directly change anything so we have to convert to the tuple to list then change modification then again change tuple then we can change.
   tuple → list → modify → tuple.
   mytuple = (10, 20, 30)
   mylist = list(mytuple)
  mylist[1] = 200
  mytuple = tuple(mylist)
  print(mytuple)


  Access Tuple Items Using Index

  mytuple = ("Python", "Java", "C++")
  index of [0] is python
  and negative index also there  and index can identify thhe position of value also and
  syntax is :
  tuple.index(value)

  count()
  count() tells us how many times a value appears.
  [10,10,10,20]
  mytuple(10) how many 10's is there #3



  what is set?

  A set is a collection of unique elements. # it is didn't store the duplicate values
  myset = {10, 20, 30} and it's didn't store the duplicate values
      1. unordered?
  Sets do not maintain a reliable positional order like lists/tuples.
  Don't depend on a particular display order.

      2.No Duplicate Values
      myset = {10, 20, 10, 30, 20}
     print(myset)
 The duplicate values are removed, conceptually leaving: #10,20,30
 and set didn't allow the duplicate values

       3.mutable
 A set itself can be changed.
    4.No Indexing
    Because a set is unordered and doesn't support indexing.

    5. declaration of set is Use curly braces { }.
    6.add()

    add() adds one element to a set.
    syntax: set.add(value)
    myset = {10, 20, 30}
   myset.add(40)  #10,20,30,40
   print(myset)
    7.remove()
   remove() removes an element.
   myset.remove(40)  #10,20,30
     8.discard()
   discard() also removes an element.
   
   #remove()  → item absent → Error
  discard() → item absent → No error
    
      9.pop()
  pop() removes one arbitrary element from a set.
  myset = {10, 20, 30, 40}
 x = myset.pop()
 print(x)
  print(myset) # one element is removed
  always removes the first or last element.
 A set is unordered, so the element removed is arbitrary.

 clear()
 clear() removes all elements from the set.
