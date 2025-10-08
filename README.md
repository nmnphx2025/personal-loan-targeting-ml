# Personal Loan Campaign — Customer Conversion Model  
Bootcamp Project-Great Learning UT Austin Post Grad Program in Business Applications of Machine Learning  | Synthetic Data | Decision Tree Classifier

## 📌 Project Overview  
This project builds a predictive model to identify depositors most likely to accept a personal loan offer. Using a synthetic dataset from a bootcamp assignment (originally sourced from Kaggle), I performed exploratory data analysis (EDA), feature engineering, and classification modeling to support targeted marketing and campaign forecasting.

## 🎯 Business Objective  
A regional bank aimed to convert liability customers (depositors) into asset customers (loan holders). The goal was to predict which customers were most likely to accept a personal loan offer, enabling more efficient campaign targeting and revenue forecasting.

## 🧪 Methods  
- **EDA**: Univariate and bivariate analysis to identify key drivers of loan acceptance  
- **Preprocessing**: Dropped highly correlated features (e.g., Experience vs Age), treated outliers and categorical variables  
- **Modeling**: Built a Decision Tree classifier using scikit-learn; tuned with pre-pruning and evaluated using recall as the primary business metric  
- **Validation**: 70/30 train-test split; confusion matrix and performance metrics used to assess model generalizability

## 📊 Key Findings  
- Customers with **higher education**, **family size of 3–4**, **CD accounts**, and **income below $100K** were more likely to accept loans  
- **Income**, **Family**, **Education**, and **CCAvg** were the strongest predictors  
- Online banking usage and credit card ownership had minimal predictive value  
- Recall was prioritized to reduce missed conversion opportunities

## 📈 Model Performance  
| Metric     | Initial Model | Pruned Model |
|------------|---------------|--------------|
| Accuracy   | 0.986         | 0.978        |
| Recall     | 0.933         | 0.785        |
| Precision  | 0.927         | 1.000        |
| F1 Score   | 0.930         | 0.880        |

> Business decision: Favor higher recall to maximize campaign reach and minimize lost revenue.

## 🧠 Business Recommendations  
- Target marketing toward high-propensity segments identified by the model  
- Use model outputs to generate best/likely/worst-case campaign ROI scenarios  
- Extend modeling to include repayment risk or lifetime value for deeper financial planning

## 📁 Repository Contents  
- `notebook.ipynb`: Full EDA, preprocessing, and model build  
- `data/`: Synthetic dataset used for training and testing  
- `figures/`: Exported visuals (feature importance, confusion matrix, EDA plots)  
- `README.md`: Project summary and instructions
  
- ## 📚 Dataset Notes  
- Source: Bootcamp dataset derived from [Kaggle’s Personal Loan Campaign dataset](https://www.kaggle.com/datasets)  
- This version is sanitized and synthetic for public sharing  
- No proprietary or personally identifiable information included  
- See `data/synthetic_personal_loan.csv` for the version used in this project

## 🛠️ How to Run  
1. Clone the repo  
2. Create a Python environment and install dependencies:  
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
