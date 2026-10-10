          Python Set Methods
   A set is a collection of unique elements. It does not allow duplicate values, and it is unordered.  
    if any values are repeated more than one time then python can remove the duplicates
    numbers = {10, 20, 20, 30}
   print(numbers)    #{10, 20, 30}
      1. issubset
      Meaning: Checks whether all elements of one set are present in another set.
      A = {1, 2}
       B = {1, 2, 3, 4, 5}
        print(A.issubset(B))   # true
        and ex2:
        A = {1, 2, 6}
        B = {1, 2, 3, 4, 5}
        print(A.issubset(B)) # false 
        Why? Because 6 is not present in B. # a.issubset b means in the a is have the values of 1,2,3, and b also have same values then only true 
       issubset() asks, “Are all my elements inside the other set?”

     2. issuperset()
     Checks whether a set contains every element of another set.

    A = {1, 2, 3, 4, 5}\
    B = {1, 2}
    print(A.issuperset(B)) # true
    Why? A contains both 1 and 2, which are all the elements of B.

    all the B  set values are included in the A set values so this is true 
    union()

    Combines the elements of two sets, removing duplicates.
    A = {1, 2, 3}
    B = {3, 4, 5}
    result = A.union(B)
     print(result) # {1, 2, 3, 4, 5}
     and u can also use to the print(A | B) and it produce the same union
     and in this union can take the common values only one value and add one set and remove the duplicates.

     intersection()

     Returns only the common elements in both sets.
     A = {1, 2, 3, 4}
     B = {3, 4, 5, 6}
    print(A.intersection(B))   #{3, 4}
    and u can also use print(A & B)

    difference()

 Returns elements that exist in the first set but not in the second set.
 A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
   print(A.difference(B))    #{1,2}
   Why? 1 and 2 are in A but not in B.
   
   symmetric_difference()
 Returns elements that are in either set, but not in both sets.
 A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
print(A.symmetric_difference(B))
{1, 2, 5, 6}  # in both sets can take the union elements only not the same numbers and unmated elements only 
     
         
