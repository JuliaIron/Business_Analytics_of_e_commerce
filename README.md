# Olist: business analysis 

#### Contributors: Ayse, Darinka, Julia

## Table of contents

1. [Introduction](#introduction)
2. [Business Problem Statement](#BusinessProblemStatement)
3. [Tools](#tools)
4. [Workflow](#workflow)
5. [Insights](#insights)
6. [Repository contents](#repositoryContents) 

## Introduction <a class="anchor" id="Introduction"></a>

This is a data analytics project focusing on business intelligence (BI). We set out to create a BI dashboard for Olist,the largest department store in the Brazilian marketplace. The dataset used is Olist public dataset of around 100,000 orders made between 2016 and 2018. The dataset structure can be seen below.

<div>
<img src="https://i.imgur.com/HRhd2Y0.png" width="800"/>
</div>

#### Data Source:
https://www.kaggle.com/olistbr/brazilian-ecommerce
(2018), Olist Store

#### About Olist

Founded: 2015

Company type: e-commerce

Olist, "marketplace of marketplaces", is an e-commerce company founded in February 2015. Its model is particularly attractive to micro and small merchants, usually reliant on physical stores, which face obstacles in integrating into the larger (virtual) market. With Olist, they can register their products on its platform and don't have to worry about advertising or driving sales. Once their product is sold on Olist, the sellers are in charge of packing and placing the order at the post office for delivery. On the other hand, Olist charges merchants an annual subscription, plus a commission fee on the final price of the order. Olist does not offer inventory nor product shipping. 

## Business problem statement <a class="anchor" id="BusinessProblemStatement"></a>

In an imagined scenario, we hypothesized that Olist had completely changed its top management and would like to get the latest update on their performance. This includes:

* definition of KPIs and providing with general insights
* the most recent overview of business performance 
* advice and longterm business strategy to increase profits and sustain good customer satisfaction levels
* deliver further information that would help Olist become a leader in the e-commerce market

## Tools <a class="anchor" id="tools"></a>

* Python 
* SQL
* Tableau

* Libraries used (pandas, sqlalchemy...)

## Workflow<a class="anchor" id="workflow"></a>

We began with **gathering data**. In our case, we were provided with an SQL file which combined both Olist sales and marketing information. This allowed us to visually explore data in more detail and do further database querying. We also connected different tables in an ER, or entity-relationship diagram (see below). 

<div>
<img src="https://github.com/plumeris/Mid-bootcamp-project/blob/main/ER.png?raw=true" width="800"/>
</div>

For the **data cleaning** part, we further explored SQL tables in Python. Using Pandas, we examined the dataset for missing or skewed values. Since the dataset was very large we singled out the following tables:

- Customer
- Orders
- Products
- Sellers
- Order_Payments
- Order_Items
- Geolocation
- Orders_customer_items_paid

For each of these individual dataframes we:

- replaced null values with average or median for numerical columns
- dropped null values for datetime values
- dropped duplicates in geographical data
- translated the product category table into English and merged it with the products dataframe
- exported cleaned tables into CSV files

Then followed trial exploratory data analysis, or **EDA and defining KPIs**. Among other, we were interested in sales revenue and growth, customer and seller performance by location, average delivery times, etc. As we explored our data, we accordingly iterated over the indicators (see final dashboard).  

The **data visualization** followed in **Tableau**, where we created a final BI dashboard.

## Insights<a class="anchor" id="insights"></a>

#### Sales

Looking at the sales development we noticed that revenues peaked during usual e-commerce dates like Black Friday, Christmas, or Valentines Day (June 12th in Brazil). Sales and orders tend to develop at an identical pace. In general, more growth is expected for Olist in the future.

#### Orders

The distribution of top-selling product categories remains similar across different regions. Southeast Brazil stands out as the largest market which is no surprise considering that it is the cultural and economic hub of the country with the largest cities: São Paulo, Rio de Janeiro, and Belo Horizonte. 

Interestingly, the vast majority of all orders (over 80%) contains only 1 item. The highest selling product categories are 
bed_bath_table, health_beauty, watches_gifts.

#### Sellers

Comparing the ratio of sellers to the amount of orders, we noticed that some product categories perform extremely well and have a higher demand that could be developed further, either by involving more similar merchants or expanding the product palette. One example is the bed-bath-table product category which also stands out with the longest delivery delays, presumably because it is difficult for small shopkeepers to meet the market demand. 

The top sellers (20,000 orders) are all located in the affluent Southeast region, but interestingly one top seller is located in the north with around 400 orders. There is definitely an opportunity to jumpstart this market.


#### Delivery times

An important factor causing delivery delays is the seller location. The shops in the north, for example, are slower to process their orders within the average shipping time. Similarly, even though there are more merchants in the southeast, the customers there are also experiencing short delays, possibly because of population density and fast demand. Luckily for Olist, customers are overall satisfied with its service. The average rating is 4 on a scale 1-5.


#### Conclusion and recommendations

Without doubt, Olist is a fast growing e-commerce company that has the potential to become a giant in the Brazilian market. Its main strength lies with the small shopkeepers which previously have not benefited from the world of online sales. We suggest Olist should:

- involve even more small businesses and integrate them into the growing market
- improve delivery times by for example investing in strategically positioned logistics hubs or otherwise improve delivery and pick-up systems
- establish shorter routes and accomodate a larger number of local producers
- encourage customers to buy more items at once
- improve  internal data collection (e.g. cross-sharing data with delivery partners)
- improve database management (confusing product categorising, no existing product inventory)


## Repository contents<a class="anchor" id="repositoryContents"></a>


* Cleaned dataset
* Jupyter notebook
* SQL: EER model
* Tableau dashboard
