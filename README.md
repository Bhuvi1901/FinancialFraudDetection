# Fraud Detection and Prevention in Banking Transactions

## Overview

Built a machine learning solution to detect fraudulent transactions using user and transaction behavior. The project focuses on improving accuracy in identifying high-risk transactions in financial data.

##  Project Structure

### 1. Data Exploration
- Fraud and legitimate transaction counts were analyzed to understand the extreme class imbalance.
- Distribution plots and count plots were created to visualize trends by transaction type, amount, and account age.

### 2. Preprocessing
- Non-numeric features were encoded using label encoding. Amount and account balance fields were scaled using StandardScaler.
- SMOTE (Synthetic Minority Over-sampling Technique) was used to balance the dataset, preventing model bias toward non-fraudulent transactions.

### 3. Modeling
- Models used include Logistic Regression, Random Forest, XGBoost, and a StackingClassifier that combines multiple models for better generalization.
- Each model was evaluated with metrics like ROC-AUC, recall (for frauds), and confusion matrices.

### 4. Evaluation and Analysis
- Feature importance was extracted from tree-based models to understand what variables contribute most to fraud detection.
- Final stacked model achieved high accuracy while maintaining reasonable fraud recall, a critical factor in fraud analysis.

### 5. Data Visualization
- Designed a [Power BI dashboard](https://github.com/user-attachments/assets/5982510f-894c-40c6-bbc9-2f2790694fdd) to provide real-time insights into:
    - Fraud volume and amount across transaction types
    - High-risk accounts and the largest fraudulent transactions
    - Fraud transaction frequency over hourly time steps
    - Transaction types most associated with fraud, via interactive treemaps 
      and donut charts


 ![image](https://github.com/user-attachments/assets/5982510f-894c-40c6-bbc9-2f2790694fdd)
  
## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Random Forest
- Logistic Regression
- Stacking classifier
- Power BI

## Output

- The final stacking classifier achieved 99.77% accuracy, with a strong performance in identifying fraudulent transactions.
- Although fraud cases were rare, the model captured 68% of fraud instances, a major improvement over baseline.


  
## How to Use

- ### Clone this repository:
  ```bash
  git clone [https://github.com/Bhuvi1901/FinancialFraudDetection](https://github.com/Bhuvi1901/FinancialFraudDetection)
  ```
- ### Navigate to the project folder:
  ```bash
  cd FinancialFraudDetection
  ```
- ### Install dependencies:
  ```bash
  pip install -r requirements.txt
  ```
- ### Run the Jupyter Notebook to execute the workflow.

## Future Improvements

- Implement real-time fraud detection using a streaming pipeline.
- Experiment with deep learning for improved recall and deploy the model as an API.
