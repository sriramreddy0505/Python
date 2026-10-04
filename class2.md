            data types?
>A data type tells Python what kind of data a variable is storing.
>age = 25
name = "Sriram"
salary = 35000.50
is_student = True
>in this code can have the (age  is the variable, 25 is the value and type is  integer )
>
>Python needs to know what type of value it is dealing with because different data types support different operations.
>a=10
>b=20 result is 30   (10 + 20       → numbers → addition)
>a="10"
>b="20" result is 1020    ("10" + "20"   → strings → concatenation )
>
>main python data types
1. Numeric
  int
  float
  complex
2. Boolean
    bool
3. Sequence
    str
    list
   tuple
4. Set
   set
5. Mapping
    dict
6. None
   NoneType

        what are primitive data types?


   >Primitive data types are simple types used to represent individual values
   >int
   float
   complex
   bool
   str
   > using of this code can we will identify the data type " print(type(age))  "
   
                 What are Non-Primitive Data Types?

>non-primitive data types are used to store multiple values.
>list
tuple
set
dictionary
>data=[10,12,3,4,,66]  here this variable can store the multiple values
>
        list stored multiple values

Ordered                                        #list is mutable we can change and its have duplicate values aslo 
Mutable
Allow duplicates
Can contain different data types
>mainly list is the mutable and we can change the list
>marks = [90, 80, 70]
marks[1] = 95               #in this starts from 0,1,2 for forward and backward is -1,-2 like this 
print(marks)

       tuple also stored multiple values

> numbers(10,20,30,40)                        # tuple is immutable and we cant chnage onece create 
> Ordered
 Immutable
 Allows duplicates       
   >mainly we can change the tuple once created because of this is a immutable
>         A set stores unique values.
  this set can remove the duplicates
> numbers = {10, 20, 20, 30, 30}                #set is a store unique values only andremove duplicates
print(numbers)       #result is the {10,20,30}

      Dictionary stores data in key-value pairs.

      student = {
    "name": "Sriram",
    "age": 25,
    "marks": 90
}
in this code left side is the key and right side is the value
dictionary means we have to store the data  in key values pair
key       value
name      Sriram
age       25
marks     90

Type Conversion
1. Implicit Conversion              #Implicit conversion does not mean Python can automatically convert every type.(10,"20") this it's can't identify some times we have to do explicit 
  Python does it automatically
2.Explicit Conversion
       Programmer does it manually


   assignment operator
   Operator | Meaning  
 `=`      | Assignment              
 `+=`     | Add and assign          
 `-=`     | Subtract and assign     #  x+=5 this  means x = x + 5
 `*=`     | Multiply and assign     
 `/=`     | Divide and assign       
 `//=`    | Floor divide and assign 
 `%=`     | Modulus and assign      
 `**=`    | Power and assign
   

