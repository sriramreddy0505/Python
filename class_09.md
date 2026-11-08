
      1.pop()
  pop() removes one arbitrary element from a set.
  myset = {10, 20, 30, 40}
 x = myset.pop()
 print(x)
  print(myset) # one element is removed
  always removes the first or last element.
 A set is unordered, so the element removed is arbitrary.

 clear()
 clear() removes all elements from the set.
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

2.popleft()

popleft() is not a normal list method.
It belongs to Python's deque from the collections module.
numbers = deque([10, 20, 30, 40])
numbers.popleft()
print(numbers) #deque([20, 30, 40])
its remove the 1st item 
