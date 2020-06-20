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

![Rossman_Stores_Sales_Forecasting](https://user-images.githubusercontent.com/19572673/80853482-58be2880-8bff-11ea-85ed-9776913c6255.PNG)

