# Decodelabs_task_eda
## Overview

This project presents a comprehensive examination of an online retail transaction dataset containing customer orders, product information, payment details, and sales revenue records. The study combines business-oriented data exploration with predictive analytics to uncover purchasing patterns and estimate future transaction values.

The workflow covers data preparation, statistical exploration, visualization of business metrics, and the implementation of a regression-based prediction model.

## Project Goals

The purpose of this project is to:

- Investigate transactional sales data.
- Understand customer purchasing behavior.
- Examine revenue performance across products.
- Monitor order processing outcomes.
- Discover relationships among sales variables.
- Build a predictive model capable of estimating order value.

## Dataset Summary

The dataset contains 1,200 transaction records collected from an e-commerce environment.

### Variables Included

| Attribute | Explanation |
|------------|------------|
| OrderID | Unique identifier assigned to each order |
| Date | Purchase date |
| CustomerID | Customer reference number |
| Product | Item purchased |
| Quantity | Number of units ordered |
| UnitPrice | Price of a single unit |
| ShippingAddress | Delivery location |
| PaymentMethod | Method used for payment |
| OrderStatus | Current status of the order |
| TrackingNumber | Shipment tracking reference |
| ItemsInCart | Number of products added to cart |
| CouponCode | Promotional code used by customer |
| ReferralSource | Source through which customer reached the store |
| TotalPrice | Total amount paid for the order |

ta Preparation

Prior to analysis, several preprocessing tasks were performed:

- Dataset inspection and validation.
- Identification of missing values.
- Replacement of empty coupon records with a NoCoupon
- Generation of descriptive summaries.
- Preparation of variables for visualization and modeling.


## Exploratory Data Analysis

### Transaction Statistics

Numerical variables were examined to understand central tendencies and variability within the dataset.

#### Observations

- Average order quantity was close to three units.
- Typical transaction values exceeded one thousand dollars.
- Customers frequently added multiple products before checkout.
- Considerable variation exists among order values.

Key Data Insights & Interpretations

### 1. Data Summary (df.describe())
The average order value is $1,053.97, the average unit price is $356.41, and customers have about 5.48 items total in their shopping cart.
 Customers are spending a good amount of money per order. Also, since individual product quantities are usually small but the total cart size is bigger,
  it shows that customers like to buy a mix of different products together.

### 2. Order Status (Pie Chart)
 Cancelled orders 20.8% and returned orders 20.6 are almost equal. Together, they make up 41.4 of all transactions.
This is a big problem for the business. Losing more than 41% of your orders to cancellations and returns means you are losing a lot of money. 
The business needs to check why customers are unhappy or if there are delivery issues.

### 3. Product Revenue (Bar Chart)
Chairs, Printers, and Laptops bring in the highest revenue. Phones* bring in the lowest amount of money.
Main income comes from office furniture and computer equipment. 
Recommendation: Marketing should be done for Laptops and Chairs. 

### 4. Monthly Sales Trend (Line Chart)
 Sales go up and down sharply like a roller coaster between January 2023 and December 2023. Sales drop to $30,000 in slow months and jump to $65,000–$70,000 in peak months.
 The monthly income is not steady. This happens when a business relies too much on quick holiday sales or special coupon discounts. People only buy when there is a big promotion.

### 5. Quantity vs. Total Price (Scatter Plot)
Data points form straight vertical lines because customers buy in exact whole numbers (1, 2, 3, 4, or 5 items). Prices only reach the maximum of $3,500 when the quantity is 5.
 Selling more items at once is the best way to increase order value. 
 Recommendation: customers rewards or free shipping if they buy 4 or more items at the same time.
