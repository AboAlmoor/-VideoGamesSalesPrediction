<p align="center"># Video Game Sales Prediction.</p>
This repository contains a final project solution for the machine learning course.


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
|---------------------|-----|------|--------|
| Linear Regression	| 0.0040 | 0.0086 | 0.7219 |
| Polynomial Regression	| - | - | 0.8231 |
| Random Forest Regressor	 | 0.0023 | 0.0059 | 0.8663 |
| XGBoost Regressor	 | 0.0022 | 0.0054 | 0.8884   |
|Gradient Boosting| 0.0020 | 0.0051 | 0.9037 |

- Gradient Boosting outperformed all other models, achieving the highest R² score and lowest errors.


## Key Findings 🔍
1. Top Features: Critic Score, User Score, and regional sales (e.g., Other Sales) significantly influenced global sales.
2. Model Performance: Ensemble methods (Gradient Boosting, XGBoost) consistently outperformed simpler models.
3. Non-Linear Relationships: Polynomial Regression improved over Linear Regression but was still less effective than ensemble methods.


## Challenges & Limitations ⚠️
1. Data Quality: Handling missing values and encoding categorical variables were critical steps.
2. Computational Complexity: Models like XGBoost and Gradient Boosting required significant resources.
3. Hyperparameter Tuning: Selecting optimal parameters was essential for model performance.


## Conclusion & Future Work 🚀
- Conclusion: Gradient Boosting emerged as the best model for predicting video game sales, demonstrating the power of ensemble methods.
- Future Work:
  - Incorporate additional features like marketing spend and player demographics.
  - Explore explainable AI techniques to interpret model decisions.

    
  
  
