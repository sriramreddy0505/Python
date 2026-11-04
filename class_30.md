               1. What is Pandas?
Pandas is a Python library used for data manipulation, data analysis, and data cleaning.
  Pandas mainly has two important data structures:
1. Series (1D)
2. DataFrame (2D)
   A. What is a Series?
A Series is a one-dimensional labeled array.
It contains only one column of data.
ex:import pandas as pd
data = [10, 20, 30, 40, 50]
s = pd.Series(data)
print(s)
# 0    10
1    20
2    30
3    40
4    50
dtype: int64
           B. What is a DataFrame?
A DataFrame is a two-dimensional labeled data structure consisting of rows and columns.
It looks like an Excel spreadsheet or a database table.
   ex: import pandas as pd

data = {
    "Name": ["Ravi", "Suresh", "Kiran", "Ram"],
    "Age": [21, 22, 20, 23],
    "Marks": [85, 90, 75, 88],
    "City": ["Hyderabad", "Chennai", "Hyderabad", "Bangalore"]
}

df = pd.DataFrame(data)
output:
     Name  Age  Marks        City
0    Ravi   21     85   Hyderabad
1  Suresh   22     90     Chennai
2   Kiran   20     75   Hyderabad
3     Ram   23     88   Bangalore
          4. How to read a CSV file using Pandas
CSV stands for Comma-Separated Values.
A CSV file stores tabular data in a text format where values are generally separated by commas.
read_csv():
- read means load.
- csv means CSV file.
- df stores the loaded dataset.
      5. Data inspection in Pandas
Data inspection means checking and understanding your dataset before performing data analysis
 5.1 head()
head() displays the first five rows by default.
syntax:
df.head()
Why do we use it?
- To check the first records.
- To understand column names.
- To verify whether data loaded correctly.
              5.2 tail()
tail() displays the last five rows by default.
syntax: df.tail()
        5.3 info()
info() gives a summary of your DataFrame.
syntax: df.info()
  mainly info can shows to the Term	Meaning
>RangeIndex	Row index information
>Entries	Total number of rows
>Data columns	Total columns
>Non-Null Count	Number of non-missing values
>Dtype	Data type of each column
>object	Usually text/string data
>int64
   You can identify missing data through info().
             5.4 describe()
describe() provides statistical information about numerical columns.
syntax: df.describe()
      Explanation of each statistic
1. count
Total number of non-missing values.
2. mean
Average value.
3. std
Standard deviation measures how spread out values are from the mean.
4. min
Minimum value.
5. 25%
First quartile (Q1).
6. 50%
Median (middle value).
7. 75%
Third quartile (Q3).
8. max
Maximum value.
print(df)
 5.5 df.dtypes
dtypes displays the data type of every column.
syntax:df.dtypes
          5.6 unique()
unique() returns the distinct values in a column.
syntax:df["columname"].unique()
  Related function: nunique()
nunique() returns the number of unique values.
syntax:df["columname"].nunique()
       maily unique() → Gives unique values.
             nunique() → Gives the count of unique values.
   5.7 memory_usage()
memory_usage() tells us how much memory each column uses.
syntax:df.memory_usage()
  5.8 df.shape
shape returns the number of rows and columns.
syntax:df.shape
        6. Data type conversion in Pandas
Data type conversion means changing one data type into another.
ex:String to integer.
Integer to float.
Float to integer.
String to datetime.
          6.1 astype()
astype() is used to convert the data type of a column.
syntax: df["Age"] = df["Age"].astype("int64")
 6.2 pd.to_numeric()
pd.to_numeric() converts values into numeric data types.
ex:df = pd.DataFrame({
    "Marks": ["85", "90", "75", "88"]
})

df["Marks"] = pd.to_numeric(df["Marks"])

print(df.dtypes)
output:
Marks    int64
      6.3 pd.to_datetime()
Used to convert date columns into datetime format.
This is particularly useful when working with stock market datasets, sales datasets, and time-series data.
              7. Data cleaning in pandas
Data cleaning means identifying and correcting errors, missing values, duplicate records, and inconsistent information in a dataset.
7.1 isnull()
isnull() identifies missing values.
syntax:df.isnull()
 count missing values in each column 
 df.isnull().sum()
   7.2 isnull().any()
any() checks whether at least one value satisfies a condition.
syntax: df.isnull().any()
 df.isnull().any().any()
 Check whether the entire DataFrame has any missing values
 First any() checks each column.
Second any() checks whether any column has missing values.
 7.3 dropna()
dropna() removes rows or columns containing missing values.
syntax:df.dropna()
ex: Important dropna() parameters
A. axis=0
Removes rows containing missing values.
Removes columns containing missing values.
Removes rows only when all values in that row are missing.
7.4 fillna()
fillna() replaces missing values with specified values.
Instead of deleting rows, we can fill missing values.
syntax:df.fillna(value)
fill all missing values using data frame 
df.fillna(0)




