# Genpact Machine Learning Hackathon

[competition link](https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon/)

## Problem Statement

Your client is a meal delivery company which operates in multiple cities. They have various fulfillment centers in these cities for dispatching meal orders to their customers. The client wants you to help these centers with demand forecasting for upcoming weeks so that these centers will plan the stock of raw materials accordingly.

The replenishment of majority of raw materials is done on weekly basis and since the raw material is perishable, the procurement planning is of utmost importance. Secondly, staffing of the centers is also one area wherein accurate demand forecasts are really helpful. Given the following information, the task is to predict the demand for the next 10 weeks (Weeks: 146-155) for the center-meal combinations in the test set:

- Historical data of demand for a product-center combination (Weeks: 1 to 145)
- Product(Meal) features such as category, sub-category, current price and discount
- Information for fulfillment center like center area, city information etc.

## Data Dictionary

1. __Weekly Demand data (train.csv)__: Contains the historical demand data for all centers, test.csv contains all the following features except the target variable.

| Variable | Definition |
| -------- | ---------- |
| id | Unique ID |
| week | Week No |
| center_id | Unique ID for fulfillment center |
| meal_id | Unique ID for Meal |
| checkout_price | Final price including discount, taxes & delivery charges | 
| base_price | Base price of the meal |
| emailer_for_promotion | Emailer sent for promotion of meal |
| homepage_featured	Meal | featured at homepage |
| num_orders | (Target) Orders Count |

2. __fulfilment_center_info.csv__: Contains information for each fulfilment center

| Variable | Definition |
| -------- | ---------- |
| center_id | Unique ID for fulfillment center |
| city_code | Unique code for city | 
| region_code | Unique code for region |
| center_type |	Anonymized center type |
| op_area |	Area of operation (in km^2) |

3. __meal_info.csv__: Contains information for each meal being served


| Variable | Definition |
| meal_id | Unique ID for the meal |
| category | Type of meal (beverages/snacks/soups….) |
| cuisine | Meal cuisine (Indian/Italian/…) |

## Evaluation Metric

The evaluation metric for this competition is __100*RMSLE__ where RMSLE is Root of Mean Squared Logarithmic Error across all entries in the test set.

Test data is further randomly divided into Public (30%) and Private (70%) data.

