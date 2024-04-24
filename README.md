# US-MACs-Analysis

# Objective of our project
Our Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) focuses on the US McDonald's menu and its associated nutritional values. The dataset used is from https://www.kaggle.com/datasets/mcdonalds/nutrition-facts

# Problem and Problem Statement
According to the National Health and Nutrition Examination Survey, over 40% of adults and almost 20% of children in the United States are classified as obese. Additionally, obesity rates exceeding 35% are reported in 19 states, marking an increase from 16 states just last year. A decade ago, no states had obesity rates surpassing 35%. Obesity is associated with numerous health conditions, including diabetes, heart disease, stroke, and various cancers such as breast and colorectal cancer. Moreover, the annual medical expenses attributed to obesity reached nearly $173 billion in 2019 alone.
These alarming statistics pushed our team to undertake this project with the objective of leveraging Machine Learning to recommend healthier MacDonald’s food options for avid fast-food consumers, allowing them to make informed decisions when buying food. This is because many consumers unknowingly consume more calories and saturated fats than they require, thereby contributing to the prevalence of obesity and associated health complications. Thus with our recommendations, we hope to help consumers monitor their diets and reduce the risk of obesity-related diseases.
With the knowledge of the various tiers on each food and drink item, consumers would be educated on the nutritional value of each item. Consumers would be empowered to make well considered choices, pick items that would be better able to cater to their daily requirements and goals, ultimately combating obesity.

# About
A full breakdown and analysis of US Macdonald's menu and its nutritional data to recommend better food options to US consumers, amidst rising obesity rates.

# Contents in our Juptyer Notebook
Problem Statement and Background Information

Introduction to dataset

Data Cleaning and Manipulation

- Food Items with zero nutrient values
- Food Items with extremely high nutrient values
- Accuracy of calories given
- Conversion of imperial units to metric units

Data Visualisation
- Density of calories and macronutrients for each food item
- Range of nutrients across the menu
- Range of calories by food category
- Top 5 food items with the highest or lowest nutrient across the whole menu
- Serving Size Problem
- Multicollinearity of variables
  
Feature Engineering

Machine Learning
- Isolation Forest
- Multivariate Linear Regression
- Gradient Boosting Machine

# Contributors
@mcreaper26 - Data Extraction, Data Cleaning and Manipulation, Feature Engineering, Gradient Boosting Machine

@jolieetan - Data Visualisation, Multivariate Linear Regression

@jiaqie - Data Visualisation, Isolation Forest


# AI models used
scikit learn:
- Isolation Forest
- Multivariate Linear Regression

Gradient Boosting Machine:
- LightGBM

# Conclusion
There are 260 different food items of varying serving sizes in US Mcdonald's Menu.

## Food Items with zero nutrient values

- Apple Slices is a healthy snack/side as it has no fats and sodium even though it has no protein
- Chicken McNuggets, French Fries & Hash Brown have zero sugar (They tend to have high fats and are highly processed and also keep in mind that this is without any condiments)
- Side Salad has zero fats
