# Quantium Retail Analytics

End-to-end retail analytics project analyzing chip purchasing behavior and store trial performance for a supermarket client. Built in Python using pandas, seaborn, matplotlib, and scipy.

## Project Overview

This project was completed as part of the Quantium Data Analytics job simulation on Forage. The work is split into two tasks:

- **Task 1:** Understand chip purchasing behavior across customer 
  segments to identify who buys chips and what drives their spend
- **Task 2:** Evaluate the impact of a new store layout trialled in 
  3 stores using quasi-experimental analysis

## Key Findings

**Customer Segments**
- Budget Older Families are the highest spending segment at $157k total sales, driven by volume — they buy 9+ bags per customer per year
- Mainstream Young Singles/Couples represent the strongest growth opportunity, over-indexing on flavored brands (Tyrrells, Twisties, 
  Doritos) and preferring either large sharing packs or small single-serve sizes
- Normalizing by customer count shows spend per customer is actually similar across top segments ($32-$35), meaning volume of customers not spend per head — drives total revenue differences

**Store Trial**
- The new store layout drove statistically significant chip sales 
  uplift in 2 of 3 trial stores (77 and 88)
- Primary driver was increased customer traffic rather than existing 
  customers buying more
- Store 86 showed mixed results — significant in 1 of 3 trial months
- Recommendation: introduce the new layout to all stores

## Visualizations

### Total Chip Sales by Customer Segment
![Segment Sales](segment_sales.png)

### Brand Preference — Mainstream Young Singles/Couples
![Brand Affinity](brand_affinity.png)

### Store Trial Assessment with 95% Confidence Intervals
![Trial Assessment](trial_assessment.png)

## Methodology

**Task 1 — Customer Segment Analysis**
- Cleaned 264,836 transaction records — removed test accounts, 
  non-chip products, and standardized brand names
- Engineered pack size and brand features from product name strings
- Merged transaction data with customer segment data on loyalty 
  card number
- Analyzed total sales, customers per segment, average spend per 
  customer, units per customer, and brand/pack size preferences

**Task 2 — Store Trial Assessment**
- Built monthly metrics per store (sales, customers, transactions)
- Selected control stores using Pearson correlation on pre-trial 
  sales patterns, filtered by size similarity
- Scaled control store sales to trial store baseline to remove 
  pre-existing size differences
- Built 95% confidence intervals from pre-trial variance to test 
  statistical significance
- Analyzed drivers of sales changes (customer count vs transactions 
  per customer)

## Tools & Skills
- Python (pandas, numpy, matplotlib, seaborn, scipy)
- Data cleaning and outlier detection
- Feature engineering
- Customer segmentation analysis
- Quasi-experimental design (difference-in-differences)
- Statistical significance testing

## Data
Data provided by Quantium via Forage job simulation. Raw data files 
are not included in this repository. To run the notebooks, download 
the datasets from the Quantium Data Analytics simulation on Forage 
and place them in the same directory as the notebooks.

## Notebooks
- `Quantium_Task1_Customer_Segment_Analysis.ipynb` — EDA, cleaning, 
  feature engineering, and segment analysis
- `Quantium_Task2_Store_Trial_Assessment.ipynb` — Control store 
  selection and trial impact assessment
