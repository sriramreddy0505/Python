             1. Types of data in statistics
             (quantitative)
             1.1 Discrete data
Definition: Discrete data is numerical data that contains separate, countable values. It usually comes from counting something.
Number of students in a classroom.
Number of sheep on a farm.
Number of employees in a company.
Number of products sold.
Number of cars in a parking area.
and 
Discrete data is countable.
Usually represented by integers.
Can have zero.
Often visualized using bar charts.
         1.2 Continuous data
Definition: Continuous data is numerical data that can take any value within a particular range. It usually comes from measurement.
Examples:
 Height = 170.5 cm.
 Weight = 65.75 kg.
 Temperature = 32.6°C.
 Time = 10.25 seconds.
 Rainfall = 12.75 mm.
  Height can be measured in decimal values. It is not restricted to whole numbers.

Important points:
- Continuous data is measurable.
- Can contain decimal values.
- Exists within a range.
- Often visualized using histograms and density plots.
  1.3 Nominal data(qualitative)
Definition: Nominal data is categorical data that represents names, labels or groups without any natural order or ranking.
Examples:
- Gender: Male, Female.
- City: Hyderabad, Chennai, Bengaluru.
- Blood group: A+, B+, O+.
- Department: HR, IT, Sales.
- Animal type: Sheep, Goat, Cow.
   1.4 Ordinal data
Definition: Ordinal data is categorical data that has a meaningful order or ranking.
Examples:
- Customer satisfaction: Poor, Average, Good, Excellent.
- Education level: School, Intermediate, Graduation, Postgraduation.
- Performance: Low, Medium, High.
- T-shirt size: Small, Medium, Large.
   2. What is univariate analysis?
Definition: Univariate analysis is a statistical method used to analyze only one variable at a time.
- Uni = One.
- Variate = Variable.
Therefore, univariate means analyzing one variable.
If we analyze only the Age column, it is univariate analysis.
If we analyze only the Marks column, it is also univariate analysis.
            3. What is Matplotlib?
         Matplotlib
Python data visualization library
Used to create graphs, charts and plots from data.
Definition: Matplotlib is a Python library used to visualize numerical and categorical data through different types of graphs and charts.
Why do we use Matplotlib?
Imagine you have 17,000 palm leaf images or a dataset containing 8,000 stock market records.
If you only look at rows and columns, understanding patterns can be difficult.
Matplotlib helps you:
1. Understand data visually.
2. Identify trends.
3. Compare different values.
4. Identify unusual values.
5. Understand distributions.
import matplotlib
import matplotlib.pyplot as plt
 4. Create a dummy dataset using Pandas
Before plotting, we need data.
A dummy dataset is sample data created for learning, testing, and practicing Python concepts.
 5. Types of plots in Matplotlib
Matplotlib supports different plots depending on the type of data and your analysis objective.
Let's understand the important plots one by one.
     5.1 Line plot
Definition: A line plot is used to show changes in numerical values over time or across an ordered sequence.

Examples:
- Stock market prices.
- Monthly sales.
- Daily temperatures.
- Yearly population growth.
  ex: months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun"]
sales = [100, 150, 120, 180, 220, 250]
plt.plot(months, sales)
plt.title("Monthly Sales")
plt.xlabel("Months")
plt.ylabel("Sales")
plt.show()
and explanation:
plt.plot() → Creates a line plot.
months → X-axis values.
sales → Y-axis values.
plt.title() → Adds a graph title.
plt.xlabel() → Names the X-axis.
plt.ylabel() → Names the Y-axis.
plt.show() → Displays the graph.
 6. What is linestyle in Matplotlib?
Definition: linestyle is a parameter used to change the appearance of lines in a plot.
For example, you can create:
- Solid lines.
- Dashed lines.
- Dotted lines.
- Dash-dot lines.
   ex: months = ["Jan", "Feb", "Mar", "Apr", "May"]

sales = [100, 150, 120, 180, 220]

plt.plot(
    months,
    sales,
    linestyle="--"
)
plt.title("Monthly Sales")
plt.show()
Here, linestyle="--" creates a dashed line.
explanation:
label → Gives a name to each line.
plt.legend() → Displays the names of the lines.
linestyle → Controls the line pattern.

 7. Important Matplotlib parameters
Besides linestyle, Matplotlib provides several parameters to customize graphs.
ex: using of all perameters
months = ["Jan", "Feb", "Mar", "Apr", "May"]
sales = [100, 150, 120, 180, 220]
plt.figure(figsize=(10, 5))
plt.plot(
    months,
    sales,
    color="blue",
    linestyle="--",
    marker="o",
    linewidth=2,
    markersize=8,
    label="Monthly Sales"
)
plt.title("Monthly Sales Analysis")
plt.xlabel("Months")
plt.ylabel("Sales")
plt.legend()
plt.grid()
plt.show()
  Explanation:
- plt.figure() → Creates a figure.
- figsize=(10,5) → Sets width to 10 inches and height to 5 inches.
- color="blue" → Blue line.
- marker="o" → Circular markers.
- linewidth=2 → Line thickness.
- markersize=8 → Marker size.
- plt.grid() → Displays grid lines.
   7.1 What is plt.subplots()?
plt.subplots() is used to create multiple plots inside a single figure.
     8. Which plot should you use for which data?
Plot	Best use
Line plot	===Trends over time or sequence
Bar plot===	Comparing categories
Histogram	===Numerical distribution
Scatter plot===Relationship between two numerical variables
Pie chart===	Percentage or proportion
Box plot	===Distribution and potential outliers
Count plot===	Frequency of categorical values
