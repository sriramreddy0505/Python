             1.What is data visualization?
Data visualization means representing data using graphical formats instead of only reading numbers and tables.
Scatter plot

Shows relationships between two numerical variables.
Shows proportions of a whole.
Why do we use visualization?
1. Understand data easily.
2. Find patterns.
3. Identify outliers.
4. Compare categories.
5. Understand distributions.
6. Support Machine Learning decisions.
    2. What is a histogram?
A histogram is a graph that shows the frequency distribution of numerical data.
A histogram tells us how many values fall within a particular range.
basic histogram:
 plt.hist(df["sepal length (cm)"])
 plt.show()
 What happens?
- X-axis displays sepal length.
- Y-axis displays frequency.
- Bars show how many flowers fall into each interval.
          ex:change the number of bins
  plt.hist(
    df["sepal length (cm)"],
    bins=10
  )
plt.xlabel("Sepal Length")
plt.ylabel("Frequency")
plt.title("Sepal Length Distribution")
plt.show()
ex:
It divides the data range into 10 intervals.
- Fewer bins: Less detail.
- More bins: More detail.
           ex: change histogram colors
  plt.hist(
    df["sepal length (cm)"],
    bins=15,
    color="skyblue",
    edgecolor="black"
)

plt.title("Iris Sepal Length Histogram")
plt.xlabel("Sepal Length")
plt.ylabel("Frequency")

plt.show()
color: Fills the bars.
edgecolor: Changes the border color.
bins: Controls the number of intervals.
   When do we use histograms?
- Understanding numerical data.
- Finding data distribution.
- Detecting unusual values.
- Understanding whether data is symmetric or skewed.
- Comparing numerical distributions.
     Remember: Histogram is mainly for continuous numerical data, not for counting categories.
       3. What are categories and values?
These two concepts are very important in Pandas and visualization.
  A. Categories
Categories represent different groups or labels.
ex:df["species"]
 B. Values
Values are the actual observations stored in a column.
6. What is a bar plot?
A bar plot is a visualization that compares different categories using rectangular bars.
ex: species_count = df["species"].value_counts()

plt.bar(
    species_count.index,
    species_count.values
)

plt.xlabel("Species")
plt.ylabel("Count")
plt.title("Iris Species Count")

plt.show()
explanation:
Code	                 Meaning
species_count	       Stores category counts
.index	            Gets category names
.values            	Gets numerical counts
plt.bar()	           Creates a bar chart
plt.xlabel()        	Sets X-axis label
plt.ylabel()        	Sets Y-axis label
plt.title()	           Sets chart title
   ex: horizantaal bar:
   plt.barh(
    species_count.index,
    species_count.values,
    color="purple"
)

plt.xlabel("Count")
plt.ylabel("Species")
plt.title("Horizontal Bar Plot")

plt.show()
      4. What is composition in data visualization?
Composition means understanding how different parts contribute to a complete dataset or total.
For example, our Iris dataset contains 150 flowers.
- Setosa = 50
- Versicolor = 50
- Virginica = 50
Each species contributes to the total of 150 flowers.
    5. Top values and bottom values
In Data Science, we frequently use top and bottom values to understand the highest and lowest observations.
ex: sequel length:
df.nlargest(5, "sepal length (cm)")
         6. Top colors and bottom colors
You can also highlight the highest and lowest values using different colors in one chart.
top_5 = df.nlargest(5, "petal length (cm)")
bottom_5 = df.nsmallest(5, "petal length (cm)")

combined = pd.concat([top_5, bottom_5])

colors = [
    "green" if value in top_5["petal length (cm)"].values
    else "red"
    for value in combined["petal length (cm)"]
]

plt.bar(
    range(len(combined)),
    combined["petal length (cm)"],
    color=colors
)

plt.title("Top and Bottom Petal Lengths")
plt.xlabel("Observations")
plt.ylabel("Petal Length")

plt.show()
 Green = Top values.
 Red = Bottom values.
 
