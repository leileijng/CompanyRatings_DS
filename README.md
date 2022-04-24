# About

This is our Mini-Project for SC1015. We used this [dataset](https://www.kaggle.com/datasets/vaghefi/company-reviews) from kaggle on Company Reviews. For detailed walkthrough, please view the source code in the following order:

1. [Data Preperation](https://github.com/leileijng/CompanyRatings_DS/blob/main/data_preparation/CompanyRating_Preprocessing_2.ipynb)
2. [Exploratory Data Analysis](https://github.com/leileijng/CompanyRatings_DS/blob/main/EDA/EDA_1.ipynb)
3. [Machine Learning](https://github.com/leileijng/CompanyRatings_DS/blob/main/Machine%20Learning/Model%202.ipynb)

Our raw data and processed data can be found in this [folder](https://github.com/leileijng/CompanyRatings_DS/tree/main/dataset)

# Contributors
- @leileijng: Data Extraction, Data Preperation, EDA, Light GBM Model
- @davidteyby: Data Preperation, EDA, PCA
- @kellykkhoo: EDA, Data Visualisation, Linear Regression Model

# Problem Definition
- Analyse company performance in terms of **Ratings** & **Employees Happiness Score**
  - **Prediction**: Company Ratings & Working Happiness Score
  - **Analysis**: Find most important features affecting work happiness
  - **Recommendation**: Find anomalies company ratings and advise them

# Models Used
1. Linear Regression Model
2. Stepwise Linear Regression Model
3. Principal Component Analysis with Linear Regression Model
4. Light GBM

# Libraries
- numpy
- pandas
- seaborn
- matplotlib
- pickle
- sklearn
- statsmodels.api
- lightgbm
- datetime
- time

# Files
## Jupyter Notebook #1: data_preparation/CompanyRating_Preprocessing_2.ipynb
The code in this notebook is used to extract data from the original CSV file and prepare it for EDA. 
- Cleaned our data by dropping unnecessary columns
- Removed rows with missing data 
- Dropped rows with low credibility (too few reviews)
- Changed the format of the **ratings** column from a dictionary to 5 separate columns
- Changed **employees** and **revenue** from a categorical values to numerical values
- Calculated **average salary** based using a simple average
- Grouped companies into 10 separate **industries**
- Exported the cleaned dataset as .xlsx and .pickle

## Jupyter Notebook #2: EDA/EDA_1.ipynb
In this notebook, we explored the cleaned dataset for the relationship between the different variables.
- Statistical distribution & summary of target variables (**rating** and **work happiness**)
- Distribution of numerical explanatory variables
- Correlation of explanatory variables and target variables
- Distribution of categorical variables (**employees**, **revenue** and **industry**)
- Correlation between explanatory variables and target variables, sorted by **industry**

## Jupyter Notebook #3: Machine Learning/Model 2.ipynb
In this notebook, we implement various machine learning models in order to predict **company rating** and **work happiness**.
- Normalised columns except for **rating**
- Split data into training and test set
- Fit data into a **linear regression model** to predict **work happiness**
- Fit data into a **stepwise linear regression model** to predict **work happiness**
- Used **PCA** to reduce the number of input variables
- Explored the effects of the **number of principle components** on model performance
- Fit data into a **linear regression model** to predict **work happiness** after reducing 22 variables to 7 principle components
- Explored the **relative importance** of the original 22 input variables
- Fit data into a **Light GBM model** to predict **rating**
- Explored the **relative importance** of the input variables in the **Light GBM model**
- Tabulated the anomalise based on our **Light GBM model** (companies whose ratings deviated the most from our prediction)

