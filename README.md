# Employee Fatigue EDA & Prediction

## Table of Contents

- [Background](#Background)
  - [Data Cleaning](#cleaning)
- [Findings](#Findings)
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

<a name="Usage"/>

## Usage
