## Project Overview 📌
This project aims to predict global video game sales using machine learning techniques. By analyzing features such as genre, platform, publisher, critic/user scores, and regional sales, we developed models to forecast sales performance accurately. The best-performing model achieved an R² score of 0.9037, demonstrating strong predictive power.


## Dataset 📂
- Source: [Kaggle - Video Game Sales with Ratings](https://www.kaggle.com/code/arthurtok/the-console-wars-ps-vs-xbox-vs-wii)
- Description: The dataset contains 16,598 rows and 14 features, including:
  - Name: Title of the video game.
  - Platform: Gaming console or platform (e.g., Wii, PS3).
  - Year of Release: Release year.
  - Genre: Game category (e.g., Sports, Racing).
  - Publisher: Publishing company.
  - Regional Sales: NA, EU, JP, and Other Sales.
  - Global Sales: Total worldwide sales.
  - Critic/User Scores: Average scores from critics and users.


## Methodology 🛠️
- Data Preprocessing
  1. Handling Missing Values:
     - Removed User Count due to excessive missing data.
     - Replaced "tbd" in User Score with the mean value.
     - Dropped rows with missing values, reducing the dataset to ~8,000 rows.
  2. Encoding:
     - Used OrdinalEncoder for categorical features (e.g., Platform, Genre).
  3. Scaling:
     - Applied MinMaxScaler and StandardScaler to numerical features.

- Models Evaluated:
  - Linear Regression: Baseline model.
  - Polynomial Regression: Captured non-linear relationships (degree=3).
  - Random Forest Regressor: Ensemble method for feature interactions.
  - XGBoost Regressor: Optimized for speed and accuracy.
  - Gradient Boosting Regressor: Sequentially minimized residual errors.

- Hyperparameter Tuning:
  - Used GridSearchCV to optimize hyperparameters for ensemble models.

- Evaluation Metrics:
  - Mean Absolute Error (MAE): Average magnitude of errors.
  - Root Mean Squared Error (RMSE): Penalizes larger errors.
  - R² Score: Proportion of variance explained by the model.


## Results 📈
|   Model   |   MAE   |  RMSE  |  R² Score  |
|---------------------|-----|------|----------|
| Linear Regression	| Value 2    | Value 3       |
| Value 4    | Value 5    | Value 6       |


  
