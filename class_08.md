    index() 

index() tells us where a value is located in a list.    
fruits = ["apple", "banana", "mango", "orange"]
print(fruits.index("mango"))  # 2
index is starting from "0"

index() when the same value occurs 2 times
 numbers = [10, 20, 30, 20, 40]  
                                  # here 20 occurs 2 times but output is 1 why not 3?
                                  Because index() returns the first occurrence.
print(numbers.index(20))

How to find the second occurrence?
You can use the start argument:
numbers = [10, 20, 30, 20, 40]
print(numbers.index(20, 2)) #3 
syntax;  numbers.index(value, start_position)
so index of 2 is starting from the 30 onwards and after index of 2 is one 20 is there so that position is 3 and after index of 2 its prefer the 1st 20 only.
       count()
   count() tells us how many times a value appears.
   numbers = [10, 20, 30, 20, 40, 20]
   print(numbers.count(20))   #3
   count() → How many?
      sort()
   sort() arranges the list in ascending order by default.
   numbers = [50, 10, 40, 20, 30]
      numbers.sort()
    print(numbers)
    output:10 20 30 40 50

    so sort can change original list and its didn't create  new list

    sort(reverse=True)
    descending order 
    numbers = [50, 10, 40, 20, 30]
\   numbers.sort(reverse=True)
     print(numbers) #[50, 40, 30, 20, 10]

     Sorting strings
     
     sort() can also sort strings alphabetically.
     names = ["Ravi", "Anil", "Suresh", "Bala"]
     names.sort()
     print(names)
     #['Anil', 'Bala', 'Ravi', 'Suresh']
     reverse is 
     names.sort(reverse=True)
     ['Suresh', 'Ravi', 'Bala', 'Anil']
     
     Sort by key length
     But suppose we want to sort based on length of each string.
     names.sort(key=len)
     print(names) #['Ram', 'Anil', 'Sriram', 'Krishna']
     mainly key -lengthis used to check the length then divide and arrange the ascending the length like ram is 3 and anil is 4 characters so compare the values
     ram length is less then arrange starting

     Sort by length in reverse order

     names = ["Ram", "Sriram", "Anil", "Krishna"]
    names.sort(key=len, reverse=True)
   print(names) #['Krishna', 'Sriram', 'Anil', 'Ram']
   and this is descending order and which sentence have highest length then start bigining
   
     pop() — Remove an item

     pop() removes an item from a list and returns the removed item.
     numbers = [10, 20, 30, 40]
    x = numbers.pop()
   print(x)
   (numbers)
#40
[10, 20, 30]

By default, pop() removes the last item.
pop(index)

numbers = [10, 20, 30, 40]
x = numbers.pop(1)
print(x)
print(numbers) #20
[10, 30, 40]  because index 1 is contain 20 and Remove the item at index 1.

popleft()

popleft() is not a normal list method.
It belongs to Python's deque from the collections module.
numbers = deque([10, 20, 30, 40])
numbers.popleft()
print(numbers) #deque([20, 30, 40])
its remove the 1st item 


   
