# 🏗️ Bulldozer Price Prediction

This machine learning project predicts the sale price of bulldozers using historical auction data. The data comes from the Blue Book for Bulldozers and includes equipment attributes and sale information. The project utilizes feature engineering, missing value handling, categorical encoding, and model tuning with Random Forest and RandomizedSearchCV.

## 📂 Dataset

- **Raw Dataset:** `TrainAndValid.csv`  
  Contains historical bulldozer auction data used for training and validation.

- **Processed Data:**
  - `train.csv` – Cleaned and preprocessed training dataset.
  - `valid.csv` – Validation dataset created by splitting the training data.

- **Test Dataset:** `Test.csv`  
  Contains unseen data for which predictions are made.

- **Source:** [Kaggle - Blue Book for Bulldozers](https://www.kaggle.com/c/bluebook-for-bulldozers)

## 🛠️ Project Workflow

### 📌 1. Data Loading and Exploration
- Read the data with `pandas`.
- Initial visualizations and basic info with `.info()` and `.head()`.

### 📅 2. Date Feature Engineering
- Extract `saleYear`, `saleMonth`, `saleDay`, `saleDayofweek`, and `saleDayofyear` from `saledate`.
- Drop the original `saledate` column.

### 🧹 3. Handling Missing Values
- For numeric columns: Fill with median and add an `is_missing` indicator.
- For categorical columns: Convert to ordered categories.

### 🔢 4. Encoding Categorical Features
- Convert object type columns into numeric using `astype("category").cat.codes`.

## 5️⃣ 🔍 Model Building

- **Algorithm Used:** `RandomForestRegressor`  
  A robust ensemble learning method based on decision trees, effective for regression tasks.

- **Data Splitting Strategy:**  
  Training and validation data are separated to evaluate model performance on unseen data.

- **Hyperparameter Tuning:**  
  Used `RandomizedSearchCV` for tuning parameters like `n_estimators`, `max_depth`, `min_samples_split`, etc.

- **Evaluation Metrics:**
  - `R² Score` – Measures the proportion of variance explained by the model.
  - `MAE` (Mean Absolute Error) – Measures the average magnitude of errors.
  - `RMSLE` (Root Mean Squared Log Error) – Penalizes underestimates more than overestimates.
  - `MSLE` (Mean Squared Log Error) – A logarithmic variant of MSE that works better for targets with large ranges.
 ---

  ## 📬 Contact

For any queries or suggestions, feel free to reach out:

- 📧 Email: [abineshbalasubramaniyam@example.com](mailto:abineshbalasubramaniyam@example.com)
- 💼 LinkedIn: [linkedin.com/in/abinesh-b-1b14a1290/](https://www.linkedin.com/in/abinesh-b-1b14a1290/)
    
