# Data-Mining-project3
Introduction: 
The problem I am aiming to solve is to predict FIFA player's ages based on various skills and finding out what skill or attribute contributes to a high wage. I found my dataset on Kaggle and it includes several attributes like player's age, overall rating, and overall ratings for various different skills like attacking and dribbling. I am trying to predict player wages. 
Pre-Processing: 
I have dropped the nationality_name column in my dataset because it will be hard to map every nationality since there are several and it will be hard to keep up with them although I understand it might be a significant factor in their wages. 

![code](https://github.com/user-attachments/assets/c5713158-262e-41a9-baed-32c71be6ee3e)

Experiment: Modeling 
In this Experiment, I created a linear regression model to predict player wages based on attributes like age, height, and skill ratings. The model was trained on a subset of the data and evaluated using Mean Squared Error (MSE) and R-squared (R²). MSE measures the average squared difference between actual and predicted wages, with lower values indicating better predictions, while R² indicates the proportion of wage variance explained by the model. The resulting metrics provide insights into how well the model captures wage patterns based on player attributes.

![modeling](https://github.com/user-attachments/assets/6ce2ac9a-4cd1-4419-b143-abf14b928ee2)






