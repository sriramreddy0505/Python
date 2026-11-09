             IMDB data set?
    import pandas as pd

data = {
    "Movie": ["RRR", "Pushpa", "Bahubali",
              "Jersey", "Animal", "KGF"],
    "Genre": ["Action", "Action", "Action",
              "Drama", "Drama", "Action"],
    "Rating": [8.5, 7.6, 8.0, 8.7, 7.8, 8.2],
    "Votes": [10000, 8000, 12000,
              5000, 9000, 11000],
    "Revenue": [500, 300, 600, 200, 400, 550],
    "Year": [2022, 2021, 2015, 2019, 2023, 2018]
}
df = pd.DataFrame(data)
print(df)
Our dataset has 6 rows and 6 columns.
   1. groupby().max()
Meaning: groupby().max() groups the data and finds the maximum value in each group.
Suppose you want to find the highest movie rating in each genre.
    syntax: df.groupby("column_name")["another_column"].max()
EX: df.groupby("Genre")["Rating"].max()
output:
Genre
Action    8.5
Drama     8.7
Name: Rating, dtype: float64
another ex:df.groupby("Genre")["Revenue"].max()
Genre
Action    600
Drama     400
Finding the highest revenue, highest rating, or maximum stock price in each category.
  2. groupby().idxmax()
Meaning: Returns the index of the row containing the maximum value in each group.
Understand the difference:
- max() → Gives the maximum value.
- idxmax() → Gives the index where the maximum value exists.
- ex:result = df.groupby("Genre")["Rating"].idxmax()
     print(result)
  output:
  Genre
Action    0
Drama     3
 when u want to get complete movie details then use loc[] with idxmax()
result = df.groupby("Genre")["Rating"].idxmax()
print(df.loc[result])
output:
Index	Movie	Genre	 Rating
0	    RRR	  Action	8.5
3	   Jersey	Drama	  8.7
  idxmax() does not return the movie name. It returns the row index. Use loc[] to retrieve the complete row.
   3. groupby().size().sort_values()
    Part A: groupby()
Groups rows based on a column.
df.groupby("Genre")
Part B: size()
Counts how many rows exist in each group.
ex:df.groupby("Genre").size()
output:
Genre
Action    4
Drama     2
Action has 4 movies.
Drama has 2 movies.
Part C: sort_values()
Sorts the counts.
df.groupby("Genre").size().sort_values()
output:Genre
Drama     2
Action    4
It sorts from smallest to largest.
for large to sort
df.groupby("Genre").size().sort_values(
    ascending=False
)
output:
Genre
Action    4
Drama     2
4. count()
Meaning: Counts the number of non-null values in a column.
ex:df["Rating"].count()
# 6
count() ignores missing values (NaN).
Function	       Meaning
count()	        Counts non-null values
size	          Counts all elements, including nulls
len(df2)	      Counts DataFrame rows

 5. nunique()
Meaning: Counts how many different values are present in a column.
ex:df["Genre"].nunique() # 2
6. len()
Meaning: len() counts the total number of elements or rows.
ex: len(df) # 6
count characaters in a string
len("Bahubali") # 8

ex: df.groupby("Genre").apply(len)
Genre
Action    4
Drama     2
This applies len() separately to each genre group.
 7. loc[]
Meaning: loc[] selects rows and columns using their labels.
In simple words: If you want particular rows or columns from a DataFrame, use loc[].
select one values
ex:df.loc[0, "Movie"]  # RRR
0 → Row index.
"Movie" → Column name.
and update a value
ex:df.loc[df["Movie"] == "RRR", "Rating"] = 9.0
Now RRR's rating becomes 9.0.
Important: loc[] is very useful for selecting, filtering, and updating DataFrame values.
 9. query()
Meaning: query() retrieves rows based on a condition.
ex:df.query("Rating > 8")
another ex: df.query("Genre == 'Action'")
it returns all action movies
10. query() with two conditions
This is particularly important in EDA.

Sometimes you want to check two conditions at the same time.

There are two important operators:
- and → Both conditions must be true.
- or → At least one condition must be true.
    two conditions using of AND
  df.query("Rating > 8 and Votes > 9000")
   Genre and rating
Find Action movies with ratings greater than 8.
df.query("Genre == 'Action' and Rating > 8")
 11. str.lower()
Meaning: Converts all text in a column into lowercase letters.
ex:"HELLO" → "hello"
"Action" → "action"
"DRAMA" → "drama"
df3["Genre"].str.lower()
Pandas may treat these as different values because capitalization differs.
 df3["Genre"] = df3["Genre"].str.lower()
Now all values become lowercase.
 12. str.upper()
Meaning: Converts all text into uppercase letters.
 df3["Genre"].str.upper()
 13. str.contains()
Meaning: Checks whether a particular word or character exists inside a string.
It returns Boolean values: True or False.
ex: df3["Movie"].str.contains("R")
output: 0     True
1    False
2    False
3    False
 RRR contains R.
PUSHPA doesn't contain R.
Bahubali doesn't contain R.
JERSEY doesn't contain R.
 anotehr ex: df3[df3["Movie"].str.contains("R|P")]
 Find movies containing either R or P
 14. str.replace()
Meaning: Replaces an existing character or word with another character or word.
syntax: df["column"].str.replace("old", "new")
ex:  df3["Movie"].str.replace("PUSHPA", "PUSHPA 2")
output:
0         RRR
1     PUSHPA 2
2    Bahubali
3      JERSEY
  and replace spaces
  names = pd.Series(["Bahubali 2", "Pushpa 2", "RRR"])

names.str.replace(" ", "_")
output:
0    Bahubali_2
1      Pushpa_2
2           RRR
15. str.len()
Meaning: Counts the number of characters in each string.
df["Movie"].str.len()	Character count for each movie name
df3["Movie"].str.len()
