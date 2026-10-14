       
       Python Dictionary:
  In Python, a dictionary is a built-in data type used to store data in key-value pairs.
  Dictionaries are useful when you want to store related information and access it using a key instead of an index.
  1. What is a dictionary in Python:
 A dictionary stores data in the form of key: value pairs inside curly braces {}.
per example:
student = {
    "name": "Sriram",
    "age": 22,
    "course": "Python"
}
print(student)  
and output:
{'name': 'Sriram', 'age': 22, 'course': 'Python'}
and here ("name", "age", and "course" are keys.
"Sriram", 22, and "Python" are values.)
anothef ex:
mydict={1:"ram",2:"reddy",3:"balireddy"}
mydict[4]="called"
mydict["ram"]="reddy"
print(mydict)
{1: 'ram', 2: 'reddy', 3: 'balireddy', 4: 'called', 'ram': 'reddy'}


and mainly A dictionary can contain a list as a value, but you cannot use a list as a key.
   Creating and declaring a dictionary:

There are several ways to create a dictionary.
mainly we can identify the Using curly braces {}
 add():

mydict={1:"ram",2:"reddy",3:"balireddy"}
mydict[4]="called"
print(mydict)
{1: 'ram', 2: 'reddy', 3: 'balireddy', 4: 'called'}

using of dict():

ram=dict(ram=10)
print(ram)
{'ram': 10}
Notice that with this form, the keys are written as keyword arguments without quotation marks.

Using dict() with pairs:

name=dict([("ram", "reddy"),("hhs",11)])
print(name)
{'ram': 'reddy', 'hhs': 11}
This method converts a sequence of key-value pairs into a dictionary.

 using square brakets[]:

 ex:student = {
    "name": "Sriram",
    "age": 22,
    "course": "Python"
}

print(student["name"])
print(student["age"])
output:
Sriram
22                #  when i want perticular data then i will be use to the [] and when tha key is missing then [] can give to the key error 
 Using get()

 The get() method retrieves the value associated with a key.
 syntax:dictionary.get(key)
 student = {
    "name": "Sriram",
    "age": 22
}
print(student.get("name"))
print(student.get("age"))
print(student.get("marks"))
out put: Sriram
22
None
The missing "marks" key returns None rather than raising a KeyError 
            #  and mainly difference is the [] and get() is the [] can give the missing key is the key error but get() can give the none 
 
 Updating dictionary values:
  You can change the value of an existing key by assigning a new value to it.
  ex:
mydict={1:"ram",2:"reddy",3:"balireddy"}
mydict[4]="called"
mydict[3]="reddy"
print(mydict)
{1: 'ram', 2: 'reddy', 3: 'reddy', 4: 'called'}
the name change from balireddy to reddy 
importent:  mainly key is the immutable and its can't change once create and values is mutable so its can change when we want to change and dictionary is the 
unordered .
Adding and updating with update()
The update() method can add new keys and update existing keys.
syntax:
dictionary.update({"key": value})
          The keys() method:
The keys() method returns a view of all keys in the dictionary.

syntax:dictionary.keys()
ex:student = {
    "name": "Ravi",
    "age": 20,
    "course": "Python"
}

print(student.keys())
output: dict_keys(['name', 'age', 'course'])

The values() method
The values() method returns a view of all the values in the dictionary.
dictionary.values()


The items() method
The items() method returns all dictionary entries as key-value pairs.
dictionary.items()
ex:student = {
    "name": "Ravi",
    "age": 20,
    "course": "Python"
}

print(student.items())
and output is coming to the plain text
dict_items([
    ('name', 'Ravi'),
    ('age', 20),
    ('course', 'Python')
])


