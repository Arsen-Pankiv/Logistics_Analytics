# Logistics_Analytics

## Introduction 


## Project Background and Network Description

**DeliverEase Ltd**. is an online webshop specialising in the sale and delivery of home essentials. With growing customer demand, the company aims to ensure that its distribution network can meet shipping capacity requirements while reducing operational costs.
The current network includes:

**2 suppliers (S1, S2)**

**3 warehouses (W1–W3)**

**5 distribution centres (DC1–DC5)**

**50 customers (C1–C50)**

<div align="center">
  <img src="screenshots/image_1.png" alt="image_2" width="300" height="300" />
</div>

### Distribution network 

The company currently operates with two suppliers **(S1 and S2)**, three warehouses **(W1, W2, and W3)**,
five distribution centers **(DC1 to DC5)**, and **50 customers (C1 to C50)**. As shown above, products
are first shipped from **suppliers** to **warehouses**, then from **warehouses** to **distribution centers**, and
finally from **distribution centers** to **customers**. Some transportation routes are unavailable: **S2** cannot
ship to **W1**; **W1** cannot ship to **DC4** or **DC5**; **W2** cannot ship to **DC2**; and **W3** cannot ship to **DC1** or
**DC2**.
 Each distribution center is responsible for delivering to **ten** nearby customers. An image **below**  shows
the geographical locations of all customers.



<div align="center">
  <img src="screenshots/image_2.png" alt="image_2" width="300" height="300" />
</div>

### Product Information
The company has selected five products **(P1 to P5)** for analysis. The full dataset is available in the
file **“data.xlsx”**. Product weights can be found on the **“Product weights”** sheet.


### Shipping operations
Products are transported by barge from **suppliers** to **warehouses**, and then by train from **warehouses** to
**distribution centres**. Each transportation link has a limited **capacity**. To use a link, the company must
first pay a **fixed cost** upfront to reserve its capacity. Only after this reservation can products be shipped
along that link. The **“Shipping information”** sheet in the dataset provides details on the **capacity of
each link**, as well as the associated **fixed** and **variable costs**. Variable costs are charged **per kilogram** of
product, regardless of the product type. The total weight shipped on any link must not exceed its
capacity. Note that the shipping capacity and variable costs are based on **product weight**, rather than
the number of units of product.

### Last mile delivery

Last-mile delivery covers shipments from **distribution centre**s to **customers**. The company uses its own
**vehicle fleet** and estimates transport costs based on the **distance** between each distribution centre and
**customer location**. The sheet **“Last-mile-cost per product per kg”** provides unit costs (in euros per kg
per kilometre), which vary by product type. 
Note that the distribution costs are based on product
weight , rather than the number of units of product. Coordinates for all distribution centres and
customers are listed in **“Last mile coordinates”**, and distances were calculated using the Euclidean
formula (assumed in kilometre). Customer
demands for each product type are provided in the sheet **“Demands per product type”**, representing the
number of product units ordered by **each customer**. 


## Task Overview

The project involved formulating a mathematical optimisation model to **minimise total distribution costs** for DeliverEase Ltd.’s supply chain, incorporating route availability, capacity limits, flow balance, and demand satisfaction. The model, implemented in Python using **PuLP**, was solved to identify the **optimal shipment plan** and r**eport total costs** and **shipment weights** for each **link** between suppliers, warehouses, and distribution centres. Network flow **visualisations** were created to illustrate shipment magnitudes, and **two data-driven managerial recommendations** were developed to enhance cost efficiency and resilience to demand uncertainty.


## Mathematical Programming Formulation

<div align="center">
  <img src="screenshots/image_3.png" alt="image_3" width="500" height="600" />
</div>


<div align="center">
  <img src="screenshots/image_4.png" alt="image_4" width="500" height="600" />
</div>


<div align="center">
  <img src="screenshots/image_5.png" alt="image_5" width="500" height="600" />
</div>

<div align="center">
  <img src="screenshots/image_6.png" alt="image_6" width="500" height="600" />
</div>


## Supply Chain Optimization: A Pulp Implementation for Cost Minimization


## Network Flow Visualization: Mapping Optimal Supply Chain Pathways

## Strategic supply chain recommendations

### Recommendation (1) : Strategic Network Optimization with Route Expansion

### Recommendation (2): Strategic Relocation Proposal – Northeast Site (33×60)

## Limitations 

## Conclusion 

## How to Use

1. **Install dependencies**: pandas, matplotlib, numpy.
2. **Load datasets**: use pd.read_csv() and adjust the file path/directory as needed.

## Author  
Created by **Arsen Pankiv**  
- [LinkedIn](https://www.linkedin.com/in/arsen-pankiv-6082b4349/)  
- [GitHub](https://github.com/Arsen-Pankiv)

 