# Car Price Prediction Using Machine Learning

## Exploring the Impact of Brand, Features, Horsepower, and Mileage on Car Pricing with Predictive Models
---
## Table of Contents
1. [Overview](#overview)  
2. [Data Preparation](#data-preparation)  
   2.1 [Data Collection](#data-collection)  
   2.2 [Data Cleaning](#data-cleaning)  
   2.3 [Data Exploration (Charts and Descriptions)](#data-exploration-charts-and-descriptions)  
3. [Feature Engineering](#feature-engineering)  
4. [Modeling and Evaluation](#modeling-and-evaluation)  
   4.1 [Model Selection and Training](#model-selection-and-training)  
   4.2 [Model Evaluation and Results](#model-evaluationand-results)  
5. [Conclusion](#conclusion)  
6. [Recommendations for Future Work](#recommendations-for-future-work)  
7. [Installation](#installation)

---

### Overview
This project tackles the challenge of predicting car prices through a structured ETL process, feature engineering, and Linear Regression modeling.
### ETL
#### Data Cleaning
We identified and analyzed unique values in the categorical columns to detect inconsistencies, corrected spelling errors in the company_name column using a custom function, and confirmed no duplicated records, ensuring data consistency and integrity.

#### Data Exploration (Charts and Descriptions)
The data exploration revealed that car prices are strongly influenced by features like car dimensions, engine size, and horsepower, with negative correlations to mileage. Luxury brands (Jaguar, Buick, Porsche) have the highest prices, while economy brands (Chevrolet, Nissan, Honda) are the lowest. Categorical factors such as fuel type, body type, and drive wheel configuration also impact pricing. Count plots highlighted the distribution of car body types, aspiration, and fuel types across the dataset.

### Feature Engineering
In the feature engineering process, I selected significant columns based on correlation analysis, choosing features that had strong relationships with car prices. The selected columns include both categorical and numerical variables such as engine type, fuel type, car body, aspiration, cylinder number, drive wheel, curb weight, and more.

To prepare the data for modeling, I transformed the categorical variables into numerical form using one-hot encoding. This created dummy variables for categorical columns like enginetype, fueltype, carbody, aspiration, cylindernumber, and drivewheel, while avoiding multicollinearity by dropping the first category in each. The resulting dataset contained both the original numerical features and newly created binary columns, making the data ready for further analysis and modeling.

Additionally, I standardized the numerical columns (e.g., curbweight, carlength, carwidth, enginesize, etc.) using StandardScaler to ensure they had a mean of 0 and a standard deviation of 1. This scaling helps improve model performance, particularly for algorithms sensitive to feature magnitude.
### Modeling

#### Model Selection and Training
Linear Regression was chosen for its simplicity and effectiveness in predicting continuous variables, such as car prices. The model was trained using the dataset, enabling it to learn the relationship between the features and the target variable.

#### Model Evaluation and Results
The model's performance was assessed using Mean Squared Error (MSE) and R-squared (R²) metrics. It achieved an MSE of 10,209,920.15 and an R² of 0.87, indicating that it explains 87% of the variance in car prices, reflecting a good fit.

### Conclusion
The model successfully captures key relationships in the data, achieving an R² of 0.87, highlighting its effectiveness for accurate price prediction.

### Recommendations for Future Work
Model Diversity and Hyperparameter Tuning: Explore advanced algorithms like Random Forest or Gradient Boosting while optimizing hyperparameters through techniques like Grid Search to improve predictive performance.

Outlier Analysis: Conduct a thorough examination of outliers in the dataset to assess their impact on model accuracy and implement strategies to mitigate their influence.

Integration of External Data: Incorporate external datasets, such as economic indicators or market trends, to enhance the model's context and predictive capabilities.
### Installation
To set up this project, clone the repository and install the required libraries:

```bash
git clone https://github.com/Moustafa-abdelsattar/CognoRise_infotech.git
cd CognoRise_infotech
pip install -r requirements.txt
