  1. What is a graph?
A graph is a visual representation of data. It helps us understand information easily instead of reading hundreds of rows.
Why do we use graphs?
- To compare players.
- To identify the highest and lowest scores.
- To understand patterns.
- To identify relationships between statistics.
- To make data-driven decisions.
   ex:import matplotlib.pyplot as plt

players = ["Virat", "Rohit", "Gill", "SKY", "Rahul"]
runs = [800, 650, 700, 550, 400]

plt.bar(players, runs)

plt.xlabel("Players")
plt.ylabel("Total Runs")
plt.title("Cricket Players Runs Comparison")

plt.show()
       3. What are subplots?
Subplots mean displaying multiple graphs inside one figure.
For example, instead of creating three separate figures, we can display three graphs together.
Why do we use subplots?
- Compare different statistics together.
- Save screen space.
- Analyze multiple variables.
- Understand player performance in one view.
- syntax:fig, ax = plt.subplots(1, 3)
   Meaning:
- fig = complete figure.
- ax = collection of graph axes.
- 1 = number of rows.
- 3 = number of columns.
    4. Create 3 graphs using subplots
Let's create three different graphs:
- Graph 1: Bar chart – Total runs.
- Graph 2: Line chart – Batting average.
- Graph 3: Scatter plot – Strike rate.
   we have top import to the libraries
 ex:  import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
then create a cricket data set
data = {
    "Player": ["Virat", "Rohit", "Gill", "SKY", "Rahul"],
    "Runs": [800, 650, 700, 550, 400],
    "Average": [57.1, 46.4, 50.0, 39.3, 40.0],
    "Strike_Rate": [140, 155, 135, 180, 125],
    "Half_Centuries": [6, 5, 7, 4, 3]
}

df = pd.DataFrame(data)

print(df)
then create 3 subplots
fig, ax = plt.subplots(1, 3, figsize=(18, 5))

# Graph 1: Bar chart
ax[0].bar(df["Player"], df["Runs"], color="skyblue")
ax[0].set_title("Total Runs")
ax[0].set_xlabel("Players")
ax[0].set_ylabel("Runs")

# Graph 2: Line chart
ax[1].plot(df["Player"], df["Average"],
           marker="o", color="green")
ax[1].set_title("Batting Average")
ax[1].set_xlabel("Players")
ax[1].set_ylabel("Average")

# Graph 3: Scatter plot
ax[2].scatter(df["Player"], df["Strike_Rate"],
              color="red", s=100)
ax[2].set_title("Strike Rate")
ax[2].set_xlabel("Players")
ax[2].set_ylabel("Strike Rate")

plt.tight_layout()
plt.show()
Important: Python indexing starts from zero.
- ax[0] = first graph.
- ax[1] = second graph.
- ax[2] = third graph.
        6. Compare cricket players' statistics
Now let's compare the players using Pandas.
top player:
  top_players = df.nlargest(3, "Runs")
  print(top_players)
  bottom player:
  bottom_players = df.nsmallest(3, "Runs")
   print(bottom_players)
    highest strike rate:print(df.nlargest(3, "Strike_Rate"))
     8. Important axes customization
Matplotlib provides several functions to customize axes.
 ex:plt.figure(figsize=(10, 5))

plt.bar(df["Player"], df["Runs"], color="orange")

plt.xlabel("Player Names")
plt.ylabel("Total Runs")

plt.title("Player Performance")

plt.ylim(0, 1000)
plt.yticks(range(0, 1001, 100))

plt.grid(axis="y", linestyle="--", alpha=0.5)

plt.show()
 Function          	Purpose
plt.xlim()      	Controls X-axis range
plt.ylim()	     Controls Y-axis range
plt.xticks()    	Changes X-axis tick labels
plt.yticks()	   Changes Y-axis tick values
plt.grid()	     Adds grid lines
plt.legend()    	Displays graph labels
plt.figure()	   Creates a figure

