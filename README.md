# Prosper-Loan-Data

## Dataset

> This dataset used for this exploration contains information about the loans taken by various individuals from a lending entity. It has 81 variables that describes the profile of each borrower.

### Data Structure

> The data has information on 113937 loans, described with 81 features. The variables are mostly numeric ``61``, with more floats datatype ``50`` than integers ``11``. There are also ``3`` boolean datatypes and ``17`` strings. 

### Feature of Interest

> I am particularly interested in understanding the factors that impact the interest rate - ``BorrowerAPR`` on loans.

### Select Features for Investigation

> For the purpose of this case study we are going to limit our exploratio to the variables below.

#### Variables
> - ``Term``: The length of the loan expressed in months.
> - ``LoanStatus``: The current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
> - ``BorrowerAPR``: The Borrower's Annual Percentage Rate (APR) for the loan.
> - ``EmploymentStatus``: The employment status of the borrower at the time they posted the listing.
> - ``EmploymentStatusDuration``: The length in months of the employment status at the time the listing was created.
> - ``IsBorrowerHomeOwner``: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
> - ``DebtToIncomeRatio``: The debt to income ratio of the borrower at the time the credit profile was pulled. This value is Null if the debt to income ratio is not available. This value is capped at 10.01 (any debt to income ratio larger than 1000% will be returned as 1001%).
> - ``ListingCategory (numeric)``: The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans
> - ``StatedMonthlyIncome``: The monthly income the borrower stated at the time the listing was created.
> - ``LoanOriginalAmount``: The original amount of the loan.
> - ``ProsperScore``: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009.


## Summary of Findings

> First we performed a univariate exploration of each variable selected to establish their distributions and any interesting information from the variable. We moved to bivariate exploration and compared some of the variables to establish the presence of any relationships and finally we had a multivariate exploration to dig deeper into some relationships we had established up to that point.

> The following are interesting insights we picked up:

> - BorrowerAPR has a weak negative correlation with all the numeric variables except debt-to-income ratio where it has a weak positive relationship.
> - Self-employed, employed and full-time high income earners who are home owners paid less interest for similar amount of loan compared to their counterparts who are not homeowners.
> - Low scoring borrowers in the custom score paid high interests compared to high-scoring borrowers, across homeowners and non-homeowners. Also, there is a marginal advantange to being a homeowner, as they paid less interest compared to the non-homeowners for each of the Prosper score categories.
> - On ProsperScore and LoanOriginalAmount, when plotting for homeowners and non-homeowners, the viz shows that homeowners got much more loans than their non-homeowner counterparts in the same score level.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.
> For the presentation, the focus is on the main variable of interest - BorrowerAPR. The is to show the relationships between interest and some of the variables we selected. 

> First we give a definition of BorrowerAPR variable, then its distribution is displayed. Then define and display the distributions of some of the important variables in our dataset. Subsequently, the key relationships are introduced and explained. 
