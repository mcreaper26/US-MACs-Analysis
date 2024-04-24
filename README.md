# US Macdonald's nutritional analysis

# Problem and Problem Statement
According to the National Health and Nutrition Examination Survey, over 40% of adults and almost 20% of children in the United States are classified as obese. Additionally, obesity rates exceeding 35% are reported in 19 states, marking an increase from 16 states just last year. A decade ago, no states had obesity rates surpassing 35%. Obesity is associated with numerous health conditions, including diabetes, heart disease, stroke, and various cancers such as breast and colorectal cancer. Moreover, the annual medical expenses attributed to obesity reached nearly $173 billion in 2019 alone.
These alarming statistics pushed our team to undertake this project with the objective of leveraging Machine Learning to recommend healthier MacDonald’s food options for avid fast-food consumers, allowing them to make informed decisions when buying food. This is because many consumers unknowingly consume more calories and saturated fats than they require, thereby contributing to the prevalence of obesity and associated health complications. Thus with our recommendations, we hope to help consumers monitor their diets and reduce the risk of obesity-related diseases.
With the knowledge of the various tiers on each food and drink item, consumers would be educated on the nutritional value of each item. Consumers would be empowered to make well considered choices, pick items that would be better able to cater to their daily requirements and goals, ultimately combating obesity.

# Objective of our project
Our Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) focuses on the US McDonald's menu and its associated nutritional values. It includes a full breakdown and analysis of US Macdonald's menu and its nutritional data to recommend better food options to US consumers, amidst rising obesity rates. The dataset used is from https://www.kaggle.com/datasets/mcdonalds/nutrition-facts. 

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

## Food Items with extremely high nutrient values
121 food items out of 260 hit the daily value of certain nutrients required (not advisable to hit 100% in one meal), which is roughly half of the menu.

## Accuracy of calories given
There is some discrepancy between the calories given and calculated calories. Discrepancies were observed, attributable to factors such as fibre content, sugar alcohols, and rounding rules, emphasising the need for precise nutritional information. 

## Calorie Density Finder
Desserts have the highest calorie density, followed by Breakfast and then Beef & Pork. Desserts have a high variance, followed by Breakfast and then Beef & Pork. This means, in general, when a customer chooses Beef & Pork, there is a high chance that the food item contains lots of calories but should a customer choose Desserts, there is small chance that the food item has even more calories than the Beef & Pork option.

## Range of each nutrient across the whole menu
As we can tell from above, many of the items on the menu contain high amounts of Sugars, Saturated Fats and proteins as the median values for these categories are relatively high, nearing 25% and above for a single food or drink item. The upper fence for Sugars and Saturated Fats exceeds 100% of the daily recommended value as well. Given that many Mcdonald's goers often order a set meal, it is highly likely for consumers to exceed their daily recommended intake for various nutrients in one sitting which may lead to several adverse effects on health on top of contributing to obesity.

## Serving Size
Thus, from the various graphs presented above we can confirm that generally, it's evident that there's a positive linear relationship between Calories and Serving Sizes across all categories, as indicated by the positive gradients of the linear regression lines. This suggests that larger serving sizes are associated with higher calorie counts. However, for certain food categories such as Breakfast, Beef and Pork and Chicken and Fish, the steeper gradients reveal a disproportionate increase in calories relative to serving size, because the increase in calories is higher than expected based on the increase in serving size. This implies that upsizing may lead to a significant rise in calorie intake, particularly for these categories. Thus, consumers should exercise caution and consider avoiding upsizing for certain food categories to manage their calorie consumption effectively.

## Multicollinearity 
we can tell that Saturated fats, proteins and carbohydrates have the highest correlation of 0.85, 0.79 and 0.78 respectively. This is consistent with the facts previously established as fats, proteins and carbohydrates are the biggest contributors to amount of calories present since each gram contains their respective amounts of calories. Thus, they have strong linear relationships with caloric content in the food and drink items.

## Feature Engineering
From the composite score, it can be deduced:
Frappe Chocolate Chip (Large) is the least healthiest food in the entire menu.
Premium Southwest Salad with Grilled Chicken is the most healthiest food in the entire menu.
Using water as the baseline, since it has no nutrients with zero calories, it sets a composite score of 6.76, which is pretty accurate as it is a healthy choice of beverage that can be consumed in large amounts.

## Isolation Forest
Number of anomalous values: 34
Number of non-anomalous values: 226
Total Number of Values: 260

## Multivariate Linear Regression
Looking at the coefficients of the predictors of the linear regression model.

We can tell that Trans Fats has the largest effect on the weighted composite score followed by Sodium then Dietary Fibre and Protein accordingly due to the relatively large magnitudes of the coefficients of these predictors as seen from the linear regression model.

The predicted coefficients for the factor of Trans Fat and Protein is consistent with weights allocated while Sodium and Dietary Fibre is predicted to be slightly higher than allocated.

## Gradient Boosting Machine

It helps to predict weighted composite score
Premium Southwest Salad with Grilled chicken was the healthiest food item in the whole menu.
However, the predicted unhealthiest food item is different from actual one.
LightGBM predicted the composite score based on a different scale of varying importance for the 12 predictor variables, in comparison to the weights that was assigned when feature engineering the weighted composite score earlier on.
It can be deduced that the LightGBM model's predicted composite scoring system is much more competitive and harsher, by comparing the number of unique values of the predicted weighted score against the number of unique values of the actual weighted score. This ensures there is more variability in weighted composite score

## What did we learn?
- Multicollinearity
- Plotly
- LightGBM


# References

https://www.mdanderson.org/publications/focused-on-health/what-are-macronutrients-.h15-1593780.html#:~:text=Carbohydrates%2C%20fat%20and%20protein%20are,Anderson%20Wellness%20Dietitian%20Lindsey%20Wohlford.

https://www.hsph.harvard.edu/nutritionsource/carbohydrates/#:~:text=The%20most%20common%20and%20abundant,bodily%20functions%20and%20physical%20activity.

https://www.healthhub.sg/live-healthy/why_protein_is_important#:~:text=Myth%20%232%20Protein%20is%20more%20important%20than%20carbs&text=Friends%20might%20even%20urge%20us,key%20function%20in%20our%20body.

For Data cleaning & manipulation:
For Artificial Sweeteners:
Sugar Substitutes: What You Should Know (massgeneral.org)
Artificial sugars may raise blood sugar - Harvard Health
For coffee’s half-life:
Pharmacology of Caffeine - Caffeine for the Sustainment of Mental Task Performance - NCBI Bookshelf (nih.gov)
For daily amount of sugar for men and women:
How much sugar is too much? | American Heart Association



In problem statement - Fryar, C. D., Carroll, M. D., & Afful, J. (2021, February 8). Products - health e stats - prevalence of overweight, obesity, and extreme obesity among adults aged 20 and over: United States, 1960–1962 through 2017–2018. Centers for Disease Control and Prevention.) https://www.cdc.gov/nchs/data/hestat/obesity-adult-17-18/obesity-adult.htm
Visualisation showcase to support prob statement, bar charts - Washington State Department of Social and Health Services (.gov). (n.d.). Reading food nutrition labels. Washington State Department of Social and Health Services (.gov). https://www.dshs.wa.gov/sites/default/files/ALTSA/stakeholders/documents/duals/toolkit/Reading%20Food%20Nutrition%20Labels.pdf
Problems with portion sizes - Lamour, J. (2023, September 12). McDonald’s is phasing out self-serve soda stations - here’s why. TODAY.com. https://www.today.com/food/restaurants/mcdonalds-phasing-out-self-serve-beverage-stations-rcna104432 https://www.today.com/food/restaurants/mcdonalds-phasing-out-self-serve-beverage-stations-rcna104432
Problems with portion size - Ponthieux, T. (2022, August 31). US vs Japan McDonald’s. Sugoi Mart by Japan Crate. https://sugoimart.com/blogs/sugoi-mart-blog/us-vs-japan-mcdonalds
Problems with portion size - Nutrition list: Menu: Scale for good: マクドナルド公式. McDonalds Japan. ( Idk how cite )  https://www.mcdonalds.co.jp/en/quality/allergy_Nutrition/nutrient/
Problems with portion size - National Institute of Health and Nutrition. (n.d.). Body weight status of Japanese. NIBIOHN. https://www.nibiohn.go.jp/eiken/kenkounippon21/download_files/other/document_en_02.pdf

