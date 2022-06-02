## Credit-Card-Transaction-Fraud-Analytics

Notice: For security purpose, all files are stored under master branch.


### Project Goal:

This project trained and selected a real-time supervised machine learning model based on historical labeled credit card transactions data from a US government organization to help detect future credit card transaction frauds. 


### Project Overview:

This project broke up model building into three steps, which were data exploration, data preparation, and model building. 

In the data exploration section, we examined the dataset by identifying each variable, calculating the descriptive statistics for the numeric variables, and calculating the basic traits for the categorical variables. 

Then, we did data preparation with data cleaning and variable creation. For data cleaning, we filtered transactions by only including transactions with type “P” and dealt with other kinds of dirty data in datasets. With the cleaned data, we created 1012 variables through target encodings, applying Benford’s Law, and feature combinations based on domain experts’ insights. 

Lastly, we selected 20 variables from the 1012 created variables to build the final models. For the selection process, we first used the KS method to select 80 variables and used wrapper– forward selection to select the top 20 best variables for model buildings. After comparing 5 models with different hyperparameters, we decided to use LightGBM as our final model for its high fraud detection rate (FDR) at 3% and relatively low overfitting problem. Using this model, we can eliminate 56.48% of fraud transactions, by declining 3% of the transactions. With this model and the 3% threshold, we will be able to save the company around $190K per year. 


### Folder Explaination:

This project is divided into 4 folders and 1 summary report. All implementation codes can be found under folders. Summary report gives detailed brackgrounds of this project, retionales behind the method used and explainations of each step.

(1) Data Exploration Part: (Folder)
- Practice of “Data Exploration” part listed above.
- Csv file is the original dataset.
- Ipynb file is the code used in this step.
- Pdf file is the results of this step.

(2) Data Cleaning and Create New Variables: (Folder)
- Practice of “Data Preparation” part listed above.
-	Csv file is the original dataset.
-	Ipynb file is the code used in this step.
-	Pdf file is the results of this step.

(3) Feature Selection: (Folder)
-	Practice of “Model Building” (feature selection) part listed above.
-	Csv file used in this step can be acquired from previous step. (not provide here because of the size limitation)
-	Ipynb file is the code used in this step.

(4) Fit Model & Performance Table & Graph: (Folder)
-	Practice of “Model Building” (model building and verifying) part listed above.
-	Csv files (*2) are the datasets used in this step. (Results of last step)
-	“step1 – transactions models” fits several models and make best choice.
-	“step2 – performance table” applies the best model on datasets.
-	“step3 – draw FDR selection Graph” uses business insights to test the potential savings of the model.

(5) Credit Card Fraud Analytics Report: (Report)
- Summary Report of all steps listed above.
