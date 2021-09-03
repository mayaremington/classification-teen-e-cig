Abstract

The use of nicotine-containing electronic cigarettes remains popular among teenagers in the United States. This is despite the fact that nicotine, in addition to being highly addictive, is harmful to the adolescent brain.  I used the 2020 National Youth Tobacco Survey (NYTS, conducted annually by the CDC and FDA) for this project. This survey provides data about middle and high school students’ tobacco-related beliefs, exposure to pro- and anti-tobacco influences, and behaviors (including their use of electronic cigarettes and other tobacco products). I tried a number of  models, including KNN, logistic regression, Random Forest, and XGBoost  before deciding to use logistic regression with feature engineering (class weights, optimization of F2 scoring threshold). I also performed bootstrapping on my coefficients in order to obtain confidence intervals.

Design

The use of nicotine-containing electronic cigarettes remains popular among teenagers in the United States. This is despite the fact that nicotine, in addition to being highly addictive, is harmful to the adolescent brain. The goal of this project is 2-fold: 
- to determine which factors (demographics, use of other tobacco or vaping products, tobacco-related beliefs, and exposure to pro- and anti-tobacco influences) best explain the patterns in electronic cigarette use
- to build a model to predict whether or not a student has used e_cigs based on said features

Data

I used the 2020 National Youth Tobacco Survey (NYTS, conducted annually by the CDC and FDA) for this project. This survey provides data about middle and high school students’ tobacco-related beliefs, exposure to pro- and anti-tobacco influences, and behaviors (including their use of electronic cigarettes and other tobacco products). Survey data was downloaded from the cdc website: https://www.cdc.gov/tobacco/data_statistics/surveys/nyts/index.htm.

The dataset contains 14,000+ data points, each representing an anonymized middle or high school student who completed the survey. After cleaning, +13,000 data points remained.

The original dataset had 900+ columns, each representing a survey question or part of a survey question. After selecting a subset of columns and combining or splitted as needed, I ended up with a total of 25 feature columns. Many of the columns were binary (0,1) and some were ordinal but represented as discrete numerical (for example: 1, 2, 3, 4).

My target is whether or not a middle or high school student who completed the 2020 National Youth Tobacco Survey (NYTS) has ever used an electronic cigarette.  My data revealed that out of the 13,000+ students, 24.4% have used e-cigarettes. 

Algorithms

I tried a number of  models, including KNN, logistic regression, Random Forest, and XGBoost  before deciding to use logistic regression with feature engineering (class weights, optimization of F2 scoring threshold). I chose to pursue a logistic model given it's interpretability. I also performed bootstrapping on my coefficients in order to obtain confidence intervals.

Tools

- I built a classification model in python using pandas, numpy, and sklearn

Communication

Looking forward to the presentation!
