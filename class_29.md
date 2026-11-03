                  1. Understanding np.copy()
Definition: np.copy() is used to create an independent copy of an existing NumPy array.
It means if you change the copied array, the original array will not change.
ex: import numpy as np

arr = np.array([10, 20, 30, 40])
copied = np.copy(arr)
print("Original Array:", arr)
print("Copied Array:", copied)
# Original Array: [10 20 30 40]
Copied Array:   [10 20 30 40]
   import: if we modified the copied array ?
  Original array remains unchanged.
 Copied array changes independently.
 np.copy() creates a separate array.
        2. Copying vs Slicing in NumPy
There are two ways to get data from an existing NumPy array:
- Copying
- Slicing
But both behave differently.
ex:
   arr = np.array([10, 20, 30, 40, 50])
sliced = arr[1:4]
print(sliced) # 20,30,40
 and after modify the
sliced[0] = 200

print("Original:", arr)
print("Sliced:", sliced)
Original: [10 200  30  40  50]
Sliced:   [200  30  40]
  ex:in this slicing original is changed
  Why did the original array change?
  Because basic NumPy slicing generally returns a view, not an independent copy.
  A view shares the same underlying data.
             3. np.min()
             - np.min() returns the minimum value.
Definition: np.min() is used to find the minimum (smallest) value in an array.
ex: arr = np.array([
    [10, 20, 30],
    [40, 5, 60]
])

print(np.min(arr))
# 5
It finds the minimum value across the entire array.
 Using axis
Axis is important when working with 2D and 3D arrays.
ex: arr = np.array([
    [10, 20, 30],
    [40, 5, 60]
])

print(np.min(arr, axis=0))
print(np.min(arr, axis=1))
# [10  5 30]
[10  5]
                            4. np.argmin()
Definition: np.argmin() returns the index (position) of the minimum value in an array.
- np.argmin() returns the index of the minimum value.
  ex: arr = np.array([10, 50, 20, 5, 40])

print(np.min(arr))
print(np.argmin(arr))
# 5
3
another ex: arr = np.array([
    [10, 20, 30],
    [40, 5, 60]
])
print(np.argmin(arr))
# 4
By default, NumPy flattens the array into one dimension before finding the index.
         5. np.round()
Definition: np.round() is used to round decimal values to a specified number of decimal places.
ex:arr = np.array([10.234, 20.567, 30.891])
      print(np.round(arr))
      # [10. 21. 31.]
 and rounding to 2 decimals is 
 ex:arr = np.array([10.2345, 20.5678, 30.8912])

print(np.round(arr, 2))
# [10.23 20.57 30.89]
In data analysis, we often use rounding to display prices, percentages, averages, and measurements in a readable format.
Note: NumPy uses round-to-even for exact halfway cases, such as np.round(2.5) giving 2.0 and np.round(3.5) giving 4.0.
               6. np.floor()
Definition: np.floor() rounds a number DOWN to the nearest integer.
It always moves towards negative infinity.
positive ex: arr = np.array([10.2, 20.8, 30.5, 40.9])
print(np.floor(arr))
# [10. 20. 30. 40.]
and negative ex: arr = np.array([-2.1, -3.8, 4.7])
print(np.floor(arr))
# [-3. -4.  4.]
Why does -2.1 become -3?
Because floor moves towards negative infinity, not towards zero.
              7. np.ceil()
Definition: np.ceil() rounds a number UP to the nearest integer.
It moves towards positive infinity.
positive ex: arr = np.array([10.2, 20.8, 30.5, 40.1])
print(np.ceil(arr))
# [11. 21. 31. 41.]
negative ex: arr = np.array([-2.1, -3.8, 4.7])
print(np.ceil(arr))
# [-2. -3.  5.]
    and mainly those 3 is round() = nearest value (with ties-to-even).
                        floor() = towards negative infinity.
                        ceil() = towards positive infinity.
              8. np.cumsum() – Cumulative Sum
Definition: np.cumsum() calculates the cumulative sum of array elements.
Cumulative means adding the current value to the previous total.   
ex: arr = np.array([10, 20, 30, 40])
result = np.cumsum(arr)                # in this 10+20 is 2nd one is there then 30+30 is there then 60+40 is there 
print(result)
# [ 10  30  60 100]
and using of axis is the axis=0: Cumulative sum down each column.
                        axis=1: Cumulative sum across each row
             9. np.cumprod() – Cumulative Product
Definition: np.cumprod() calculates the cumulative multiplication of array elements.
ex:arr = np.array([2, 3, 4, 5])
        result = np.cumprod(arr)
       print(result)
       # [  2   6  24 120]
       this is multiplying previous numbers      # 2x6 
       
       Definition: np.concatenate() is used to combine two or more NumPy arrays into a single array.
      It can combine arrays horizontally or vertically depending on the axis.
      ex:
      arr1 = np.array([10, 20, 30])
     arr2 = np.array([40, 50, 60])
    result = np.concatenate((arr1, arr2))
    print(result) 
    # [10 20 30 40 50 60]
    First array contains 3 values.
    Second array contains 3 values.
    Concatenate combines both arrays.
