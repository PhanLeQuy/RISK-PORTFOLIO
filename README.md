# RISK-PORTFOLIO
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/35eefc84-8062-468f-8d76-94c863b2e1a0" />
<img width="1919" height="1021" alt="image" src="https://github.com/user-attachments/assets/0e8e5406-5240-4398-9fd7-109f084c17d9" />
<img width="1916" height="1016" alt="image" src="https://github.com/user-attachments/assets/f6a86552-8c29-4a6c-b849-148d19d0e02a" />


I. PROJECT OVERVIEW
For financial institutions (commercial banks, funds,...) and finance companies, the occurrence of bad debts on loans during operations results in significant losses. One way to manage and mitigate this risk is for financial institutions (banks, funds, etc.) and finance companies to set aside specific provisions for each loan and general provisions for all loans.

My project this time is to create a monitoring and analysis report of the retail credit portfolio to identify potential risks hidden within loans --> Optimize the amount of provisions to be set aside.

II. OBJECTIVES
TO OPTIMIZE PROVISIONS

I calculated the TRIGGER INDICATORS (early warning system - EWS) including:
FPD - First Payment Default
SPD - Second Payment Default
TPD - Third Payment Default
NST90 - Non Starter 90 days
--> Loss --> Loss to Sale

Then I calculated these indicators for the retail credit portfolio classified by disbursement period (here I divided it by month).

Then I calculated the provisions for the credit portfolio (Group 2 debt -> Group 5 debt). And from there, I performed the classification of credit categories by product and region to identify WHERE CREDIT RISK CONCENTRATING

*Note: I classified the debt and calculated the provision for bad debts according to the proposals of the State Bank of Vietnam (SBV) through Circular 31/2024 and Resolution 86/2024.

Finally, I calculated the organization's risk-adjusted return.

III.  DATA ARCHITECTURE
- Pipeline - 4 layer Temporary Table:

FACT_LOAN_MANAGEMENT --> #STEP1_BASE --> #STEP2_MAX_DPD --> #STEP3_FLAGS  --> #STEP4_DEFAULT_METRIC  --> #STEP6_FPD_SPD_TPD_EWS  --> #VINTAGE_LOSS_TO_SALE

Final analytical table for Vintage / Loss / Risk-Adjusted Return

IV. KEYINSIGHT

