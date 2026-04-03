# RISK-PORTFOLIO
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/35eefc84-8062-468f-8d76-94c863b2e1a0" />


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

Then I calculated the provisions for the credit portfolio (Group 2 debt -> Group 5 debt). And from there, I performed the classification of credit categories by product and region.

*Note: I classified the debt and calculated the provision for bad debts according to the proposals of the State Bank of Vietnam (SBV) through Circular 31/2024 and Resolution 86/2024.

Finally, I calculated the organization's risk-adjusted return.

III.  DATA ARCHITECTURE
Pipeline - 4 layer Temporary Table

FACT_LOAN_MANAGEMENT
	 I
	v
#STEP1_BASE
	 I
	v
#STEP2_MAX_DPD
	 I
	v
#STEP3_FLAGS
	 I
	v
#STEP4_DEFAULT_METRIC
	 I
	v
#STEP6_FPD_SPD_TPD_EWS
	 I
	v
#VINTAGE_LOSS_TO_SALE

Final analytical table for Vintage / Loss / Risk-Adjusted Return

