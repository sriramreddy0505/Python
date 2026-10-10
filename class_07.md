  python list?
  
A list is a collection of multiple values stored in a single variable.
   Characteristics of a List
   1.ordered 

  Lists maintain the order in which elements are added.
  fruits = ["apple", "banana", "mango"]
  print(fruits)
  output:
  ['apple', 'banana', 'mango']
     2. mutable
     Mutable means we can change the list after creating it.
    mylist=["reddy",1,2,"ram"]
    print(mylist)
    output: ['reddy',1,2,'ram']

      3.Duplicate Values
    A list can contain the same value multiple times and list can allow the duplicates values
    numbers = [10, 20, 10, 30, 10]
    print(numbers)   output: [10,20,10,30,10]
      4.Different Data Types
    A single list can contain different types of data and allow the all the different data type
    data = [10, "Sriram", 25.5, True] #list can allow all type of data
      5. indexing
    each element has an index       #like forward is 0 onwards start  and backward is -1 onwards start   
      fruits = ["apple", "banana", "mango"]
      fruits[1]=["ram"]
      print(fruits)
      output:
         ['apple','ram','mango']
         6.Negative Indexing
       this list can allow the negative indexing also  like forward is 0 onwards start  and backward is -1 onwards start
       ruits = ["apple", "banana", "mango"]
      fruits[-2]=["ram"]
      print(fruits)
      output:
         ['apple','ram','mango']
         
     list addition?

   There are two common meanings when we say list addition.
   list1 = [1, 2, 3]
   list2 = [4, 5, 6]
    result = list1 + list2
    print(result) 
    out put:
    [1,2,3,4,5,6]  # addition can add the both lists elements and then give result in one line and + operator can use to combine the 2 lists
    This is called list concatenation.
     It does not add corresponding numbers.
     [1,2,3]+[4,5,6] is like [5,7,8]  # not valid this is incorrect 
     [1,2,3,4,5,6] this is correct and # this is valid 

     List Multiplication 

     The * operator repeats a list.
     numbers = [1, 2, 3]                 #list="sriram"
                                          print(list*3)  op: sriramsriramsriram
    result = numbers * 3
    print(result)
    output:
    [1,2,3,1,2,3,1,2,3]
    ##in list multiplication means in list element not do the mathematical multiplication in list can multiply the specified number of times

    len()
    len() means length.
    how many elements are present in a list
    fruits = ["apple", "banana", "mango"]
    print(len(fruits))   #3
     append()
    append() adds one element at the end of a list.
      mylist=["apple",'banana',"1",10]
      mylist.append("reddy")
     print(mylist)
     ['apple', 'banana', '1', 10, 'reddy']

      insert()
     insert() adds an element at a specific position.
     syntax:
     list.insert(index, value)
     list=[22,33,55,66,]
      list.insert(2,"ram")
       print(list)
     [22, 33, 'ram', 55, 66]
     remove()

    remove() removes a specific value from the list.
    remove() takes the value, not the index.
    list=[22,33,55,66,]
   list.remove(33)
   print(list)  #[22,55,66]
   this is not remove index and only remove the value
   If you want to remove using an index, you would normally use pop() or del, which are separate concepts.

   clear()
   clear() removes all elements from the list.
   list=[2,3,4]
   list.clear()
   print(list)  #[]

    
    
