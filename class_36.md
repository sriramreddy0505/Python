                      IMDB  movie data set?
                        import pandas as pd

data = {
    "Movie": ["RRR", "Pushpa", "Bahubali",
              "Jersey", "Animal", "KGF"],

    "Genre": ["Action", "Action", "Action",
              "Drama", "Drama", "Action"],

    "Rating": [8.5, 7.6, 8.0, 8.7, 7.8, 8.2],

    "Votes": [10000, 8000, 12000, 5000, 9000, 11000],

    "Revenue": [500, 300, 600, 200, 400, 550],

    "Year": [2022, 2021, 2015, 2019, 2023, 2018]
}
df = pd.DataFrame(data)
print(df)
and data set contain 6 movies and 6 columns.
         1. nlargest()
Meaning: nlargest() returns the N largest values from a particular column.
In simple words: Find the top-rated movies.
 syntax:df.nlargest(number, "column_name")
 ex:df.nlargest(3, "Rating")
 output:
 Index	Movie 	Rating
 3	     Jersey	8.7
 0	      RRR 	8.5
 5      	KGF	  8.2
 ex with index :
 result = df.nlargest(3, "Rating")
print(result.index)
# Index([3, 0, 5], dtype='int64')
 df.nsmallest(3, "Rating") find the top 3 lowest movies and using of the rating
                     2. nunique()
 Counts how many different or unique values exist in a column.
 ex:df["Genre"].nunique() # 2
  because Our genres are:
- Action
- Drama
There are only two different genres.
            Difference between unique() and nunique()
  ex:df["Genre"].unique()
  # ['Action' 'Drama']
  This returns the actual unique values.
  ex:df["Genre"].nunique()
  # 2
  This returns the number of unique values.
  value_counts =Counts frequency of each value
      3. groupby()
 groupby() divides the dataset into different groups based on a column.
   Group 1 → Action movies
  Group 2 → Drama movies
  syntax: df.groupby("column_name")
              ex:df.groupby("Genre")["Rating"].mean()
    Genre
Action    8.075
Drama     8.250
 ex: df.groupby("Genre")["Revenue"].sum()
Genre
Action    1950
Drama      600
This calculates total revenue for each genre.
 4. groupby().idxmax()
Meaning: Returns the index of the row containing the maximum value in each group.
In simple words: Find the highest-rated movie in every genre and return its index.
  ex:
  result = df.groupby("Genre")["Rating"].idxmax()
  print(result)
  # Genre
Action    0
Drama     3
 explanation:Action → Highest rating is 8.5 (RRR), index 0.
    Drama → Highest rating is 8.7 (Jersey), index 3.
    mainly :
    max() returns the maximum value.
   idxmax() returns the index where the maximum value occurs.
   ex:df["Rating"].max()  #8.7
   ex: df["Rating"].idxmax() # 3
    5. groupby().idxmin()
    Returns the index of the minimum value in each group.
    ex:result = df.groupby("Genre")["Rating"].idxmin()
    print(result)
    # Genre
     Action    1
     Drama     4
Explanation:
- Action → Pushpa has the lowest rating (7.6), index 1.
- Drama → Animal has the lowest rating (7.8), index 4.
       6. groupby().filter()
Meaning: Filters complete groups based on a condition.
Suppose you want only genres that have more than two movies.
   ex:result = df.groupby("Genre").filter(
    lambda x: len(x) > 2
)
print(result)
# Movie	   Genre	  Rating
  RRR	     Action	  8.5
  Pushpa 	 Action	  7.6
  Bahubali	Action	 8.0
  KGF     	Action
explanation: 
Action has 4 movies.
Drama has 2 movies.
Our condition is len(x) > 2.
Therefore, only Action is returned.
in given condition mainly can play the role is ;
     lambda x: len(x) > 2
- lambda → Creates a small anonymous function.
- x → Represents one group.
- len(x) → Counts rows in that group.
- > 2 → Checks whether the group contains more than two rows.
  Remember: filter() keeps or removes the entire group, not just individual rows.
           7.genres.value_counts()
  >  ex:genres.value_counts()
  > Action    4
Drama     2
Name: count, dtype: int64
  > Meaning: Counts how many times each genre appears.

For example:
- Action appears 4 times.
- Drama appears 2 times.
   9. genres.size and groupby().size()
Meaning: size counts the total number of elements or rows.
  ex:genres = df["Genre"]
  print(genres.size)   # 6
  ex:df.groupby("Genre").size()
  # Genre
Action    4
Drama     2
count() → Counts non-null ratings.
size() → Counts all rows in each group, including rows with missing ratings.
 10. sort_values()
Meaning: Sorts data in ascending or descending order.
ex: df.sort_values("Rating")
# This arranges ratings from lowest to highest.
and highest rating ex: df.sort_values("Rating", ascending=False)
 ascending=True → Smallest to largest.
 ascending=False → Largest to smallest.
  sort group ex:
  df.groupby("Genre").size().sort_values()
  # Genre
  Drama     2
  Action    4
It sorts the number of movies in each genre from lowest to highest.
  for decending order:
  df.groupby("Genre").size().sort_values(
    ascending=False
)
output:Genre
Action    4
Drama     2
    11.query()
Meaning: query() filters rows based on a condition.
syntax:df.query("condition")
ex:df.query("Rating < 8")
output:
Movie	Rating
Rating
Pushpa	7.6
Animal	7.5
another ex: with 2 conditions
df.query("Rating > 8 and Votes > 9000")
Movie	   Rating  	   Votes
RRR	      8.5        	10000
Bahubali	8.0	        12000
KGF	      8.2	        11000
Notice that Bahubali is excluded because its rating is exactly 8, not greater than 8.
another ex: Movies with either high rating or high revenue
 df.query("Rating > 8.5 or Revenue > 550")
     13. agg()
Meaning: agg() means aggregation.

It allows us to apply one or multiple statistical functions to columns.

For example, you want:
- Average rating
- Maximum rating
- Minimum rating
- Total revenue
- Average votes
 Instead of writing separate code for everything, use agg().
multiple calucalation for one column:
df["Rating"].agg(["mean", "max", "min", "median"])
