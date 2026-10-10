  introduction of if, elif, else;
  
  >In Python, if, elif, and else are used for decision-making.
  >A program often needs to make decisions based on a condition.

  number=18
if number>=18:
  print("adult")
else:
  print("not available for vote")         # more than or equal to 18 is available to vote 
  
    what is a condition?

  a condition is a expression that produces either true or false
  per ex: age = 20 
          age >= 18  result is true 
          
    if statement 
    
  The if statement executes a block of code only when the condition is True.  
  syntax:
  if condition:
  statement                        #if the condition is true then only execute the code 

  After the condition, we use a colon:

if age >= 18:
The colon tells Python that a block of code is starting.

Correct:
if age >= 18:
    print("Eligible")

Incorrect:
if age >= 18
    print("Eligible")

Python uses indentation to identify which statements belong to the if block.

Correct:
age = 20
if age >= 18:
    print("Eligible")
The print() statement is indented.
                                         #mainly indentation can use to identify the if block code in python and given to                                               the  4 spaces before print()
Usually, Python uses 4 spaces.

Incorrect:
age = 20
if age >= 18:
print("Eligible")
This causes an indentation error.


     else Statement

else is used when the if condition is False.
Syntax
if condition:
    statement
else:
    statement                #when the if condition is false then use the else 

Example:
age = 15
if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")
Output:
Not eligible to vote


else if

We use elif when we want to check multiple conditions.

Syntax
if condition1:
    statement
elif condition2:
    statement
else:                                  #when if condition is false then use the else if (when we have multiple conditions )
    statement

Example:
marks = 75
if marks >= 90:
    print("Grade A")
elif marks >= 60:
    print("Grade B")
else:
    print("Grade C")
Output:
Grade B

and mainly we can use mandatory of it condition and some times we use elif instead of else and we have use many elifs based on condition and in those conditions only one condition is true .
either if or elif and else in those conditions only one statement is true.

          Nested if ?
An if statement inside another if statement is called a nested if statement.   
syntax:
if condition1: 
  if condition2:
    statement

    
  if condition1 is True:
       check condition2
       if condition2 is True:
        execute statement

    The inner if is checked only when the outer if condition is True
Both conditions need to be True for the innermost statement to execute. 

ex:#nested if 
n=int(input("enter a number:"))
if n>=18:
  print("person hase id ")
  b=input("do u have an id :")
  if b=="yes": 
    print("entry allow")
  else:
    print("id required")  
else:
  print("not aligible")  
