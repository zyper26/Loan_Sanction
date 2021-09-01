# Predict the loan sanction Amount

Buying a house requires a lot of careful planning. Once you have finalized your budget and the house that you want to buy, you must ensure that you have sufficient funds to pay the seller.

With rising property rates, most people avail home loans to buy their dream houses. The bank only lends up to 80% of the total amount based on a person's finances (salary, outgoing expenses, existing loans, etc.). You will need to make the rest of the payment yourself after the bank tells you how much they can lend.

# Task

You work for XYZ bank. Predict the loan amount that can be sanctioned to customers who have applied for a home loan using the features provided in the dataset.


# Steps:

  1. Loading dataset
  2. Exploratory data analysis (EDA)
  3. Handling missing values and outliers
  4. Encoding categorical variables <br/>
      i. Used one hot multiclass encoding on some variables. Based on the winning solution of KDD 2009 Cup i.e. we are going to limit the number of categories in             the these 3 variables to 10 most frequent labels. <br/>
      ii. Used a custom code where for any column we can choose how many values in that variable we want to keep.
  5. Split the dataset into train and test
  6. Dividing into X and Y sets for the model building
  7. Scaling the numerical variables  <br/>
      i. Took care of data leakage on numerical variables by using fit_transform on training data but transform on validation and test data. <br/>
      ii. Used Robust Scaler, Standard Scaler, MinMaxScaler based on the distribution of variables. <br/>
  8. Model Buidling <br/>
      i. We will run classification to identify whether the loan saction amount will be zero or not. <br/>
          a. Logistic Regression <br/>
          b. Random Forest Classifier <br/>
      ii. Now, regression to get the actual amount to be sanctioned to the customers. <br/>
          a. Linear regression with RFE (feature selection method) <br/>
          b. Ridge regression <br/>
          c. Lasso regression <br/>
  9. Creating a submission file <br/>
       i. Utilized both the classification and regression by first predicting with classification method (Whether to we should give loan or not) then used regression on the customers whom we should give to identify the amount to be given.
       
     
 # Target variable distribution
 
 https://github.com/zyper26/Loan_Sanction/blob/main/target_variable.png
