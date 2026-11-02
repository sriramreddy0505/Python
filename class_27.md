               1. What is NumPy?
NumPy stands for Numerical Python.
NumPy is a Python library used to perform mathematical and numerical operations efficiently.
It provides a special data structure called an Array (ndarray).
we use numpy for:

Working with large amounts of numerical data.
Mathematical calculations.
Matrix operations.
Statistical operations.
Data preprocessing.
Machine Learning and Deep Learning.
Image processing and CNN models.

mainly we can use numpy and python
we have to see difference between python and numpy:
normal python:
numbers = [10, 20, 30, 40, 50]
result = [x * 2 for x in numbers]
print(result)    # [20, 40, 60, 80, 100]

with numpy:
import numpy as np
numbers =np.array([10,22,33,4,5,6])
result=numbers*2
print(result)
[20 44 66  8 10 12]
difference:
Python lists generally require loops or comprehensions for element-wise mathematical operations.
NumPy arrays support vectorized operations, making numerical calculations faster and more convenient.

            2.What is an Array in NumPy?
An array is a collection of elements stored in a structured format.
ex:
import numpy as np
numbers=np.array([1,2,3,45,5])
print(numbers)
[ 1  2  3 45  5]
result: [10 20 30 40 50]
syntax of array 
np.array([elements])


   Types of NumPy arrays
NumPy arrays are commonly classified based on their dimensions.

There are four important concepts:
1. 0D Array
2. 1D Array
3. 2D Array
4. 3D Array
                  1. 0D Array
   A 0D array is also called a scalar array.
  It contains only one element.
    a=np.array([10])
                    2. 1D Array
   A 1D array is a one-dimensional array.
  It contains elements arranged in a single line.

    import numpy as np
a = np.array([10, 20, 30, 40, 50])

print(a)
print("Dimension:", a.ndim)
print("Shape:", a.shape)
output:
[10 20 30 40 50]

Dimension: 1
Shape: (5,)
                    3. 2D Array
               A 2D array is a two-dimensional array.
              It contains rows and columns.


    a = np.array([
    [10, 20, 30, 40],
    [50, 60, 70, 80]
])

print(a.shape)
print(a.ndim)

output:
(2, 4)
2
and mainly A 2D array is commonly used to represent matrices, tabular data, and grayscale images.
                               4. 3D Array             
A 3D array is a three-dimensional array.
It contains multiple 2D arrays stacked together.
Think of it as a collection of matrices.
ex: 
import numpy as np
n=np.array([[[1,2,3],[2,4,4]],[[2,32,3],[234,42,43]]])
print(n)
print(n.ndim)
print(n.shape)
[[[  1   2   3]
  [  2   4   4]]

 [[  2  32   3]
  [234  42  43]]]
3
(2, 2, 3)

                3. What is dtype in NumPy?
dtype means Data Type.
It tells us what type of data is stored inside a NumPy array.
ex:import numpy as np
a = np.array([10, 20, 30, 40])
print(a.dtype)
                    #int64
 It means the array is storing 64-bit integers (on a typical 64-bit environment).
                   4. convert d type?
            syntax: array.astype(new_dtype)
            ex: 
a=np.array([1,32,3,44,4])
b=a.astype(np.float64)
print(b)
[ 1. 32.  3. 44.  4.]

astype() is a NumPy method used to convert an array from one data type to another.

for CNN:
Why do we use float32 in Deep Learning?
- It uses 4 bytes per value.
- It generally requires less memory than float64, which uses 8 bytes.
- It is widely supported by deep learning frameworks.
- It is commonly used for image pixel values and model inputs.
-  convert to the list to array
 a = [10, 20, 30, 40]
b = np.array(a)
print(b)
#[10 20 30 40]
       Important NumPy Properties:
   import numpy as np

a = np.array([
    [10, 20, 30],
    [40, 50, 60]
])
             Property 1: shape
shape tells us the number of elements along each dimension.
          print(a.shape)
              # (2, 3)

              Property 2: ndim
ndim tells us the number of dimensions of an array.
       print(a.ndim)
       #2
       this is 2D array 
  Property 3: dtype
dtype tells us the data type of the elements.
print(a.dtype)
# int64
                    Property 4: size
size tells us the total number of elements.
print(a.size)
# 6
                  Property 5: itemsize
itemsize tells us how many bytes each element occupies.
print(a.itemsize)
# 8
             12. What is arange() in NumPy?
arange() means array range.
It generates evenly spaced values using a specified step size.
   syntax: np.arange(start, stop, step)
   ex: a = np.arange(1, 20, 2)
   print(a)  # [ 1  3  5  7  9 11 13 15 17 19]

   another ex: import numpy as np

a = np.arange(1.0, 5.0, 0.5)

print(a)
# [1.  1.5 2.  2.5 3.  3.5 4.  4.5]

                                  5. What is linspace() in NumPy?
linspace() means Linear Space.
It generates a specified number of evenly spaced values between a starting point and an ending point.
syntax: np.linspace(start, stop, num)
ex: import numpy as np
a = np.linspace(1, 10, 5)
print(a) # [ 1.    3.25  5.5   7.75 10.  ]
means we have to complete the with in 5 steps 
                                 6. What is ones() in NumPy?
ones() is used to create an array filled with 1s.
syntax: np.ones(shape)
ex: import numpy as np

a = np.ones(5)
print(a)
# [1. 1. 1. 1. 1.]
By default, the data type is float64.
and Zeros also same like this

                     6. What is zeros() in NumPy?
         a = np.zeros((2, 3))
       print(a)
       #
           [[0. 0. 0.]
          [0. 0. 0.]]
                     7. full()
Creates an array filled with a specific value.
a = np.full((2, 3), 7)
print(a)     # [[7 7 7]
              [7 7 7]]
          8. eye()
Creates an identity matrix.
ex:  a = np.eye(3)
print(a)
               #  [[1. 0. 0.]
                  [0. 1. 0.]
                  [0. 0. 1.]]
                  



   
 

   

        
            
