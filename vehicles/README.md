This is a readme file for the data analysis of a coupons.csv (pushing coupons to drivers for various eating/drinking establishments on their route) using python libraries - Pandas, Seaborn, Matplotlib etc.
The idea is to slice and dice the data and look at subgroups that accept coupons more readily.
This way one can be more targeted in terms of pushing coupons to the right segment (where segment is defined as a collection of 1 or more attributes of the data set)

**
As a start the notebook zeeiyerWork-Module5-prompt.ipnyb 
- loads the coupons.csv file (please change the code based on the relative location of the coupons file)
- Explores the data sets.
- And executes the analysis for just BAR Coupons.
- And executes something similar for high end restaruant Coupons (20-50$ price range)

**
Further analysis is about slicing and dicing the variables to find high-coupon acceptance groups across coupon segments for targeted marketing.
**
Needed files:
- NOTES: README.md
- CODE: zeeiyerWork-Module5-prompt.ipynb (has suitable notes for additional guidance)
- DATA: coupons.csv (needs to be relocated in the right place to ensure that you do not encounter "file-not-found" errors)

DATASET NOTE: 
- 74 duplicate rows that can be safely removed.
- Further dropna results in the majority of rows being dropped since seems like cars have only 108 entries out of the total dataset in excess of 12000 rows. Hence using fill.
