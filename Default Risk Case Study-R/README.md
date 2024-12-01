# Project Title: Mortgage Default Analysis

## Description:
This project analyzes mortgage default trends using historical data from Fannie Mae. The objective is to explore key factors influencing defaults, such as borrower attributes, property types, and loan characteristics, and to provide actionable insights for lenders and policymakers.

## Key Features:
1. Visualization of default and non-default trends across property types.
2. Identification of significant factors influencing mortgage default.
3. Insights into foreclosure-related events, such as the initiation and finalization of the foreclosure process.

## Data Overview
The dataset used for this analysis contains mortgage-level data, with the following relevant columns:

1. PROP_TYP: Property type (e.g., Single-Family Home, Condominium).
2. default_status: Indicates whether the loan defaulted (1 = Default, 0 = No Default).
3. FCE_DTE: The date when the foreclosure process is triggered (foreclosure-related event occurs).
4. FCC_DTE: The date when the foreclosure process is finalized.
5. Other columns for loan characteristics, borrower attributes, and property details.

## Key Findings

1. Property Types & Default Trends:
Single-family homes are more stable across both default and non-default categories, while planned urban developments and manufactured homes show higher risk of default.

2. Default Indicators:
Foreclosure-related event date (FCE_DTE) is a more relevant indicator for identifying default events than the foreclosure completion date (FCC_DTE).

## Limitations
The analysis relies on historical data from Fannie Mae, which may not capture emerging market trends or shifts in borrower behavior in the post-COVID economy.
Some features in the dataset are highly correlated, which might influence the robustness of conclusions.

## Future Research
1. Incorporate post-COVID-19 data to analyze changes in mortgage default behavior and economic recovery trends.
2. Expand the analysis to include geographic factors, such as regional economic conditions or property market trends.
3. Investigate the impact of borrower assistance programs and their effectiveness in reducing defaults.