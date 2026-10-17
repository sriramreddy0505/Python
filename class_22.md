                           1. What is file handling in Python?
File handling means performing operations on files using Python.
For example, imagine you want to store student details, sheep farm records, or employee information.
Instead of storing everything inside variables, you can save the data in a file and access it whenever you need it
explanation:
Common file operations:
- Open a file.
- Read data from a file.
- Write data to a file.
- Append new data to a file.
- Close a file.

   2. How to open a file using open()
Python provides the built-in open() function to open files.
syntax:
file = open("filename.txt", "mode")
ex:
file = open("sample.txt", "r")
print(file.read())
file.close()
Important: The file must exist when you use "r". Otherwise, Python raises a FileNotFoundError.

3. How to read a file
Suppose sample.txt contains the following text:
mainly it can helpful to the
Mode	Meaning
"r"	Read an existing file
"w"	Write to a file; replaces existing content
"a"	Append content to the end of a file
"x"	Create a new file; raises an error if it already exists
"rb"	Read a file in binary mode
"wb"	Write a file in binary mode
"r+"	Read and write without initially truncating the file

and mainly open() opens the file.
file.read() reads the contents.
print(data) displays the contents.
file.close() closes the file.

You can also specify how many characters to read:
file = open("sample.txt", "r")
print(file.read(6))file.close()
Output:
Python

     4. The readline() method reads one line at a time.
   here ex: file = open("sample.txt", "r")

print(file.readline())
print(file.readline())

file.close()
output:
Python is easy to learn.
Python is a programming language.

        5.  The readlines() method reads all lines and returns them as a list of strings.
    ex:   file = open("sample.txt", "r")

lines = file.readlines()

print(lines)

file.close()
output:
[
    'Python is easy to learn.\n',
    'Python is a programming language.\n',
    'I am learning file handling.'
]
The \n represents a newline character.

and mainly it can;
read() — read all contents as one string.
readline() — read one line at a time.
readlines() — read all lines into a list.
for line in file — process lines individually, especially in large files.

       6. Writing multiple lines using writelines()
The writelines() method writes multiple strings from an iterable, such as a list.
ex:
file = open("subjects.txt", "w")

subjects = [
    "Python\n",
    "Machine Learning\n",
    "Data Science\n"
]

file.writelines(subjects)

file.close()
output:
Python
Machine Learning
Data Science

Notice that writelines() does not automatically add newline characters. We included \n in each string.
             7. How to close a file using close()
The close() method closes an opened file.

ex: file = open("sample.txt", "r")

data = file.read()
print(data)

file.close()

and mainly we can close to the file means 
It releases system resources.
It helps ensure pending writes are finalized.
It prevents you from accidentally continuing to use a file that should no longer be open.

Use with open()
Python provides a safer and cleaner way to handle files: the with statement.


    8. What is a module in Python?
A module is a Python file (.py) that contains reusable code, such as functions, variables, and classes.
For example, you could create one file for mathematical operations and another file to use those operations.
Benefits of modules:
- Reuse code in multiple programs.
- Organize large projects into smaller files.
- Make code easier to maintain.
- Avoid rewriting the same functions repeatedly.

       9. Import specific functions using from ... import
You do not always need to write the module name before a function.
from mymodule import add, subtractprint(add(20, 10))print(subtract(20, 10))
Output:
30
10
Here, only the add and subtract functions are imported.

          10.Import a module using an alias
An alias is an alternative name for a module.
Syntax:
import module_name as alias
Example:
import mymodule as mmprint(mm.add(7, 3))
Output:
10
Here, mm is an alias for mymodule.
