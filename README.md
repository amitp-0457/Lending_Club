# Project Name -Lending Club case study
Lending Club is a finance company which specialises in lending various types of loans to urban customers
When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile.
Two types of risks are associated with the bank’s decision:
   1.If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

   2.If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company

The data given below contains information about past loan applicants and whether they ‘defaulted’ or not. 
The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.


## Table of Contents
* [General Info]
* [Technologies Used]- panda,matplotlib,seaborn
* [Conclusions]
* [Acknowledgements]


## General Information
This case study is done to avoid the defaulters before accepting the loan request from them.
Also we need to be careful that the applicant who is likely to repay the loan should not ignored or missed, else this a loss to the business for Lending Club

This involves the details analysis of the columns() provided in the data set. Following classification need to done to analyse
Broadly the data set is divided into 3 types of variables :-
     1. Applicant related info(like demography,age,occupation, etc)
     2. Loan Characterstics variable (amount of loan, interest rate, purpose of loan,etc)
     3. Customer behavior variable (such as delinquent 2 years, revolving balance, next payment date etc.)

Now, the customer behavior variables are not available at the time of loan application, and thus they cannot be used as predictors for credit approval
Also the ones marked 'current' are neither fully paid not defaulted, therefore need to give less emphasis.


## Conclusions

- After removing unnecessary colummn for the case study
- Before removal of outliers, Old Shape:  (39717, 25)
- After removal of outliers,New Shape:  (37874, 25). Based upon Annual income, outliers were removed

- CORRELATION RELATIONSHIP
     Analysis based upon correlation Matrix :-
       1. Loan amount, investor amount, funding amount are strongly correlated(near to 1).
       2. Annual income and DTI(Debt-to-income ratio) is negatively correalted(-0.075).
          Debt income ratio is the percentage of a borrower's monthly gross income that goes toward paying debts. 
          This means when annual income is low  then DTI is high & vice versa.
       3.Positive correlation between annual income and employment years(0.19) which means borrower income increases with employment  length ie work experience
       4. Going ahead we will work only with 'Loan Amount as the Loan Amount, Funded Amount and Funded Amount Inv are strongly correlated. This we can confirm further by seeing the distribution plot.


- Loan Amount Requested (loan_amnt),Approved Funded Amount by LC(funded_amn) , Funded Amount Inv(funded_amnt_inv)
     Distribution of all three amounts for all similar. Therefore loan amount column was used for rest of our analysis.

-  Univariate Analysis :-
     1. Loan amout is spread between 5000 -15000
     2. Most of the borrower's Annual incomes are in range of 40000- 80000
     3. Most of the Interest rates on loans are in range of 10% - 15%
     4. Most of the loans were taken for the purpose of debt consolidation & paying credit card bill.Charged off is higher in debt_consolidation.
     5. Most of them living in rented home or mortgage  home. Therefore " Charged off"  is high in these category as the application count is high.
     6. Those who had taken loan to repay in 36 months had more percentage of number of applicants getting  charged off as  compared to applicants who had taken loan for 60 months

- BiVariate Analysis :-
    Assumptions made :-
       - We need to form category for the numerical  continous variable . They are as follows
                 a)loan_amnt
                 b)annual_inc
                 c)int_rate
                 d)dti
       - we need to analyze the loan status  vs  important columns which might have played important role in charged off loans.
     
     Analysis :-
 
       - Annual Income range 80000+  has less chances of charged off.
           Annual Income range 0-20000 has high chances of charged off.
           With increase in annual income charged off proportion got decreased. 

       - Grade "A" has very less chance of charged off.
            Grade "F" and "G" have very high chance of charged off.
            Chances of charged off is increasing with grade moving from "A" towards "G"

       -  Sub Grade "A" has very less chance of charged off.
              Grade "F" and "G" have very high chance of charged off.
              Among the grades as A1,A2 ...A5 varies, charged off proportion also increased
              Similarly this is applicable for other Grades (B,C....G) 

       - Interest rate < 10% has very less chances of charged off.
            Interest rate > 16% has good chnaces of charged off as compared to other category interest rates.
            Charged off proportion is increasing with higher intrest rates. 

       - Work experience less than 1 year of experience have high chances of getting charged off. Rest years  of experience remains same.
       
       - Small Business applicants have high chances of getting charged off.

       - Low DTI gets low inteerest rate.There is slight increase in interest rate with increase in DTI.
     
       - Intrest rate is increasing with an increase in loan amount.

       - Average intrest rate is highest for small business purpose ie it had to pay the loan with more interest rate then any other purpose.     


## Technologies Used
- library - version 1.0
- library - version 2.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements



## Contact
Created by [@githubusername] - https://github.com/amitp-0457
Git Hub Link

https://github.com/amitp-0457/Lending_Club
