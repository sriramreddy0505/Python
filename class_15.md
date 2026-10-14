      dict.pop()
    Removing an item from a dictionary
    The pop() method removes a specified key from a dictionary and returns the value associated with that key
    
    syntax: dictionary.pop(key, default)
    key: The key you want to remove.
    default: Optional. The value returned if the key does not exist.
    ex:
    mydict={1:"ram",2:"reddy",3:"balireddy"}
    name=mydict.pop(2)
    print(name)
   print(mydict)
   output:
  reddy (this is removed value)
  1: 'ram', 3: 'balireddy'} (this is updated dictionary )
  Important: If the key does not exist and you do not supply a default, pop() raises a KeyError.

  dict.setdefault():

  Get a value or create a key
  The setdefault() method returns the value of a key if it already exists. 
  If the key does not exist, it adds that key with the specified default value and returns the value.

  syntax:
  dictionary.setdefault(key, default_value)

  if Key already exists
  student = {
    "name": "Sriram",
    "age": 22
}

result = student.setdefault("age", 25)
print(result)
print(student)
output:
22
{'name': 'Sriram', 'age': 22}
Why did it return 22, not 25? Because "age" already exists, so setdefault() does not replace its value.
 Key does not exist
 student = {
    "name": "Sriram",
    "age": 22
}

result = student.setdefault("course", "Python")
print(result)
print(student)
output:
Python
{'name': 'Sriram', 'age': 22, 'course': 'Python'}
Python checks whether "course" exists.
It does not exist.
Python adds "course": "Python".
It returns "Python".



  dict.update()

  The update() method adds key-value pairs from another dictionary or suitable iterable. If a key already exists, its value is replaced.
  synatax: dictionary1.update(dictionary2)
  and it's updating two dictionarys

  ex:
mydict1={1:"ram",2:"reddy",3:"balireddy"}
mydict2={4:"venkat",5:"krishna",2:"chandu"}
mydict1.update(mydict2)
print(mydict1)
{1: 'ram', 2: 'chandu', 3: 'balireddy', 4: 'venkat', 5: 'krishna'}
  notice: dict1 contains three entries.
dict2 contains two entries.
Python checks each entry in dict2.
"age" exists in dict1, so reddy becomes chandu.
"course" is new, so it is added.
The updated result is stored in dict1.

Notice that update() modifies dict1 directly. It does not automatically create a new dictionary.


       Finding a key in a dictionary:
   You can check whether a key exists using the in operator.
   ex: key exist
     mydict1={1:"ram",2:"reddy",3:"balireddy"}
     print(2 in mydict1)
       True

       another ex: key did'nt exit 
      print("marks" in student) #false

      Sorting dictionary keys by their length:
      
    The built-in sorted() function returns a sorted list. You can use its key parameter to sort dictionary keys according to their lengths.
    syntax:
    sorted(dictionary, key=len)
    ex: student = {
    "name": "Ravi",
    "age": 20,
    "course": "Python",
    "city": "Delhi"                  # this is ascending order
}

result = sorted(student, key=len)
print(result)
      output: ['age', 'name', 'city', 'course']

      sorted(student) gets the dictionary's keys.
      key=len tells Python to compare the length of each key.
    "age" has 3 characters.
    "name" and "city" each have 4 characters.
     "course" has 6 characters.
    Python returns a list sorted by key length.

    desending order is :
    result = sorted(student, key=len, reverse=True)
    print(result)


     Sorting dictionary values:
There are different ways to sort values, depending on what you want.
Sort only the values
     marks = {
    "Ravi": 85,
    "Sriram": 95,
    "Kiran": 75
}
result = sorted(marks.values())
print(result)
output:[75, 85, 95]

Sort dictionary entries by their values:
Suppose you want each student's name alongside their marks, sorted from lowest to highest.

marks = {
    "Ravi": 85,
    "Sriram": 95,
    "Kiran": 75
}
result = sorted(marks.items(), key=lambda item: item[1])
print(result)
 #  [('Kiran', 75), ('Ravi', 85), ('Sriram', 95)]
 Here, item[1] means the value, so Python sorts by marks.

 sorted() returns a list; it does not automatically change the original dictionary's order.

 Finding the type of a dictionary:
 Python provides the type() function to identify the data type of an object.

 student = {
    "name": "Sriram",
    "age": 22
}
print(type(student))  # <class 'dict'>
 and when u use only some separate values print(type(student["name"])) its will be show the this is string so its shows to the string 
 ex:
 student = {
    "name": "Sriram",
    "age": 22,
    "marks": 95.5
}

print(type(student))
print(type(student["name"]))
print(type(student["age"]))
print(type(student["marks"]))
output:
<class 'dict'>
<class 'str'>
<class 'int'>
<class 'float'>


del
Deletes a specified key-value entry:
d = {"a": 10, "b": 20}
del d["a"]
print(d)
output:
{'b': 20}  
 



    
    
    
