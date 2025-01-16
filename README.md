# Wine Price Prediction Project

## Project Description:
In this project, I aim to predict the price 💰 of Bordeaux wines 🍷 based on their various features, such as rating, volume, and other characteristics.  
I utilized the 21st Century Bordeaux Wine Dataset from Kaggle, which contains valuable information about 14,349 wines. The goal was to build a machine learning model that can accurately predict wine prices based on specific factors.

I chose to use ElasticNet, a regression model that combines both Ridge and Lasso regression, to achieve this. Additionally, I performed grid search to optimize the model’s hyperparameters, ensuring the best possible performance.

Source of the dataset: [21st Century Bordeaux Wine Dataset on Kaggle](https://www.kaggle.com/datasets/mexwell/21st-century-bordeaux-wine-dataset/data)

![south-park-wine-tasting-meme](https://github.com/user-attachments/assets/297f3eea-6dc3-4e99-9413-a1bed7c1cdf3)
---

## Project Workflow:
### 1. Data Import and Cleaning:
- Loaded the dataset and created a copy to preserve the original data.
- Cleaned the ‘Price’ column by removing invalid values (e.g., "$NA") and unnecessary characters like ‘ml’ and ‘$’.
- Created the ‘Volume’ column by extracting volume information from the ‘Price’ column when applicable (e.g., "375ml").
- Added new features, such as ‘Price_per_ml’ and ‘Price_per_750ml’, to gain better insights into wine pricing.

### 2. Model Development:
- Chose the ElasticNet regression model due to its ability to handle multicollinearity and perform feature selection.
- Optimized hyperparameters using GridSearchCV to find the best combination of alpha and l1_ratio.

### 3. Evaluation Metrics:
- **\( R^2 \):** 0.995 – The model explains 99.5% of the variance in wine prices.
- **Mean Absolute Error (MAE):** 2.282 – On average, the predicted prices deviate from the actual prices by $2.28.
- **Root Mean Squared Error (RMSE):** 5.741 – Captures the typical magnitude of errors, considering both smaller and larger deviations.

### 4. Model Insights:
- **Performance by Price Range:** The model performs exceptionally well for wines in the lower to mid-price ranges. However, errors increase for premium wines, as shown by the bar plot of MAE across price ranges.
- **Error Distribution:** The prediction errors are symmetrically distributed around zero, confirming the model’s unbiased predictions.

---

## Visual Analysis:
Key plots from the analysis include:
1. **Actual vs Predicted Prices:** Predicted values closely align with actual values, forming a near-perfect diagonal line (\( R^2 = 0.995 \)).
2. **Error Distribution:** Errors are tightly concentrated around zero, demonstrating high accuracy.
3. **Prediction Errors vs Predicted Prices:** Highlights how the errors vary across the predicted price range.
4. **Model Performance by Price Range:** The model performs consistently well across different price ranges, though errors slightly increase for premium wines.
