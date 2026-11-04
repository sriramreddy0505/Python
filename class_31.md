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
  
       11. MultiIndex
Meaning: MultiIndex means having more than one index level.
In simple words, you can use multiple columns together as an index.
           12.df.loc[]
Meaning: Selects rows and columns using index labels and column names.
df.loc[row_label, column_label]
ex:print(df.loc[0])
Returns the first row (index label 0).
Important: loc includes the ending label when slicing.
loc means Location based on labels.
It is used to select particular rows and columns using their labels.
In simple words, if you want to get one  row's information or only the Salary column, you can use loc.
       13. df.iloc[]
Very important
What is iloc?
iloc means Integer Location.
It selects rows and columns based on their numerical positions.
Remember:
- loc = Labels.
- iloc = Positions.
- syntax:df.iloc[row_position, column_position]
- ex: select 1st row
- print(df.iloc[0])
then we can got the index of 0 both columna and rows
   14. df.at[]
What is at?
at is used to access one particular cell using row and column labels.
It is similar to loc, but it is specifically designed for accessing a single value.
syntax:df.at[row_label, column_label]
When do we use at?
When we want to read or update just one particular cell using labels.
         18. df.iat[]
What is iat?
iat is used to access one particular cell using integer positions.
It is similar to iloc, but it is designed for accessing one value.
syntax:df.iat[row_position, column_position]
        19. df.query()
What is query?
query() is used to filter rows based on conditions.
In simple words, suppose you have 1000 employee records, but you want only employees whose salary is greater than ₹30,000.
You can use query().
syntax:df.query("condition")
When do we use query()?
- Employee salary analysis.
- Student marks analysis.
- Stock market data filtering.
- Sales data analysis.
-  20. df.filter()
What is filter?
filter() is used to select specific rows or columns based on their labels.
Important: filter() does not filter rows based on conditions like Age greater than 25.
select one row
print(df.filter(items=["Name"]))
