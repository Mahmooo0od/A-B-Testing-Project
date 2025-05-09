# A/B Test Results Analysis

This project analyzes the results of an A/B test conducted on an e-commerce website. The goal is to understand user conversion patterns and provide actionable recommendations to the company regarding their webpage strategy.  Specifically, the analysis aims to determine whether a new webpage design increases customer purchases.

## Table of Contents

-   [Introduction](#intro)
-   [Part I - Probability](#probability)
-   [Part II - A/B Test](#ab_test)
-   [Part III - Regression](#regression)

## Project Description

###   Introduction <a id="intro"></a>

This project involves analyzing the results of an A/B test conducted on an e-commerce website to understand user conversion and provide actionable recommendations. The goal is to advise the company on whether to implement a new webpage designed to increase customer purchases, maintain the existing page, or extend the experiment.

###   Data <a id="data"></a>

The analysis is based on the `ab_data.csv` dataset, which contains information about 200K+ users involved in the A/B test. The dataset includes the following columns:

* `user_id`: Unique identifier for each user.
* `timestamp`: Date and time of each user's visit to the website.
* `group`:  The group each user was assigned to ('control' or 'treatment'). The `control` group was shown the old page, and the `treatment` group was shown the new page.
* `landing_page`: The page displayed to the user ('new\_page' or 'old\_page').
* `converted`:  Indicates whether the user made a purchase (1) or not (0).

###   Analysis <a id="analysis"></a>

The analysis is structured into three main parts:

* **Part I - Probability:**
    * Initial exploration of the dataset to understand its basic properties (size, number of unique users, time frame of the experiment, conversion rate, etc.).
    * Data cleaning to ensure the data is suitable for A/B testing. This involves removing inconsistent data where users are assigned to the wrong group or page.
    * Handling duplicate entries to avoid skewing results.
* **Part II - A/B Test:**
    * Statistical analysis to determine if there's a significant difference in conversion rates between the control and treatment groups.
    * Calculation of observed difference and p-values to assess the statistical significance of the A/B test results.
* **Part III - Regression:**
    * Using logistic regression to model the probability of conversion based on the page viewed (new or old).
    * Investigating the potential influence of other factors, such as country, on the conversion rate.

###   Recommendation <a id="recommendation"></a>

The analysis concludes with a recommendation to the company, based on the statistical evidence, on whether to launch the new page, keep the old page, or conduct further testing.

##   Dependencies

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Statsmodels

##   How to Run

1.  Clone the repository.
2.  Ensure you have the required libraries installed (`pip install pandas numpy matplotlib statsmodels`).
3.  Run the Jupyter Notebook `A_B_Testing_Project.ipynb`.
