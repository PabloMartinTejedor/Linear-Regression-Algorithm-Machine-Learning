# 📌 Machine Learning Project - Smartphone Prices Prediction

This project focuses on developing the `Linear Regression Algorithm` from scratch to predict smartphone prices based on their characteristics.
Firstly, the dataset goes through preprocessing, including feature selection, handling `NaN` values and encoding categorical variables.
Secondly, the model is trained and evaluated using regression metrics.
Finally, the results are compared with the implementation provided by `Scikit-Learn`, evaluating accuracy and efficiency.

## 📂 Project Structure

- `Smartphone_Prices_Prediction.ipynb`: Contains all code organized, explanations and analysis.
- `Requirements.txt`: Required Python libraries.
- `Smartphones.csv`: Dataset with smartphone feautures.

## 📖 Dataset

The dataset used in this project contains information about multiple smartphones an their respective features, which are used to predict their final prices. You can access the dataset via the following link:

🔗 [Smartphones Dataset](https://raw.githubusercontent.com/PabloMartinTejedor/Linear-Regression-Algorithm-Machine-Learning/refs/heads/main/Smartphones.csv)

## 📊 Data Preprocessing

1. **Removing Irrelevant Columns / Variables**: Brands, models, storage capacities and colors with few records are removed to improve the prediction of the relationship between the different variables in the dataset with the `Final Price` (target variable).

2. **Handling "NaN" Values**:

   - **RAM** `NaN` values are replaced with the **median** (statistical measure less sensitive to outliers).
   - **Storage** `NaN` values are removed (small percentage of such data removed doesn't affect the relationship between the different variables in the dataset with the target variable.

3. **Encoding Categorical Variables**:  `Brand`, `Model`, `Color` and `Free` are encoded as numerical variables to analyze their relationship with the target variable.

## 📈 Model Training & Evaluation

1. **Dataset Split**: 80% for training, 20% for testing.

2. **Linear Regression Model Implementation Using 2 Methods**:

   - **Scikit-Learn**: Uses the efficient implementation of **Ordinary Least Squares** internally to compute the model´s coefficients (betas).
   - **Ordinary Least Squares (OLS)**: Manually implemented to calculate the model´s coefficients (betas) using the equation: 
      ```math
      B = (X^T  X)^{-1} X^T Y
      ```

3. **Linear Regression Model Evaluation Using 2 Regression Metrics**:

   - **Coefficient of Determination (R²)**: Measures the percentage of variation in the target variable that can be explained by the model. A higher `R²` indicates a better fit.
   - **Root Mean Square Error (RMSE)**: Provides the average error between predicted and actual values. A lower `RMSE` indicates more accurate predictions.

## 🧮 Results and Analysis 

- Both methods achieved the same evaluation results (R² = 76.94% & RMSE = 209.2), as `Scikit Learn` internally employs `OLS`, ensuring identical results and confirming the correct implementation of the model.
- `RAM` (0.442) and `Storage` (0.699) are the most impactful factors.
- Specific models and brands (`Brand_Apple`, `Model_Iphone_13` and `Model_Iphone_14`) also show high correlations with the target variable.
-  `Color_Purple` (0.158) has a lower influence. 
