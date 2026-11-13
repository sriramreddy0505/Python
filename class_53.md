          1. What is Feature Engineering?
Feature Engineering is the process of creating, transforming, selecting, or modifying input variables (features) to improve the performance of a Machine Learning model.
We take existing data and prepare it in a better format so that a Machine Learning model can understand it and make better predictions.
     Why do we use Feature Engineering?
1. Improve model accuracy.
2. Extract useful information.
3. Create meaningful features.
4. Reduce unnecessary complexity.
5. Help models identify patterns.
         Types of Feature Engineering
Technique	Meaning
Feature Creation	            Creating new columns
Feature Transformation       	Changing existing values
Feature Encoding	            Converting categories into numbers
Feature Scaling	              Bringing values to comparable scales
Feature Selection	            Selecting important columns
Feature Extraction	           Extracting useful information from existing data

 2. What are Missing Values?
Missing values are values that are not available in a dataset.
Here, NaN means Not a Number. It is commonly used by Pandas to represent missing numerical values.

Missing data can occur because:
- A person did not provide information.
- Data was not collected.
- A sensor failed.
- Information was deleted.
- A data entry mistake occurred.
-   3. Missing Completely At Random (MCAR)
MCAR means Missing Completely At Random.
The missing values have no relationship with any other variable or with the missing value itself.
Example:
Suppose you are collecting the ages of 100 passengers.
Due to a temporary technical problem, 10 age records are randomly lost.
The missing ages are not related to age, gender, ticket price, or any other factor.
If the missing ages occurred due to a random computer failure, this could be MCAR.

 How to handle MCAR?
- Drop missing rows if only a small percentage is missing and dropping them is appropriate.
- Fill missing values using mean, median or another suitable method.
- Investigate the amount of missing data before deciding.
   4. Missing At Random (MAR)
MAR means Missing At Random.
Missing values depend on another observed variable, but not on the missing value itself after accounting for that variable.
Example:
Suppose a survey collects salary and gender.
Some people with a particular gender are less likely to report their salary.
Here, missing salary information is related to gender, which is available in the dataset.
This is an example of MAR if salary missingness does not additionally depend on the actual salary after accounting for gender.
How to handle MAR?
- Group-based median imputation.
- Group-based mean imputation.
- Multiple imputation.
- Predictive imputation.
   ex:df["Age"] = df.groupby("Sex")["Age"].transform(
    lambda x: x.fillna(x.median())

)           
 5. Missing Not At Random (MNAR)
MNAR means Missing Not At Random.
The probability of a value being missing depends on the value that is missing itself, even after accounting for observed variables.
Example:
Suppose people with very high salaries are less willing to disclose their salaries.
The missingness depends on the actual salary.
This is MNAR.
How to handle MNAR?
- Investigate why the values are missing.
- Collect additional information if possible.
- Use domain knowledge.
- Consider specialized statistical models.
- Perform sensitivity analysis.
    6.How to fill missing values with median()
Before understanding median imputation, let's understand three statistical measures.
- Mean = Average value.
- Median = Middle value after sorting.
- Mode = Most frequently occurring value.
What is Median Imputation?
Median imputation means replacing missing numerical values with the median of the available values.
  7. What is Embarked?
Embarked is a categorical column in the Titanic dataset.
It represents the port where a passenger boarded the Titanic.
It contains three categories:
Value	Meaning
C	   Cherbourg
Q	   Queenstown
S	   Southampton
  Suppose the Embarked column contains missing values.
How can we fill them?
One common approach is using mode.
df["Embarked"].mode()
This returns the most frequently occurring category.
To get the first mode value:
df["Embarked"].mode()[0]
To fill missing values:
df["Embarked"] = df["Embarked"].fillna(
 df["Embarked"].mode()[0])
Why mode?
Because Embarked is categorical data, not numerical data.
We cannot meaningfully calculate the average of C, Q and S.
Therefore, mode is often suitable.
  8. What is notna()?
notna() is used to identify values that are NOT missing.
ex:df["Age"].notna()
  0     True
1    False
2     True
3     True
    Difference between isna() and notna()
Function  	Meaning
isna()    	Identifies missing values
notna()	    Identifies non-missing values
dropna()	  Removes missing values
fillna()	  Fills missing values
  9. What is Upsampling?
Upsampling is a technique used to increase the number of samples in a dataset.
In Machine Learning, it is particularly useful when dealing with imbalanced datasets.
Let's understand with an example.
Suppose you are building an animal disease prediction model.
Your dataset contains:
Class	Images
Healthy sheep	900
Disease A	80
Disease B	20
Here, Healthy sheep have many more examples than Disease B.
This is called an imbalanced dataset.
A model may learn to predict the majority class more often.
Upsampling increases the representation of minority classes.

10. What is Downsampling?
Downsampling is the process of reducing the number of samples from the majority class.
We reduce the majority class to make the classes more balanced.

11. What is a Box Plot?
A Box Plot is a visualization technique used to understand the distribution of numerical data and identify outliers.
12. What is Data Encoding?
Data Encoding is the process of converting categorical data into numerical values so that Machine Learning algorithms can process it.
 13. What is Target-Guided Ordinal Encoding?
This is an important feature engineering technique.
Target-Guided Ordinal Encoding means encoding categorical variables based on their relationship with the target variable.
In simple words:
We calculate the target variable's average for each category and assign numerical values according to that average.
Let's understand with a Titanic example.
Suppose your target variable is:
Survived
- 0 = Did not survive.
- 1 = Survived.
Your categorical column is Embarked.
