     1. What is Matplotlib?
Matplotlib is a Python library used for data visualization.
Data visualization means representing data in graphical format,
 Instead of reading all the numbers, you can create a graph to understand the marks easily.
  ex:import matplotlib.pyplot as plt
students = ["A", "B", "C", "D", "E"]
marks = [70, 85, 60, 95, 80]
plt.plot(students, marks)
plt.show()
explanation:
matplotlib – visualization library.
pyplot – module used to create plots.
plt – short name (alias).
plot() – creates a line plot.
show() – displays the graph.
 2. What is a Figure and Axes?
 Figure: The complete canvas or window where your visualization is created.
 Axes: The actual plotting area inside the figure.
  import matplotlib.pyplot as plt
fig, ax = plt.subplots()
ax.plot([1, 2, 3, 4], [10, 20, 30, 40])
plt.show()
output:
fig = complete figure.
ax = plotting area.
subplots() = creates a figure and one or more axes.
 Remember:
Figure = Complete canvas
Axes = Actual graph area
 4. What is a Scatter Plot?
A Scatter Plot is a graph that represents the relationship between two numerical variables using individual dots.
For example:
- X-axis = Hours studied
- Y-axis = Marks obtained
import matplotlib.pyplot as plt
hours = [1, 2, 3, 4, 5, 6]
marks = [30, 40, 50, 60, 75, 90]
plt.scatter(hours, marks)
plt.xlabel("Hours Studied")
plt.ylabel("Marks")
plt.title("Hours vs Marks")
plt.show()
    5. How to change Scatter Plot colors
You can customize your scatter plot using different colors.
ex:import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]
plt.scatter(
    x, y,
    color="red",
    s=100,
    marker="o",
    alpha=0.7
)
plt.title("Scatter Plot")
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.show()
explanation:
color="red" – changes dots to red.
s=100 – controls dot size.
marker="o" – circular markers.
alpha=0.7 – 70% opacity.
                6. What is Marker in Matplotlib?
A marker changes the shape of each data point.
plt.scatter(x, y, marker="o")
ex:plt.scatter(x, y, marker="*", color="green", s=150)
plt.show()
 8. What is the Iris Dataset?
The Iris dataset is one of the most popular datasets
 It contains measurements of three flower species.
 The three classes are:
1. Setosa
2. Versicolor
3. Virginica
The dataset contains 150 records and 5 columns.
Why do we use Iris?
- To understand data visualization.
- To learn scatter plots.
- To understand relationships between features.
- To practice classification.
- To learn ML algorithms such as KNN, Decision Tree and Logistic Regression.
    9. Iris Dataset – Complete Scatter Plot Project
  we have to import libraries
  import pandas as pd
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris
load iris dataset:
iris = load_iris()
df = pd.DataFrame(
    iris.data,
    columns=iris.feature_names
)
df["species"] = iris.target
print(df.head())
explanation:
load_iris() – loads the Iris dataset.
iris.data – contains four numerical features.
iris.feature_names – contains feature names.
DataFrame() – converts the data into a Pandas DataFrame.
iris.target – contains numerical class labels.
      "Change colors according to species"
This is one of the most important parts of data visualization.
We want:
- Setosa = Red
- Versicolor = Green
- Virginica = Blue
  ex:colors = {
    "Setosa": "red",
    "Versicolor": "green",
    "Virginica": "blue" 
}

for species, color in colors.items():

    subset = df[df["species"] == species]
      plt.scatter(
        subset["sepal length (cm)"],
        subset["sepal width (cm)"],
        color=color,
        label=species,
        s=60
    )

plt.xlabel("Sepal Length (cm)")
plt.ylabel("Sepal Width (cm)")
plt.title("Iris Species Scatter Plot")
plt.legend()
plt.show()
 10. What is plt.figure()?
plt.figure() creates a new figure (canvas) for your graph.
plt.figure(figsize=(10, 6))
