# Bengaluru House Price Prediction 🏡

## 📌 Overview

This project uses Machine Learning to predict residential property prices in Bengaluru, India, based on features such as location, total square footage, number of bathrooms, and number of bedrooms (BHK).

The project involves data cleaning, exploratory data analysis, feature engineering, outlier removal, categorical encoding, and model training using Linear Regression.

## 🎯 Objectives

- Analyze real estate data to identify property price patterns.
- Clean and preprocess the housing dataset.
- Perform feature engineering to improve data quality.
- Detect and remove statistical outliers.
- Encode categorical features using One-Hot Encoding.
- Build a Linear Regression model to predict house prices.
- Evaluate model performance using train-test splitting and cross-validation.

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Scikit-learn** – Machine learning and model evaluation
- **Jupyter Notebook** – Development environment

## 📂 Project Structure

```text
Bengaluru-House-Price-Prediction/
│
├── Real_estate.ipynb
├── Bengaluru_House_Data.csv
└── README.md
```

## 📊 Dataset

The project uses the Bengaluru housing dataset, `Bengaluru_House_Data.csv`, containing information about residential properties.

**Key features include:**

- `location` – Property location
- `total_sqft` – Total area in square feet
- `size` – Property configuration
- `bhk` – Number of bedrooms
- `bath` – Number of bathrooms
- `price` – Property price in lakhs
- `price_per_sqft` – Engineered price per square foot

## ⚙️ Project Workflow

### 1. Data Cleaning and Preprocessing
- Handled missing values and removed unnecessary columns.
- Extracted BHK values from the property size column.
- Converted square-footage ranges into numerical values.
- Prepared the dataset for analysis and model training.

### 2. Exploratory Data Analysis (EDA)
- Analyzed housing data distributions.
- Visualized price-per-square-foot distributions.
- Compared property prices across different BHK configurations.
- Examined bathroom counts and potential anomalies.

### 3. Feature Engineering
- Created a price-per-square-foot feature.
- Grouped less frequent locations into an `other` category.
- Applied location-based filtering to improve data quality.
- Prepared numerical and categorical features for modeling.

### 4. Outlier Detection and Removal
- Applied statistical filtering to identify unusual property prices.
- Compared properties with different bedroom configurations.
- Removed selected square-footage, price, and bathroom-related outliers.

### 5. Categorical Encoding
- Applied One-Hot Encoding to the location feature.
- Combined encoded location variables with numerical features.
- Separated independent variables and the target variable.

### 6. Model Building
- Trained a Linear Regression model using Scikit-learn.
- Split the dataset into training and testing sets using an 80:20 ratio.
- Used a fixed random state of 10 for reproducibility.

### 7. Model Evaluation
- Evaluated the model using the test-set score.
- Applied five-split ShuffleSplit cross-validation to assess performance across different data splits.

### 8. Price Prediction
Developed a custom `predict_price()` function to estimate property prices using location, square footage, number of bathrooms, and BHK.

Example:

```python
predict_price('1st Phase JP Nagar', 1000, 2, 2)

predict_price('Indira Nagar', 1000, 3, 2)
```

## 🚀 Installation and Usage

### Prerequisites

Install Python and the required libraries.

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Bengaluru-House-Price-Prediction.git
```

### Step 2: Navigate to the Project Directory

```bash
cd Bengaluru-House-Price-Prediction
```

### Step 3: Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### Step 4: Add the Dataset

Place `Bengaluru_House_Data.csv` in the project directory. Update the dataset path in the notebook if necessary.

### Step 5: Run the Notebook

```bash
jupyter notebook
```

Open `Real_estate.ipynb` and execute the cells in sequence.

## 📈 Model Performance

The model is evaluated using a held-out test dataset and five-split cross-validation.

Performance metrics can be added after running the notebook, including:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

## 🔮 Future Improvements

- Compare Linear Regression with Ridge Regression, Lasso Regression, and tree-based models.
- Add additional regression evaluation metrics.
- Develop an interactive house price prediction application using Streamlit.
- Improve feature engineering and outlier-handling techniques.
- Save the trained model for future predictions.

## 📚 Key Learnings

- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Statistical outlier detection
- Categorical feature encoding
- Supervised machine learning
- Linear Regression
- Train-test splitting and cross-validation
- Building prediction functions using Scikit-learn

