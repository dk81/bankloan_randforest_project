# Project On A Random Forest Model On Bank Loan Data
---

This was for a school project in Late November / December 2019. 

&nbsp;

## Project Brief

A (Czech) bank wants to automate their loan approval process.  The dataset contains 606 successful loan and 76 not successful loans along with their information and transactions. These loans are for existing clients.

The data was pulled from the school database. However this bank data can be found online through links such as [this link](https://relational.fit.cvut.cz/dataset/Financial) with its information from [here](https://sorry.vse.cz/~berka/challenge/pkdd1999/berka.htm)

&nbsp;

## Dataset Pull

The .csv from the database data pull is included in this repository. I have provided the Python code with the SQL parts in the .ipynb file. Note that the login and password details connecting to the school database is cut out. 

Columns from the pulled data are:

* account_id - Bank client ID                   
* frequency - frequency of issuance of statements          
* loan_amount - Loan amount            
* loan_date - Date of Loan
* loan_duration - Duration Of Loan  
* loan_pmt - Loan Payment               
* status - Status Of Paying Off Loan (Look at Bottom)            
* card_type - Credit card type    
* disp_type - Disposition type (Owner / User)                  
* num_tsns  - Number of transactions for the account            
* last_tsn_date - Last transaction date               
* num_cc_withdraw  - Number of Credit Card Withdrawals            
* num_credit_in_cash  - Number Of Credit In Cash occurences        
* num_collect_from_diff_bank - Number of Collections From Another Bank
* num_cash_withdraw - Number of Cash Withdrawals         
* num_remit_to_diff_bank - Number Of Remittances To Another Bank   
* avg_cc_withdraw - Average Amount Of Credit Card Withdrawals For The Account            
* avg_credit_in_cash - Average Amount Of Credit In Cash For Account          
* avg_collect_from_diff_bank - Average Collection Amount From Another Bank For Account  
* avg_cash_withdraw - Average Cash Withdraw Amount For Account          
* avg_remit_to_diff_bank - Average Remittance Amount To Another Bank For Account     


&nbsp;

## Loan Status

In the data, the status variable refers to loan statis for the bnak client. There are four letters which are A, B, C and D. From [the website](https://sorry.vse.cz/~berka/challenge/pkdd1999/berka.htm) it says that:

* 'A' stands for contract finished, no problems,
* 'B' stands for contract finished, loan not payed,
* 'C' stands for running contract, OK so far,
* 'D' stands for running contract, client in debt

The letters A and C are changed into 1s for loan approval and the letters B and D turn into 0 for no loan approval.

&nbsp;

## Random Forest Model & SHAP Summary Plots

For the loan approval model, a random forest was selected. The random forest would use all of the features listed above. SHAP values would be used as well to determine determine which features / variables have the greatest impact on a bank cliebnt being approved for a loan or not. 


&nbsp;
