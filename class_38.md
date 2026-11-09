     1.startswith() in Python
What is startswith()?
startswith() is a built-in Python string method.
It checks whether a string starts with a particular character or word.
syntax:string.startswith("value")
ex:name = "Python Developer"
result = name.startswith("Python")
print(result)
output:
True
another ex:
name = "Python Developer"
print(name.startswith("Java"))
output: false
Because the string starts with Python, not Java.
  Using startswith() in Pandas
Suppose you have a DataFrame:
 ex: import pandas as pd
df = pd.DataFrame({
    "Name": ["Sriram", "Ravi", "Srikanth", "Kiran"],
    "Salary": [25000, 30000, 35000, 20000]
})
result = df[df["Name"].str.startswith("S")]
print(result)
output:
       Name  Salary
0    Sriram   25000
2  Srikanth   35000

   Real-time applications:
- Finding files starting with a particular name.
- Filtering employee names.
- Checking product codes.
- Filtering email prefixes.
- Finding specific categories in datasets.
    2. strip() in Python
What is strip()?
strip() is a Python string method.
It removes unwanted spaces or specified characters from both the beginning and ending of a string.
It does not remove spaces between words.
syntax: string.strip()
ex: remove spaces
name = "   Sriram   "
result = name.strip()
print(result)
output:
sriram
 another ex: Removing specified characters
name = "###Python###"
print(name.strip("#"))
output:
Python
         3. lstrip() in Python
What is lstrip()?
lstrip() means Left Strip.
It removes unwanted spaces or specified characters only from the left side (beginning) of a string.
  syntax: string.lstrip()
  ex:name = "     Sriram     "
          result = name.lstrip()
          print(result)
 output: Sriram
Explanation:
- Left-side spaces are removed.
- Right-side spaces remain.
    4. rstrip() in Python
What is rstrip()?
rstrip() means Right Strip.
It removes unwanted spaces or specified characters only from the right side (ending) of a string.
syntax: string.rstrip()
ex:   name = "     Sriram     "
     result = name.rstrip()
     print(result)
  output:
   "    Sriram"
  Right-side spaces are removed.
 Left-side spaces remain.
 5. get() in Python
What is get()?
get() is a dictionary method.
It retrieves the value associated with a particular key.
syntax:dictionary.get(key)
ex:student = {
    "name": "Sriram",
    "age": 22,
    "course": "Python"
}
print(student.get("name"))
print(student.get("age"))
output:
Sriram
22
mainly:
"name" is the key.
"Sriram" is its value.
get("name") retrieves the value.
if suppose i am using salary instead of age it will be return to the "none" Because the dictionary does not contain the key "salary".
When working with employee records, customer details, API responses, or JSON data, some keys may be missing. get() helps avoid errors.
     6.What is a list of dictionaries?
A list of dictionaries means storing multiple dictionaries inside one list.
Each dictionary can represent one record, such as one employee, customer, student, or product.
ex:  employees = [
    {
        "name": "Sriram",
        "age": 22,
        "salary": 25000
    },
    {
        "name": "Ravi",
        "age": 24,
        "salary": 30000
    },
    {
        "name": "Kiran",
        "age": 25,
        "salary": 35000
    }

]
output:
employees = List.
Each {} = Dictionary.
"name", "age", "salary" = Keys.
"Sriram", 22, 25000 = Values.
7. pd.read_csv() in Pandas
What is pd.read_csv()?
read_csv() is a Pandas function used to read data from a CSV file and convert it into a DataFrame.
CSV stands for Comma-Separated Values.
A CSV file stores data in rows and columns.
syntax: pd.read_csv("file_name.csv")
ex:df = pd.read_csv("employees.csv", sep=";")
Here, sep=";" tells Pandas that the separator is a semicolon instead of a comma.

Real-time applications:
- Reading company employee data.
- Reading stock market datasets.
- Reading customer records.
- Reading agricultural datasets.
- Loading datasets for machine learning.
      8. pd.read_html() in Pandas
What is read_html()?
pd.read_html() is a Pandas function that extracts tabular data from HTML tables.
HTML stands for HyperText Markup Language.
Websites use HTML to display information such as:
- Tables
- Headings
- Paragraphs
- Links
- Images
For example, a website might contain a table showing company names, prices, and locations.
read_html() can extract those HTML tables and convert them into Pandas DataFrames.
syntax:pd.read_html("URL or HTML file")
ex: import pandas as pd
tables = pd.read_html("employees.html")
print(tables[0])
output:
Name	Age	Salary
0	Sriram	22	25000
1	Ravi	24	30000
read_html() returns a list of DataFrames, because an HTML page can contain multiple tables.
     9. What is an HTML file?
Meaning of HTML
HTML stands for HyperText Markup Language.
It is the standard markup language used to structure webpages.
HTML is not a programming language like Python. It describes the structure and content of a webpage.
  and mainly basic html structure is the
  <!DOCTYPE html>

<html>

<head>
    <title>Employee Details</title>
</head>

<body>

    <h1>Employee Information</h1>

    <table border="1">

        <tr>
            <th>Name</th>
            <th>Age</th>
        </tr>

        <tr>
            <td>Sriram</td>
            <td>22</td>
        </tr>

        <tr>
            <td>Ravi</td>
            <td>24</td>
        </tr>

    </table>
</body>
</html>

10. enumerate() in Python
What is enumerate()?
enumerate() is a built-in Python function.
It allows you to access two things simultaneously when looping:
1. Index (position)
2. Value (actual element)
enumerate(iterable, start=0)
iterable = List, tuple, string, etc.
start = Starting index. Default is 0.
normal for loop:
names = ["Sriram","Ravi","Kiran"]
for name in names:
    print(name)
 output:
Sriram
Ravi
Kiran
and using enumerate():
names = ["Sriram", "Ravi", "Kiran"]
for index, name in enumerate(names):
     print(index, name)
   output:
   0 Sriram
1 Ravi
2 Kiran
  another ex:
names = ["Sriram", "Ravi", "Kiran"]
for index, name in enumerate(names, start=1):
   print(index, name)
output:
Why start=1?
Because we want numbering to begin at 1 instead of 0.
  11. df.to_excel() in Pandas
What is to_excel()?
to_excel() is a Pandas DataFrame method used to export or save DataFrame data into an Excel file.
creating an excel file
import pandas as pd

data = {
    "Name": ["Sriram", "Ravi", "Kiran"],
    "Age": [22, 24, 25],
    "Salary": [25000, 30000, 35000]
}

df = pd.DataFrame(data)
df.to_excel("employees.xlsx", index=False)

Now an Excel file named employees.xlsx will be created.
What is index=False?
Normally, Pandas saves the DataFrame index as an additional Excel column.
