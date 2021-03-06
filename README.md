# Employee Fatigue EDA & Prediction

## Table of Contents

- [Background](#Background)
  - [Data Cleaning](#cleaning)
- [Findings](#Findings)
  - [correlation](#corr)
- [Usage](#Usage)

<a name="Background"/>

## Background

This data is from Kaggle found [here](https://www.kaggle.com/blurredmachine/are-your-employees-burning-out). The goal of this project was to see if we can find what variables affect employee burnout. After determining what variables are meaningful we need to see if we can build a model to accurately predict employee burn rate.

### Data Cleaning

This dataset was from Kaggle so it was already organized, but I did have to:
1. Identify and Remove Nan values. There was a small amount 5%. So determined this was fine.
2. Using date of joining column to create Days Worked column so that it can be used in our analysis better. I calculated this by subtracting date of joining by the current date.

<a name="Findings"/>

## Findings

<a name="corr"/>

![corr](IMG/corr.png)

The correlation shows that burn rate has a strong correlation with all of the variables except for days worked. That was surprising to me because I expected number of days worked to be important.

![days_worked](IMG/days_worked.png)

Averaging the burn rate by the number of days worked showed no connection. One would expect if the more days someone worked then the graph would be high on the earlier dates and then reduce as the date got closer to the current date, but that wasn't what happened.

![designation](IMG/burn_rate_designation.png)
![wfh](IMG/wfh.png)

I also wanted to see how the categorical variables affected burn rates and only found that designation was obviously a factor that did affect burn rate aswell as also wfh slightly. The categorical variables that didn't seem to affect burn rate were gender and company.  

![importance](IMG/importance.png)

I used two models to predict burn rate which were Random Forest Regressor and Support Vector Regression. The chart above shows the importance of each variable in our Random Forest model. We can see that Mental Fatigue Score was the most important variable to determine burn rate. This makes alot of sense. Resource allocation followed which was how many hours each employee worked. So as we had determined before the variables that didn't help our models were Gender or Company.

The outcome was that our models scored:
Random Forest R_2score: .908
SVR: .890

<a name="Usage"/>

## Usage

Full jupyter notebook can be found [here](https://nbviewer.org/github/EdgarFonseca94/EmployeeFatigue/blob/main/Employee_Burnout.ipynb)
