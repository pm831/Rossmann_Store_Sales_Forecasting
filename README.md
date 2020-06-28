# Rossman Stores Sales Forecasting
### Pujan Malavia

![rossman](https://user-images.githubusercontent.com/19572673/62430687-d2b39680-b6ed-11e9-83e0-ae936209d6fe.png)

### Link to Dataset:

https://www.kaggle.com/c/rossmann-store-sales/data

### Abstract:
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. 

### Industry:
Retail

### Company Information:
Dirk Rossmann GmbH is Germany's second-largest drug store chain (after dm-drogerie markt), with over 3,790 stores in Europe.
Rossmann was founded in 1972 by Dirk Rossmann.
The Rossmann family owns 60%, and the Hong Kong-based A.S. Watson Group 40% of the company. The company headquarters are in the German town of Burgwedel near Hanover.

https://en.wikipedia.org/wiki/Rossmann_(company)

https://www.aswatson.com/our-brands/health-beauty/rossmann/#.XUd5uuhKhGM

### Use Case:
Predicting their daily sales for up to six weeks in advance.

### Initial Dataset(s):
train.csv - historical data including Sales

test.csv - historical data excluding Sales

sample_submission.csv - a sample submission file in the correct format

store.csv - supplemental information about the stores

### Software:
Python (Jupyter Notebook), Tableau

### Techniques:

ARIMA Model

xgBoost

### Data:

You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

### Data fields

Most of the fields are self-explanatory. The following are descriptions for those that aren't.

Id - an Id that represents a (Store, Date) duple within the test set

Store - a unique Id for each store

Sales - the turnover for any given day (this is what you are predicting)

Customers - the number of customers on a given day

Open - an indicator for whether the store was open: 0 = closed, 1 = open

StateHoliday - indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. a = public holiday, b = Easter holiday, c = Christmas, 0 = None

SchoolHoliday - indicates if the (Store, Date) was affected by the closure of public schools

StoreType - differentiates between 4 different store models: a, b, c, d

Assortment - describes an assortment level: a = basic, b = extra, c = extended

CompetitionDistance - distance in meters to the nearest competitor store

CompetitionOpenSince[Month/Year] - gives the approximate year and month of the time the nearest competitor was opened

Promo - indicates whether a store is running a promo on that day

Promo2 - Promo2 is a continuing and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating

Promo2Since[Year/Week] - describes the year and calendar week when the store started participating in Promo2

PromoInterval - describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. ##### "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

### Quick Data Visualization

Tableau Visualization:
https://public.tableau.com/profile/pujan.malavia#!/

![Rossman_Stores_Sales_Forecasting](https://user-images.githubusercontent.com/19572673/80853482-58be2880-8bff-11ea-85ed-9776913c6255.PNG)

Python (Jupyter Notebook) Visualization:
https://github.com/pm831/Rossmann_Store_Sales_Forecasting/blob/master/Rossman%20Sales%20Forecasting.ipynb

Sales of Store 1 from 2013-01 to 2015-09

![output_20_1](https://user-images.githubusercontent.com/19572673/85776145-6a4b1a80-b6ee-11ea-961b-c55918784bdf.png)


![output_21_1](https://user-images.githubusercontent.com/19572673/85776146-6ae3b100-b6ee-11ea-9590-05fcb40f8841.png)


![output_21_2](https://user-images.githubusercontent.com/19572673/85776148-6ae3b100-b6ee-11ea-8e73-06cd43d81377.png)

Heatmap - Correlations between each Variable

![output_33_1](https://user-images.githubusercontent.com/19572673/85776149-6ae3b100-b6ee-11ea-943c-a610cdca4403.png)

Store 2, 85, 1, 13 Sales (Respectively) from Jan 2013 to July 2015

![output_39_1](https://user-images.githubusercontent.com/19572673/85776150-6b7c4780-b6ee-11ea-8065-71fc2ef72e21.png)

Store 2 Original, Rolling Mean, Rolling Std Time Series Plot

![output_41_0](https://user-images.githubusercontent.com/19572673/85776151-6b7c4780-b6ee-11ea-9d11-089b59a858a3.png)

Store 2 Trend, Seasonality, & Residuals Plot

![output_45_1](https://user-images.githubusercontent.com/19572673/85776153-6b7c4780-b6ee-11ea-9d0a-bd8d20d6a3f1.png)

Store 85 Trend, Seasonality, & Residuals Plot

![output_46_1](https://user-images.githubusercontent.com/19572673/85776154-6c14de00-b6ee-11ea-90c9-356f9dc41673.png)

Store 1 Trend, Seasonality, & Residuals Plot

![output_47_1](https://user-images.githubusercontent.com/19572673/85776156-6c14de00-b6ee-11ea-86a9-658f5cbe8db4.png)

Store 13 Trend, Seasonality, & Residuals Plot

![output_48_1](https://user-images.githubusercontent.com/19572673/85776157-6c14de00-b6ee-11ea-958a-d7b6f9208132.png)

Store 2 Autocorrelation Plot

![output_50_1](https://user-images.githubusercontent.com/19572673/85776159-6c14de00-b6ee-11ea-95bd-cfd496833929.png)

Store 85 Autocorrelation Plot

![output_51_1](https://user-images.githubusercontent.com/19572673/85776160-6cad7480-b6ee-11ea-8805-7ad43c2d6979.png)

Store 1 Autocorrelation Plot

![output_52_1](https://user-images.githubusercontent.com/19572673/85776161-6cad7480-b6ee-11ea-92cf-dffc1d141ac0.png)

Store 13 Autocorrelation Plot

![output_53_1](https://user-images.githubusercontent.com/19572673/85776163-6cad7480-b6ee-11ea-8a5d-85a63a3ded4e.png)

ARIMA Model (Observed vs. One-Step Ahead Forecast) - Store 2

![output_61_1](https://user-images.githubusercontent.com/19572673/85776164-6cad7480-b6ee-11ea-9bcb-aa3f0aa7e910.png)

ARIMA Model (Observed vs. One-Step Ahead Forecast) - Store 85

![output_62_1](https://user-images.githubusercontent.com/19572673/85776166-6d460b00-b6ee-11ea-9dd9-14be70c984d0.png)

ARIMA Model (Observed vs. One-Step Ahead Forecast) - Store 1

![output_63_0](https://user-images.githubusercontent.com/19572673/85776167-6d460b00-b6ee-11ea-8566-147042a1165d.png)

XGBoost Model

![output_75_1](https://user-images.githubusercontent.com/19572673/85776168-6d460b00-b6ee-11ea-909b-7e8e39e0c5a3.png)

### Communication of Results to Business Partner:
To a business partner, I would explain that the xgBoost (all else equal) is an efficient and easy to use algorithm which delivers high performance and accuracy as compared to other algorithms.

### Future Work:
Continue to do hyperparameter tuning of the model and creating new features/removing old features to help increase the prediction accuracy of the model

Try other types of models to see if the accuracy rate improves

More data visualization/patterns within the dataset (external sources) that can lead to more insights and decision-making from a business perspective
