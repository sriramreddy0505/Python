   1.What is Training Data?
Training data is the data that we provide to a Machine Learning algorithm so that it can learn patterns and relationships.
Why do we use training data?
1. To teach the algorithm.
2. To identify patterns.
3. To understand relationships between features and labels.
4. To learn mathematical parameters.
5. To build a Machine Learning model.
ex:If you want to teach a child to identify different fruits, you show pictures of apples, bananas and oranges.
Similarly, we provide historical data to a Machine Learning algorithm so that it can learn.
  2.What is Testing Data?
Definition:
Testing data is the data used to evaluate how well a trained Machine Learning model performs on data it has not seen during training.
In simple words:
Testing data = Data used to check the model's performance.
Let's understand with our house price dataset.
If the predicted prices are close to actual prices, the model is performing well.
  Why do we use testing data?
- To evaluate model performance.
- To check whether the model learned properly.
- To identify overfitting.
- To understand whether the model generalizes to new data.
Important: We should not train the model using the testing data. Otherwise, our evaluation may not represent its ability to handle genuinely unseen data.
       3. What is Supervised Learning?
Supervised Learning is a type of Machine Learning in which an algorithm learns from labelled data.
Let's understand the important word: Label.
 here:
- Study hours = Input (Feature)
- Exam marks = Output (Label)
We already know the correct answers (exam marks).
Therefore, this is called labelled data.
The algorithm learns the relationship between study hours and exam marks.
Now, if a student studies for 6 hours, the model can predict the expected marks.
in supervised learning:
- Input data is provided.
- Correct output labels are provided.
- The algorithm learns from both.
- The trained model predicts outputs for new inputs.
  type of supervised learmimg;
  1. Regression
Regression predicts continuous numerical values.
2. Classification
Classification predicts categories or classes.
 4.What is a Supervised Learning Algorithm?
A supervised learning algorithm is a mathematical procedure that learns relationships between input features and known output labels from training data.
5.What is a Model in Machine Learning?
A Machine Learning model is the learned mathematical representation of patterns and relationships obtained from training data.
  Here, the model has learned a mathematical relationship between house size and price, using the units in this example.
 6.Why Do We Use a Machine Learning Model?
   We use a model because we want computers to make predictions based on patterns learned from historical data.
   For example, in agriculture, you can train a model using:
- Rainfall
- Temperature
- Soil type
- Fertilizer quantity
- Previous crop production
The model can predict expected crop production for new conditions.
Main purpose: Use learned patterns to make predictions on new data.
 7. What is Model Training?
Definition:
Model training is the process of providing training data to a Machine Learning algorithm so that it can learn the relationship between input features and output labels.
Here, the model has learned a mathematical relationship between house size and price, using the units in this example.
 Think about it like this:
- Algorithm = Teacher's teaching method.
- Training data = Study material.
- Model = Knowledge learned by the student.
- Prediction = Student answering a new question.
  8. What is Linear Regression?
  Definition:
Linear Regression is a supervised Machine Learning algorithm used to predict a continuous numerical value by learning a linear relationship between independent variables (input features) and a dependent variable (output).
In simple words:
  What do you observe?
When study hours increase, marks also increase.
There is a linear relationship between study hours and marks in this illustrative dataset.
The Linear Regression algorithm learns that relationship.
It finds a straight line that best represents the relationship between X and Y.
y=mx+c
9.What is Slope?
Definition:
Slope represents how much the predicted output changes when the input feature increases by one unit.
Meaning: For every additional study hour, predicted marks increase by 10 in this example.
 10.What is Simple Linear Regression?
Definition:
Simple Linear Regression is a type of Linear Regression that uses only one independent variable (one input feature) to predict one dependent variable (output).
For example:
You want to predict student marks based on study hours.
- Input X = Study hours.
- Output Y = Exam marks.
There is only one input feature.
Therefore, it is Simple Linear Regression.
  
