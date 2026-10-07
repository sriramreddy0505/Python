string methods 

    zfill()

zfill() means zero fill.
It adds 0 to the left side of a string until it reaches the specified length.

syntax:
string.zfill(width)     #mystring="25"
                         print(mystring.zfill(5))
                             output:00025
in this example width is 5 and its only have 2 numbers so left side of width its automatically add to the 3 remaining spaces is 0 then width filled.

      replace()
replace() is used to replace one piece of text with another
syntax:
string.replace(old, new)
ex:  string="ram kumar reddy"
      print(string.replace('kumar','chandu'))
      result: ram chandu reddy
      
        isalnum()
        
   isalnum() checks whether all characters are alphabetic or numeric.
   alnum = alphabet + number  
   ex:
   text = "Python123"
   print(text.isalnum())    #python 123  is false because their is a space 
     result: true                         #python@123 is false because it's not a letter and number 
     > isalnum() is mainly used to strings  have  letters and  numbers. 
     >if they have numbers and letters it is true otherwise false #if have extra space and unwanted things this is false
     
        lstrip()
 lstrip() removes whitespace from the left side.
 ex:
  text = "   Python"
  print(text.lstrip())
  result: python      #remove the all the left side of the whitespace 
  
         rstrip()
   rstrip() removes whitespace from the right side.
   ex:
   T="python    "
   print(T.rstrip())     #remove the all right side  of the whitespace

          strip()
 strip() removes whitespace from both sides.
 text="        pyt         "
 print(text.strip())                #remove both left and right whitespaces and give output 
      
    isspace()
 isspace() checks whether the string contains only whitespace characters.
 ex:
 text="           "
 print(text.isspace())
 result : true       #if any characters is there in its shows to the fasle if only when strings contain whitespaces then only can output true is there 
     result:pyt


     text="  rre"
     print(text.isspace())  # this is false
     
        casefold()
        
   casefold() converts text into a case-insensitive lowercase form.
  It is similar to lower(), but designed to be more aggressive for case-insensitive comparisons, especially across languages
text = "HELLO PYTHON"
print(text.casefold())
      result: hello python 

 suppose :name1 = "Python"
name2 = "PYTHON"   #when compare both its can comes to true only because of the casefold can converted to lowercase form 

    swapcase()

    > mainly swapcase can use to change  the upper case to lower case and lower case to upper case 
    text = "Hello Python"
    print(text.swapcase())   #hELLO pYTHON

          title()

    title() converts the first character of each word to uppercase.

    in this title can do the every 1st letter of word can make it capital letter

          find()

    find() searches for a substring and returns its position/index.
    text = "I love Python"
    print(text.find("Python")) result: 7 #index can count to the spaces also and python can start of 7 index number 

    text = "I love Python"
    print(text.find("Java"))
    result: -1 # when the substring is not found.

  when its come to index 
     text = "I love Python"
    print(text.index ("Java"))  result : error 
       find()  → -1 if not found
    index() → ValueError if not found    

           count()

    count() counts how many times a substring occurs
    text = "banana"
    print(text.count("a"))  result: 3
    > count() is when a substring or character can chech how many times can repreat

         split()

     split() breaks a string into a list.  
     
     text = "I love Python"
     result = text.split()                 #suppose in after word comma is there na text.split(",")  ("banana,ram,reddy")
        print(result)
        ["I","Love","python"]
        startswith()

        Checks whether a string starts with a particular value.

        text = "Python programming"
        print(text.startswith("Python"))  #true 
        in text all python programming is there so if we put the related that words def it is come to true otherwise false is there 

        string formatting()

      name = "Sriram"
 age = 25
 print(f"My name is {name} and I am {age} years old.") 
 result: my name is sriram and i am 25 years old

 The f tells Python:
"I want to insert variables into this string."

    
