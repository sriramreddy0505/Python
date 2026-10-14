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
    "city": "Delhi"
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
    
    
