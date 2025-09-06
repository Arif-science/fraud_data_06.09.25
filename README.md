# fraud_data_06.09.25
Drop unnecessary columns
There is 'Date of transaction' column. Convert it to datetime data type using pd.to_datetime. (add dayfirst=True as hyperparameter)
Create 'transaction_year', 'transaction_month' and 'transaction_day' columns from it. Example as below:
data['column_name'].dt.year

data['column_name'].dt.month

data['column_name'].dt.day

After creating above mentioned columns drop 'Date of transaction' column
Check missing values
Create new_data from original data using LabelEncoder (convert categorical to numerical)
Declare inputs from new_data, and inputs_cat form data. Fill missings for inputs_cat if there any with 'Missing value'.
Train test split step. X_train, X_test, y_train, y_test and X_train_cat, X_test_cat, y_train_cat, y_test_cat has to be created.
Concat 2 tables of default and optimized models Gini result and decide which of them is the best one.
5. Feature importance and Shap Value analysis and
Variables with Importance > 1% have to be selected.

For the best model check result of SHAP and importance, remove variables which has no impact to output.

6. Build best model using final inputs
train best selected model on final inputs , if result is higher than 40% model will proceed into production environment.
7. Deployment
Deploy model on fraud_deploy_data.xlsx
Create 'probability of fraud' column
Extract data where 'probability of fraud' is higher than 10%
