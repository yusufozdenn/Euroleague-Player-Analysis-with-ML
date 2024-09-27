# Euroleague-Player-Analysis-with-Linear-Regression
This project analyzes Euroleague basketball player performance using machine learning techniques. The goal is to predict game scores based on key player statistics and to explore the most significant factors influencing player performance.

## Steps:
**1- EDA (Exploratary Data Analysis)**
<br>
**2- Modeling**
<br>
**3- Prediction and Model Evaluation**
<br>
**4- Conclusion**

# Here's some examples from each steps:

### 1.
first 10 observations of the dataset:

![Screenshot 2024-09-28 at 02 08 34](https://github.com/user-attachments/assets/d2c6703f-1b72-4ef2-8892-8861588265e4) 

MP :minutes played in game,
FG% :Percantage of field goal,
AST :Asist,
GmSc : Game Score's +/- 

all data's are shown indiviually for specific game,which are shown in the index from website : https://www.basketball-reference.com

Correlation heatmap provides graphical representation of the relationships between variables in a dataset:

![Screenshot 2024-09-28 at 01 58 59](https://github.com/user-attachments/assets/77038b2e-d8b7-4538-bf11-e92afa2753fb)

**according to many other visualization techniques i used in this project; I was able to choose which independent variables i should choose to model my predictions.**

### 2.
For modeling,Both statsmodel and scikit-learn used for good measurements.

*screenshot of model summary of data*

![Screenshot 2024-09-28 at 02 24 44](https://github.com/user-attachments/assets/2eaeb484-ed68-40ac-8a52-6b7245c91210) 

*quantile plot of residuals*

![Screenshot 2024-09-28 at 01 58 23](https://github.com/user-attachments/assets/02500bf1-07fc-4e6c-8f52-e5277eecb991)

**After evaluating metrics such as R-squared and F-statistics, along with analyzing residual plots, I proceeded to the model prediction and evaluation step.**

### 3.

Measuring and visualizing the model performance:

![Screenshot 2024-09-28 at 02 32 14](https://github.com/user-attachments/assets/f6a4db03-b098-42be-8437-2d47b6a98bf2)



after that,I wanted to do a prediction with my new data whereas FG% was 0.5 and PTS was 14.

![Screenshot 2024-09-28 at 02 45 28](https://github.com/user-attachments/assets/81361f55-b6a8-4809-8302-0630a506b546)

so the model predicted the Game score will be around 11.2

I also checked the dataset and find similar values whereas the FG% was 0.5 and PTS was 14 and here's the GmSc results of them:

![Screenshot 2024-09-28 at 02 41 01](https://github.com/user-attachments/assets/855048a2-67e1-4c29-9e0a-9948650720b7)

for further prediction testing i choose 3rd data which is far from my predictions against 35th data.
Even though I choose the further data,model's predictions seemed on point,at least on the MSE and RMSE values:

![Screenshot 2024-09-28 at 02 49 31](https://github.com/user-attachments/assets/1faea1a0-f46d-425b-ad3b-26dcf4f4ae2b)

And lastly evaluation of the dataset included the model tuning :

Sample graph:

![Screenshot 2024-09-28 at 01 57 52](https://github.com/user-attachments/assets/caa19e3e-889f-4564-aa39-d9b3f245b7b2)

### 4.
I observed strong correlations between player points,percantage of the field goal and game score suggesting that these metrics are important points for tuning.

The regression model performed with an RMSE of 2.6 and also average R-squared value of 0.50, which indicates that approximately 50% of the variance in the player’s performance could be explained by the features used in the model indicating relatively good accuracy. However, there is room for improvement, especially due to the unpredictable nature of sports data. Future work could focus on incorporating additional features such as player fatigue, game location, and team dynamics to enhance the model's predictive power.


Lastly,I wanted to thank https://www.basketball-reference.com again for the dataset.
