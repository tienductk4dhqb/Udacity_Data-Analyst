# Prosper Loan Data
##  prosperLoanData.csv


## Dataset
Loan Data from Prosper: This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. 
Download dataset:  
https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000  
Detail description:
https://docs.google.com/document/d/e/2PACX-1vQmkX4iOT6Rcrin42vslquX2_wQCjIa_hbwD0xmxrERPSOJYDtpNc_3wwK_p9_KpOsfA6QVyEHdxxq7/pub  
See this data dictionary to understand the dataset's variables.  
https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit?usp=sharing  

## Summary of Findings  
I have researched and analyzed it using excel along with the data descriptor file 'Prosper Loan Data.xlsx'  
to filter out the necessary information (Select relevant columns, few null values, clear data...).  
Define the number of columns to use in the project  
Clean some invalid data  
Univariate analysis  
Binary analysis  
Multivariate analysis  
All are analyzed and modeled by displaying meaningful charts, make comments after each chart.  
-> All analytical views, comments from univariate have reached the final conclusion, after multivariate analysis and modeling  
1. What factors affect a loan's outcome status?   
EmploymentStatus, IncomeRange, ProsperScore, LoanOriginalAmount, LoanCurrentDaysDelinquent, LoanMonthsSinceOrigination are all related to and affect LoanStatus.  `
2. What affects the borrower's APR or interest rate?  
BorrowerRate, LenderYield are all related to and influence BorrowerAPR  
3. Is there a difference between loans depending on how much is the original loan amount?  
3.1. What is the average interest rate on a large loan? What is the interest rate for a small loan?  
Small loans have higher interest rates than large loans. The difference is about 0.12 or 12%.  
3.2. Who borrows big? Who borrows small?  
The difference between borrowing more(33,944) and borrowing less(31896) of the borrower is Employed is not significant.  
The difference is most obvious in Full-time when borrowers with less(20008) need to borrow are nearly twice as large as to borrow more(6036).  
3.3. Are small loans past due or defaulted more often? Small loans overdue compared to large loans are almost the same.  
High distribution between 0-250 days, and low from about 250 days onwards.  
In general, this is only a one-sided conclusion and it will not be entirely true, because the reality of loans in real life will be much more complicated.  

## Key Insights for Presentation  
**What factors affect a loan's outcome status?**  
I chose the **LoanStatus** column as the main column to focus on finding relevant data for the question.  
**LoanStatus** is described as:  
The current status of the loan: Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.  
Use the file 'Prosper Loan Data.xslx' to better understand the dataset, select columns whose descriptions are supposed to be related to **LoanStatus**  
EmploymentStatus The employment status of the borrower at the time they posted the listing.  
IncomeRange The income range of the borrower at the time the listing was created.  
LoanOriginalAmount The origination amount of the loan.  
LoanCurrentDaysDelinquent The number of days delinquent.  
LoanMonthsSinceOrigination Number of months since the loan originated.  
ProsperScore A custom risk score built using historical Prosper data  
Starting with the project I will define the columns to use in the project.  
Next, clean data feels inappropriate (null many, incorrect data...)  
Univariate analysis  
Discover relationships between variables for **LoanStatus**, model and visualize with charts.  
Binary analysis  
Create a relationship between **LoanStatus** with variables of type categories, and number.  
Comments and conclusions after displaying relationships by chart.  
Multivariate analysis  
The final step of data analysis and modeling, creating multivariate relationships between **LoanStatus** and the remaining variables, modeling by plot.  
After modeling I have seen more clearly the relationship of the **LoanStatus** variable with the rest of the variables, specifically:  
LoanOriginalAmount increase **LoanStatus** tends to change  
LoanCurrentDaysDelinquent increases **LoanStatus** tends to change **LoanStatus** = Past due++  
ProsperScore increases (risk score decreases) **LoanStatus** tends to change according to LoanOriginalAmount  
In conclusion, the factors that change **LoanStatus** include:  
**EmploymentStatus
IncomeRange
LoanOriginalAmount
LoanCurrentDaysDelinquent
LoanMonthsSinceOrigination
ProsperScore**