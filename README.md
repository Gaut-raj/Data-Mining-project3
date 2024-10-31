# Data-Mining-project3
Introduction: 
The problem I am aiming to solve is to predict FIFA player's wages based on various skills and finding out what skill or attribute contributes to a high wage. I found my dataset on Kaggle and it includes several attributes like player's age, overall rating, and overall ratings for various different skills like attacking and dribbling. I am trying to predict player wages. 
Link to dataset on kaggle: https://www.kaggle.com/datasets/ulrikthygepedersen/fifa-players

What is Regression and how does it work? 
Regression is a method used to find relationships between variables, especially when we want to predict one variable based on others. Think of it as trying to find a line (or curve) that best fits your data points to show a trend or pattern. In linear regression (the most basic type), we focus on finding a straight line that represents this trend.
How Linear Regression works: 

Imagine you have a scatterplot of points representing, say, player age on the x-axis and wages on the y-axis. Linear regression tries to draw a line through these points that best fits the pattern. This line is our "best guess" for predicting wages based on other factors. 

Experiment 1: Data Understanding 

Countplot to understand the variation of players with different overall ratings 
Insights with countplot: 
There are several players with different overall ratings and there are players with ratings as low as 47 and high as 93

![Screenshot 2024-10-28 122459](https://github.com/user-attachments/assets/baa73592-9c44-4206-b4e8-900e8895b95a)



Countplot to understand the variation of nationality names
Insights: There are several different nationalities that I cannot differentiate from because it is impossible to see the number of nationalities even by editing the size of the countplot 

![Screenshot 2024-10-28 123339](https://github.com/user-attachments/assets/80f4d74e-1463-416a-994e-b3b2b7b9d553)

Visualization 3: 
Correlation heatmap: 
Target variable: wage_eur
Insights: 
There is a strong correlation between overall ratings, potential ratings, and offensive skills while there is a weaker correlation between defensive and goalkeeping skills. 
Negative Correlations:
No strong negative correlations are present with wage_eur in this heatmap, meaning that none of the features inversely impact wages to a significant degree.

![output](https://github.com/user-attachments/assets/43409971-f91d-4d08-ae67-492fcad0635c)




Expirement 1, Pre-Processing: 
I have dropped the nationality_name column in my dataset because it will be hard to map every nationality since there are several and it will be hard to keep up with them although I understand it might be a significant factor in their wages. 

![code](https://github.com/user-attachments/assets/c5713158-262e-41a9-baed-32c71be6ee3e)

Experiment 1: Modeling 
In this Experiment, I created a linear regression model to predict player wages based on attributes like age, height, and skill ratings. The model was trained on a subset of the data and evaluated using Mean Squared Error (MSE) and R-squared (R²). MSE measures the average squared difference between actual and predicted wages, with lower values indicating better predictions, while R² indicates the proportion of wage variance explained by the model. The resulting metrics provide insights into how well the model captures wage patterns based on player attributes. 

Expirement 1: Evaluation

Scores Achieved: 

Mean Squared Error (MSE): 246773937.67981625

R-squared (R²): 0.37462174506960466

These results indicate that the model explains about 37% of the variance in player wages and has a relatively high MSE. This suggests potential improvements through further feature engineering and possibly experimenting with nonlinear models or additional features to better capture the complex relationships in the data.




![modeling](https://github.com/user-attachments/assets/6ce2ac9a-4cd1-4419-b143-abf14b928ee2)



Expirement 2: 

In Expirement 2, I aimed to improve upon initial model performance by exploring changes to the model. 

Model Selection: For the first expirement, I used a simple linear regression model which yielded low scores. For the second expirement, I decided to try a SDGregressor. I decided to use this dataset because it is optimized for larger datasets and allows for feature engineering which might handle any potential overfitting. 

Model evaluation: 
Switching to SGDregressor significantly improved the model's performance. The Mean Absolute Error decreased to approximately 8406.33, which translates to about a 2-3% average error relative to target wage values. This was notable compared to the linear regression model since the first model had a much higher error rate. 

![Screenshot 2024-10-31 091123](https://github.com/user-attachments/assets/3aec154e-6bbe-4202-ad40-f0ff51377ab5)

Expirement 3: 

In Expirement 3, I aimed to improve upon the first and second model by making a change to the model

Model selection: I used a simple linear regression model for the first expirement and a SGDScaler model for the second expirement. I applied Ridge regression in this expirement because ridge regression includes a regularization term, which helps manage high-dimensional features and correlated features effectively.

Model Evaluation: I achieved a mean absolute error score of 8274.70 which is a better score the scores I recieved from the first and second model. This reduction in MAE suggests that Ridge regression, may be more effective at capturing patterns in this dataset without overfitting, leading to more accurate wage predictions. 

![Screenshot 2024-10-31 092104](https://github.com/user-attachments/assets/28eae07b-946a-40f6-9556-f00a707685ba)


Impact: 
My project will not have any negative and positive impacts affecting real life athletes or soccer players since this project uses a dataset from a video game and the wages are completely fictional although the players from this video game exist in real life. 

Positive Impacts: 
Enhanced gameplay experiences: Contributes to a more realistic and engaging experience for players by accurately predicting player wages. This might improve the performance of team management gameplay modes within the FIFA video game. 
Fair representation of player attributes: Allows player's wages to closely align with their attributes like overall, potential, and offensive skills 

Negative Impacts: 
Ethical Considerations in Player Representation: If the model overemphasizes or underestimates certain attributes, it could create skewed perceptions of player value based on characteristics that may not fully represent real-world performance.
Reinforcement of Biases: Machine learning models can unintentionally reinforce biases present in training data. If certain player attributes are historically undervalued in the dataset, the model might perpetuate these biases in wage predictions, impacting the representation of various player types or demographics.
It is also important to note that young players of this video game might mistake them to be accurate wages and that this dataset is sligthly outdated since newer versions of the game have been released. 


References: 
Regression_example.ipynb(Demo notebook from canvas) 

https://pieriantraining.com/7-machine-learning-regression-algorithms-python/


Code: 
On Code section of this repository


