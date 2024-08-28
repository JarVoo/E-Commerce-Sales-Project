## E-Commerce Performance Analysis: Online Pet Store

## Dashboard Link : 

![Home](https://github.com/user-attachments/assets/906ccf6a-2101-434e-be89-348b01fc017d)

## Introduction

In this case study, my goal is to create a Power BI dashboard which management can use to clearly observe its performance. Whiskique is a chain of online pet stores in the United States which prides itself on low costs in its operations. I am going to do a deep dive analysis on the company and look for paths to decrease costs and get an overall view of the company.

## Problem Statement


## The primary business goals include:

- Serve as many customers as possible and increase sales
- Reduce operating costs

It is important for Whiskique to know which products sell best and what type of costs might be associated with selling those products. With regard to sales, I will:

- Investigate which products sell in higher quantities and how much total sales they generate
- Which products have the highest shipping costs associated so that overall cost can be reduced.

In the analysis, I will also dive into market basket analysis to see which products cross-sell and upsell. 


## Data Collection and Understanding

![data dictionary e-commerce](https://github.com/user-attachments/assets/5b747d97-28a2-4b94-9af7-33a1324a287d)

The case study is made up of four CSV files, the Sales table is the primary transaction table, Product and Customer contain additional attributes and lastly State Mapping has consistent values for locations.

The CSV files were imported into Power BI where relationships were formed, and the data was cleaned. All transactions with empty invoice values were removed.
The Order State column contained different entries for the same states, so the State Mapping table was imported to clean this up.

I explored the data by creating measures:

1) Total customers
2) Customer LTV(avg) - total value of all sales by a customer

The LTV was visualized with State, showing that North Dakota had the highest average LTV ($1,278). 

![customer ltv by state](https://github.com/user-attachments/assets/27ed9c0d-ac41-40a3-848d-411c662a0c78)

Below are the States ranked highest to lowest by total number of customers.
California wins with the most customers.

![total customers by state](https://github.com/user-attachments/assets/384e148b-cb6d-4fac-a38a-486a1f4bddb4)

## Exploratory Data Analysis

Next I looked at products and shipping:

- Which products sell in higher quantities
- How much total sales did those products generate?

Shipping Cost 1000 mile is the average cost to ship a single quantity of a product by itself (without combining it with other products)

The food, disposables and grooming products made up the most sales with various brands of cat food and snacks selling the highest average quantity.

I can now see that Taste of the Wild dry dog food is the most expensive product to ship ($20 per individual shipment)

![products   shipping](https://github.com/user-attachments/assets/8ec4224d-5263-49e3-9a2e-1144a2122e47)

Many customers buy a single quantity of a product but combine it with other product types. Most often Whiskique ship multiple products in a single shipment as can be seen in the bottom plot with a quantity of 1 only having total sales of 5.98% of the grand total of sales. The rest were sold in quantities > 1. The company does a good job of selling multiple product types in a single invoice.

![Total Sales by Total Quantity](https://github.com/user-attachments/assets/b7a35ebf-5d70-4aec-b355-8309cf219abf)

I created a market basket tool in my dashboard that allows the user to select a product and see which other products were commonly ordered alongside the order.

As an example, when selecting the best-selling item, the Taste of the Wild dry dog food, the Memory Foam Pet Bed is the item most commonly ordered with it.

I have attached snapshots of my dashboard and a copy is uploaded into my repository.

![Executive Summary](https://github.com/user-attachments/assets/2371e412-5a10-47ba-b078-90aae45922d6)
![Shipping Metrics](https://github.com/user-attachments/assets/20120ed8-b6e5-4169-b149-a5b3e6bb9650)
![Market Basket Analysis](https://github.com/user-attachments/assets/465c27ca-a27b-4a61-b874-c61c50dac5c2)

I used a What-If analysis for management to dynamically adjust how many items are shipped and to see how much is spent on shipping and how much can be saved when shipping multiple items.

Shipping more than one item can help management save money, so I created a measure to calculate these savings. Below is the Blended Shipping Cost Factor, which was combined with a parameter in Power BI.

![cost multiplier](https://github.com/user-attachments/assets/9e2f76fa-3411-4e52-b360-4df56d2bef24)

Now management can use a slider to adjust the quantity and the cost of shipping is returned, and the amount saved. The default shipping quantity value is set to 5 items. 

The baseline shipping cost for shipping more than 1 item costs the company $385,150, so playing around with the quantity, a decent savings can be made the more is shipped.


## Insights


The Following inferences can be drawn from the dashboard;

### [1] Total Sales = $1.55 Million

Total Profit (Baseline) = $427,336 (27.5 %)

Top Profit Generating Product Categories = Electronics, Grooming, Cleaning Supplies

Top Sales by State = California

          
### [2] Shipping

Baseline Shipping Cost = $385,149 

If 5 items are purchased, Whiskique saves $59,095

Taste of the Wild dog food is the most expensive product to ship

California is the most expensive state for shipping costs


## Conclusions

When analyzing the LTV values, the higher the customer's lifetime value is, the more important the customer is to the company. The marketing team could help drive future customer campaigns to make this a priority.

This case study has been an amazing opportunity to dive into online e-commerce sales data and create useful tools to allow others to observe clear changes in money saving metrics in a simple dashboard. 

Management can incorporate interesting campaigns and experiments to shift customer behavior to buy certain products in one order, to save on shipping and to group product categories together that would benefit the customer.

In terms of reach, Whiskique still has many strides to make to reach more customers in more states. Right now, Califonia, New York, Florida and Texas take the lead in number of customers, but the company can advertise better in other states to increase sales.
