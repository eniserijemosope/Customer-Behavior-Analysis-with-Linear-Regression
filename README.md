# Customer Spending Prediction with Linear Regression

## 📌 Project Overview

This notebook analyzes customer data from a fictional e-commerce company to predict annual spending patterns. The project uses exploratory data analysis (EDA) and a linear regression model to:

- Identify which customer features correlate most strongly with spending
- Help the company decide whether to invest more in website or mobile app improvements

## 🛠️ Technologies Used

- **Python** (Primary programming language)
- **Pandas** (Data manipulation and analysis)
- **NumPy** (Numerical computing)
- **Matplotlib/Seaborn** (Data visualization)
- **Scikit-learn** (Machine learning implementation)
  - `train_test_split` (Data splitting)
  - `LinearRegression` (Model implementation)
  - Evaluation metrics (`mean_absolute_error`, `mean_squared_error`, `r2_score`)

## 📂 Dataset

The dataset (`Ecommerce Customers.csv`) contains information about 500 customers with the following features:

- `Email`
- `Address`
- `Avatar`
- `Avg. Session Length`
- `Time on App`
- `Time on Website`
- `Length of Membership`
- `Yearly Amount Spent` (Target variable)

## 🔍 Key Steps

1. **Data Loading & Initial Exploration**
   - Import and examine the dataset structure
   - Check for missing values and data types

2. **Exploratory Data Analysis (EDA)**
   - Visualize relationships between features
   - Identify correlations with spending

3. **Data Preparation**
   - Select relevant features
   - Split data into training and test sets

4. **Model Building**
   - Implement Linear Regression
   - Train the model on customer data

5. **Evaluation**
   - Assess model performance using metrics:
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
     - R-squared (R²) score

6. **Insights & Recommendations**
   - Determine which factors most influence spending
   - Provide actionable business recommendations

##  Business Applications

This analysis helps e-commerce businesses:
- Understand customer behavior patterns
- Optimize resource allocation between website and app development
- Develop targeted marketing strategies
- Improve customer retention and revenue


### Prerequisites
- Python 3.x
- Jupyter Notebook
- Libraries listed in the first code cell

### Installation
1. Clone the repository
2. Install required packages: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Open the notebook in Jupyter: `jupyter notebook Consumer_Spend_Prediction_ML_Model.ipynb`

## 📈 Key Findings

Right now, the mobile app is linked to more customer spending than the website. But before deciding what to focus on, it’s a good idea to dig a bit deeper.

You should look at how Length of Membership relates to both App and Website usage. For example:

1. Do older customers prefer one platform over the other?

2. Are new users more active on the app?

Answering these kinds of questions can help you decide whether to:

a. Improve the website to make it more engaging, or

b. Keep investing in the app, since it's already performing well.

The best decision depends on what your users are doing and what the company wants to achieve.

## Model Summary

### Coefficient Interpretation

| Feature                  | Coefficient | Interpretation                                                               |
| ------------------------ | ----------- | ---------------------------------------------------------------------------- |
| **Avg. Session Length**  | +25.98      | Spending increases by **\$25.98** for every unit increase in session length. |
| **Time on App**          | +38.59      | Spending increases by **\$38.59** for every unit increase in app time.       |
| **Time on Website**      | +0.19       | Spending increases slightly by **\$0.19** per unit increase in website time. |
| **Length of Membership** | +61.27      | Strongest predictor: adds **\$61.27** per extra year of membership.          |

These coefficients were obtained using a multiple linear regression model. All variables were assumed to be linearly independent with minimal multicollinearity.

### Model Evaluation

| Metric                   | Value  |
| ------------------------ | ------ |
| Mean Absolute Error      | 12.02  |
| Mean Squared Error       | 240.10 |
| Root Mean Squared Error  | 15.49  |
| R² Score (Explained Var) | 0.98   |

R² score of **0.98** indicates the model explains **98%** of the variability in customer spending — a strong fit.

## 🤝 Contributing

Contributions are welcome! Please fork the repository and create a pull request with your improvements.

## ✉️ Contact

For questions or feedback, please open an issue in the repository.
