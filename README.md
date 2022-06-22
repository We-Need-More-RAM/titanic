# titanic

## Purpose

Predict the outcome of Titanic passengers based on their personal information.

## Dataset

The classic titanic datase found [here](https://www.kaggle.com/competitions/titanic).

## Data processing

Removed the Cabin column because the majority of values were null. Replaced the null values in the Age and Embarked columns with the median values for the respective columns. Dropped the PassengerId, Name, and Ticket columns because they were deemed irrelevant for the problem at hand. Encoded the Sex and Embarked columns into numerical values. Split the dataframe into features and the target variable for training.

## Model training

Used the sklearn [decision tree](https://scikit-learn.org/stable/modules/tree.html) as the algorithm for this project. Created a basic loop to train decision trees with depths from 3 to 7 and record the accuracy from each trial.

## Results

The deepest tree (max_depth=7) produced the best accuracy of roughly 88%.

## Discussion

There is a high risk of overfitting on the training data, given the depth of the decision tree and the limited training data. Future attempts could perform more exploratory data analysis to determine the best predictors of survival, optimize the use of the decision tree algorithm, or approach the problem with an entirely new algorithm.
