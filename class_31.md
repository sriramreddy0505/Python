               DATA CLEANING():
   2. What is interpolate() in Pandas?
Definition: interpolate() is a Pandas function used to fill missing values (NaN) by estimating values based on surrounding data.
 ex: marks = [10, 20, np.nan, 40, 50]
The missing value is between 20 and 40.
Pandas can calculate the missing value using interpolation.
syntax: df.interpolate()
df1 = pd.DataFrame({
    "Marks": [10, 20, np.nan, 40, 50]
})

print(df1.interpolate())
 #  Marks
0   10.0
1   20.0
2   30.0
3   40.0
4   50.0
 3. What is drop_duplicates()?
Definition: drop_duplicates() removes repeated or duplicate rows from a DataFrame.
We can remove duplicate records.
syntax:df.drop_duplicates()
and when we want to the 1st value from duplicates we have to write df.drop_duplicates(keep="first")
if last na df.drop_duplicates(keep="last")
if i want to remove all duplicates na df.drop_duplicates(keep=False)
and when we want to check the only duplicates inside of subset for paarticular values df.drop_duplicates(subset=["Name"])
#df.duplicated()	Identifies duplicate rows
#df.drop_duplicates()	Removes duplicate rows
  4. What is replace()?
Definition: replace() is used to replace existing values with new values in a DataFrame.
ex: df["r"] = df["r"].replace("Py", "Python") and in this after replacing can write "py" instead of "python"
     5. Changing data types in multiple columns
     Convert multiple columns
Suppose you want to convert Age and Experience to integers.
Converting a column containing NaN directly to ordinary int64 will cause an error. You can use Pandas nullable integer type Int64 (capital I).
 errors="coerce" converts invalid values into NaN.
 errors="raise" raises an error when conversion fails.
       6. What is rename()?
Definition: rename() is used to change column names or index names in a DataFrame.
ex:Student_Name, Student_Age, Monthly_Salary
df.rename(columns={
    "Name": "Student_Name",
    "Age": "Student_Age",
    "Salary": "Monthly_Salary"
}, inplace=True)
 rename() changes selected names.
df.columns can replace all column names.
        INDEXING AND VALUES:
        8. What is indexing?
Definition: Indexing means identifying and accessing individual rows or records using their index labels or positions.
   What is values?
values returns the underlying data as a NumPy array.
 print(df.values)
  df.index gives index labels.
  df.columns gives column names.
 df.values gives the underlying data array.
   9. What is set_index()?
Definition: set_index() changes an existing column into the DataFrame index.
  ex:df.set_index("Name", inplace=True)
           10. What is reset_index()?
Definition: reset_index() changes the existing index back into a normal column and creates a new numerical index.
 df.reset_index(inplace=True)
      like this   
      Name   Age  Salary
0  Sriram   22   25000
1  Ravi     25   30000
2  Kiran    24   35000
3  Raju     28   40000
drop=True removes the old index instead of adding it as a column.
 - set_index() converts a column into an index.
- reset_index() converts the existing index back into a column (unless drop=True).
  
