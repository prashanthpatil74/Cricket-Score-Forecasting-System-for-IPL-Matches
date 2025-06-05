# Cricket Score Prediction System for IPL Matches

Predict the final IPL match score using machine learning models based on mid-match data.

## About The Project

The **Cricket Score Prediction System for IPL Matches** is a machine learning project designed to predict the final score of an IPL cricket match based on the current game state. Using historical IPL match data, the system learns patterns and relationships between match variables to estimate the expected final runs for the batting team.

### Key Aspects of the Project

- **Data Collection and Cleaning**  
  Historical IPL match data is loaded and cleaned. Irrelevant columns are dropped, and categorical features such as team names are processed using **One-Hot Encoding** to convert them into numerical format suitable for machine learning models.

- **Feature Engineering**  
  Features used for prediction include:  
  - Current batting and bowling teams (encoded as categorical variables)  
  - Number of overs completed in the innings  
  - Runs scored so far  
  - Wickets lost  
  - Runs scored and wickets lost in the last 5 overs (to capture recent momentum)

- **Train-Test Split Based on Season**  
  To avoid data leakage and simulate real-world prediction scenarios, the dataset is split into training and test sets based on IPL seasons. Models are trained on past seasons and tested on a future season.

- **Modeling**  
  Several regression algorithms are trained and compared, including:  
  - **Linear Regression** — baseline model for linear relationships  
  - **Decision Tree Regressor** — captures non-linear patterns  
  - **Random Forest Regressor** — ensemble method to improve accuracy and reduce overfitting  
  - **AdaBoost Regressor** — boosting technique to combine weak learners into a strong predictor

- **Model Evaluation**  
  Models are evaluated using:  
  - **Mean Absolute Error (MAE)**  
  - **Mean Squared Error (MSE)**  
  - **Root Mean Squared Error (RMSE)**

- **Prediction Function**  
  A user-friendly prediction function takes live match parameters (teams, overs, runs, wickets, recent performance) and outputs the predicted final score range. This can be used for real-time score prediction applications.
