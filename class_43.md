   1. What is a Bar Chart?
A Bar Chart is a data visualization technique used to compare different categories using rectangular bars.
For example, imagine we have 8 cricket players and want to compare their total runs.
A bar chart helps us understand which player scored more runs and which player scored fewer runs.
 Why do we use bar charts?
1. Comparing different players.
2. Identifying top-performing players.
3. Identifying bottom-performing players.
4. Comparing batting averages.
5. Comparing strike rates.
6. Comparing half-centuries and centuries.
   2.Understanding Top Players
Top players means players who have achieved the highest values in a particular performance metric.
ex:Top runs = highest runs.
Top average = highest batting average.
Top strike rate = highest strike rate.
Top half-centuries = highest number of 50s.
ex:plt.figure(figsize=(9, 5))

plt.bar(top_players["Player"], top_players["Runs"])

plt.title("Top 5 Cricket Players by Runs")
plt.xlabel("Players")
plt.ylabel("Total Runs")

plt.show()
ex;bottom_players = df.nsmallest(3, "Runs")
Meaning of nsmallest():
- n = number of records.
- smallest = lowest values.
- "Runs" = column to check.
        nlargest() = highest values.
        nsmallest() = lowest values.
You can use both functions for runs, average, strike rate, half-centuries and centuries.
  3. Understanding Bottom Players
Bottom players means players who have the lowest values in a selected metric.
ex:bottom_players = df.nsmallest(3, "Runs")

print(bottom_players)
 4. Understanding Player Indexing
Indexing means accessing a particular row or column from a dataset.
  part A: set players name as the index:
  df = df.set_index("Player")
    print(df)
Now player names become the index instead of 0, 1, 2, 3...
   B. Using loc[]
loc[] selects rows using their labels.
 print(df.loc["Virat"])
This displays all information about Virat.
 C. Using iloc[]
iloc[] selects rows using their integer positions.
print(df.iloc[0])
             4. Comparing Strike Rate and Batting Average
This is an important cricket analysis topic.
What is batting average?
Batting average tells us how many runs a player scores per dismissal.

Formula:
\[
Average = \frac{Total\ Runs}{Dismissals}
\]

For example:
- Total runs = 600
- Times dismissed = 12
\[
Average = \frac{600}{12}=50
\]

The batting average is 50.

What is strike rate?

Strike rate tells us how quickly a batsman scores runs.
Formula:
\[
SR = \frac{Runs}{Balls\ Faced}\times100
\]

Example:
- Runs = 150
- Balls = 100
\[
SR = \frac{150}{100}\times100=150
\]
The strike rate is 150.
  ex: compare strike rate using bar chat
  plt.figure(figsize=(10, 5))

plt.bar(
    df.index,
    df["Strike_Rate"],
    color="blue"
)

plt.title("Player Strike Rate Comparison")
plt.xlabel("Players")
plt.ylabel("Strike Rate")

plt.show()
 5. Pie Chart in Matplotlib
A pie chart is used to show how different categories contribute to a total.
basic pai chat ex:plt.figure(figsize=(8, 8))

plt.pie(
    df["Runs"],
    labels=df.index,
    autopct="%1.1f%%"
)

plt.title("Player Run Contribution")

plt.show()
 Parameter    	Meaning
df["Runs"]	     Values used for pie slices
labels          	Names of players
autopct         	Displays percentages
%1.1f%%	          Displays percentage with one decimal
plt.title()	      Adds title
 6. What is Explode in a Pie Chart?
Explode means separating one or more slices from the main pie chart.
ex:explode = [0.1, 0, 0, 0, 0, 0, 0, 0]

plt.figure(figsize=(8, 8))

plt.pie(
    df["Runs"],
    labels=df.index,
    autopct="%1.1f%%",
    explode=explode,
    shadow=True,
    startangle=90
)

plt.title("Player Run Contribution with Explode")
plt.show()
