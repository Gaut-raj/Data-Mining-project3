# Data-Mining-project3
Introduction: 
The problem I am aiming to solve is to predict FIFA player's wages based on various skills and finding out what skill or attribute contributes to a high wage. I found my dataset on Kaggle and it includes several attributes like player's age, overall rating, and overall ratings for various different skills like attacking and dribbling. I am trying to predict player wages. 
Link to dataset on kaggle: https://www.kaggle.com/datasets/ulrikthygepedersen/fifa-players

What is Regression and how does it work? 
Regression is a method used to find relationships between variables, especially when we want to predict one variable based on others. Think of it as trying to find a line (or curve) that best fits your data points to show a trend or pattern. In linear regression (the most basic type), we focus on finding a straight line that represents this trend.
How Linear Regression works: 

Imagine you have a scatterplot of points representing, say, player age on the x-axis and wages on the y-axis. Linear regression tries to draw a line through these points that best fits the pattern. This line is our "best guess" for predicting wages based on other factors. 



Pre-Processing: 
I have dropped the nationality_name column in my dataset because it will be hard to map every nationality since there are several and it will be hard to keep up with them although I understand it might be a significant factor in their wages. 

![code](https://github.com/user-attachments/assets/c5713158-262e-41a9-baed-32c71be6ee3e)

Experiment: Modeling 
In this Experiment, I created a linear regression model to predict player wages based on attributes like age, height, and skill ratings. The model was trained on a subset of the data and evaluated using Mean Squared Error (MSE) and R-squared (R²). MSE measures the average squared difference between actual and predicted wages, with lower values indicating better predictions, while R² indicates the proportion of wage variance explained by the model. The resulting metrics provide insights into how well the model captures wage patterns based on player attributes. 
Scores Achieved: 

Mean Squared Error (MSE): 246773937.67981625

R-squared (R²): 0.37462174506960466

These results indicate that the model explains about 37% of the variance in player wages and has a relatively high MSE. This suggests potential improvements through further feature engineering and possibly experimenting with nonlinear models or additional features to better capture the complex relationships in the data.




![modeling](https://github.com/user-attachments/assets/6ce2ac9a-4cd1-4419-b143-abf14b928ee2)






