                        1. NumPy Random Functions
NumPy provides a random module to generate random numbers.

We use random numbers for:
- Generating sample datasets.
- Machine Learning model testing.
- Simulations.
- Random initialization of neural network weights.
- Creating dummy data.
-                   1.1 Random Float – np.random.rand()
A random float is a decimal number generated randomly between 0 and 1.
 syntax:  np.random.rand()
 ex: import numpy as np
x = np.random.rand()
print(x)  # 0.745821
The output changes whenever you execute the code.
another ex:
x = np.random.rand(5)
print(x)  # [0.23 0.76 0.45 0.91 0.12]
Here, 5 means generate five random values.
       1.2 Random Integers – np.random.randint()
This function generates random integer values.
syntax:   np.random.randint(low, high, size)
ex: x = np.random.randint(1, 100, size=5)
print(x)  # [12 45 78 23 90]            minly size can show to the how many steps to complete to the 1 to 100 and in this 5 steps 
         2. NumPy Reshape – np.reshape()
Reshape means changing the dimensions of an array without changing its elements.
  ex: converting 1D to 2D 
  import numpy as np

arr = np.array([10, 20, 30, 40, 50, 60])
new_arr = np.reshape(arr, (2, 3))
print(new_arr)  # [[10 20 30]
 [40 50 60]]
                         3. NumPy title / tile() Function
I assume you mean NumPy's np.tile() function.
The tile() function repeats an array multiple times.

why do we use it?
Repeating data.
Creating patterns.
Generating sample arrays.
Preparing arrays for mathematical operations.
syntax: np.tile(array, repetitions)
ex: import numpy as np

arr = np.array([10, 20, 30])
result = np.tile(arr, 2)
print(result) # [10 20 30 10 20 30]
and 2D is 
arr = np.array([1, 2, 3])
result = np.tile(arr, (2, 1))
print(result) # [[1 2 3]
                [1 2 3]]
   explanation: 2 = repeat two times vertically.
              1 = repeat one time horizontally. 
      4. NumPy fromfunction()
The np.fromfunction() function creates an array by applying a function to coordinate indices.
It is useful when you want to generate values based on row and column positions. 
syntax:
 np.fromfunction(function, shape)
 ex: import numpy as np

def my_function(i, j):
    return i + j
arr = np.fromfunction(my_function, (3, 3))
print(arr)    # [[0. 1. 2.]
                 [1. 2. 3.]
                [2. 3. 4.]]
  5. NumPy fromiter()
The np.fromiter() function creates a NumPy array from an iterable.
What is an iterable?
An iterable is something that can be accessed one element at a time.  
syntax: np.fromiter(iterable, dtype)
fromiter() converts the generated values into a NumPy array.
                     6. NumPy Diagonal – np.diag()
The np.diag() function is used to extract the diagonal elements of a 2D array or create a diagonal matrix from a 1D array.
ex:  import numpy as np
arr = np.array([10, 20, 30])
result = np.diag(arr)
print(result) 
[[10  0  0]
 [ 0 20  0]
 [ 0  0 30]]
 Here, the values are placed along the main diagonal. Other positions contain zero.
  Upper and lower diagonals
  ex: arr = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])

print(np.diag(arr, k=1))
print(np.diag(arr, k=-1))
output: [2 6]
        [4 8]
               7. NumPy Indexing
Indexing means accessing individual elements from an array using their positions.
NumPy indexing starts from 0, not 1.      
ex: import numpy as np

arr = np.array([10, 20, 30, 40, 50])

print(arr[0])
print(arr[1])
print(arr[4])
#10
20
50
                       8. NumPy Slicing
Slicing means extracting a portion of an array.
syntax: array[start:stop:step]
   ex: import numpy as np
arr = np.array([10, 20, 30, 40, 50, 60])
print(arr[1:4])
# [20 30 40]
explanation: Start at index 1.
Stop before index 4.
Extract 20, 30, 40.
         9. Fancy Indexing
Fancy indexing means selecting specific elements using a list or array of index positions.
It is useful when you want particular elements that are not necessarily next to each other.
ex: import numpy as np

arr = np.array([10, 20, 30, 40, 50, 60])
result = arr[[0, 2, 4]]
print(result)
#[10 30 50]
                  10. Boolean Indexing / Boolean Slicing
Boolean indexing means selecting array elements based on conditions.
