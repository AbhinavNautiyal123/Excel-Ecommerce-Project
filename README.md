# Excel-Ecommerce-Project
📊 Ecommerce Supply Chain Analysis in Excel

## 📖 **Background**
DataCo Analysis Group is a leading business analytics consultancy. This project, "Streamline & Spotlight," focuses on how supply chain operations and digital consumer behaviour are connected.

We use two key datasets:
📦 Supply Chain Data – Includes sales, logistics, and delivery details.
🌍 Digital Access Logs – Tracks customer online interactions and preferences.

By analysing these datasets, businesses can improve their supply chains and better understand how customers engage with their products online.

## 🎯 **Objective**
This project uses Microsoft Excel to:

- ✅ Clean and merge data for better analysis.
- ✅ Find trends and patterns in supply chain and digital engagement.
- ✅ Create an interactive dashboard to visualise key insights.
- ✅ Suggest improvements for business growth and efficiency.

The goal is to help businesses make smarter decisions about product management, marketing, and customer relationships by connecting supply chain performance with digital behaviour.

## **Datasets**

### 1.  **Supply Chain Dataset:**
   This dataset contains detailed information on customer orders, sales performance, shipping details, and product data. The key fields can be grouped into different categories:
   
   - **Type** – The type of transaction (e.g., Cash,debit,payment,transfer).
   - **Order Id** – A unique identifier for each order.
   - **Order Date** – The date when the order was placed.
   - **Shipping Date** – The actual shipping date of the product.
   - **Delivery Status** – Status of the order (e.g., Advance, PENDING, CANCELED, Late).
   - **Shipping Mode** – The type of shipping service (e.g., Standard Class, First Class, Same Day).
   - **Customer Id** – A unique identifier for each customer.
   - **Customer Name (First & Last)** – The buyer’s name.
   - **Customer Segment** – Classification of customers (Consumer, Corporate, Home Office).
   - **Customer Location** (City, State, Country, Zipcode) – Identifies where customers are making purchases.
   - **Market & Order Region** – The geographical market or region where the order was delivered.
   - **Product Id & Name** – Unique code and name of the product.
   - **Category Name** – The category of the product (e.g., Electronics, Furniture).
   - **Product Price** – Price of the product before discounts.
   - **Sales** – The total revenue generated from the product.
   - **Order Item Discount & Discount Rate** – The discount applied to the product.
   - **Order Item Profit Ratio** – The profit margin for each product sold.
   - **Product Status** – Indicates whether a product is in stock (0: Available, 1: Not Available)
     
### 2.  **Access Logs Dataset**
   This dataset captures user interactions on the website, helping businesses understand consumer behaviour, product popularity, and website performance. The key fields are:
   
   - **Date & Time** – The exact timestamp when a user accessed the website.
   - **Month** – Helps in identifying seasonal trends.
   - **Hour** – Determines peak traffic hours on the website.
   - **Product** – Name of the product that was viewed.
   - **Category** – The product's category (e.g., Electronics, Fashion).
   - **Department** – The department to which the product belongs (e.g., Home Appliances, Clothing).
  
## **Merging and Handling Null Values**

### 1.  **Merging**
 he first dataset contains 70,004 rows, while the second dataset consists of 60,001 rows. To combine these two datasets, we use the Product Name column as the common key. However, due to their large size, Excel struggles to handle direct table merging efficiently. To overcome this limitation, we use the XLOOKUP function, which allows us to seamlessly retrieve matching data from one dataset to another without overwhelming Excel’s processing capabilities.

### 2. **Handling Null values:**
  The Order Zipcode column contains 60,371 null values, which accounts for over 86% of the total dataset. Additionally, the Product Description column is entirely empty, with 100% null values. Since these columns provide little to no useful information, they were removed during the merging process to streamline the dataset and improve efficiency.

## **EDA**

### **Q1. Calculate the average shipping delay (difference between 'Days for shipping (real)' and 'Days for shipment (scheduled)') for each product category.**
![image](https://github.com/user-attachments/assets/158a8c46-bd5c-4e5b-94f0-2c3984e7c727)

The chart shows that "As Seen on TV" has the longest shipping delays, followed by Soccer, Crafts, and Pet Supplies. Music and Tennis & Racquet have the shortest delays. This suggests possible supply chain issues, high demand, or inventory problems in certain categories, impacting customer satisfaction and delivery efficiency.

### **Q2. Use COUNTIF and other functions to analyze the distribution of customers across different cities and countries.**

#### Top 20 Cities 
![image](https://github.com/user-attachments/assets/bc488043-fb71-470c-9daa-fcce95287dde)
The chart shows the distribution of customers across various cities, with Santo Domingo and New York City having the highest number of customers, followed by Tegucigalpa and Los Angeles. The customer base gradually decreases across other cities, with Houston, Chicago, and Sydney having the lowest numbers among the listed cities. This suggests that the business has a strong presence in certain metropolitan areas, while other cities may have lower engagement or market penetration

#### Top 20 Countries
![image](https://github.com/user-attachments/assets/a7838270-33d2-4b8c-b99a-35ea0668d920)
The chart displays the distribution of customers across different countries. The United States has the highest number of customers, followed by Mexico and France. Other countries such as Germany, Australia, Brazil, and the UK also have a significant number of customers. The customer count gradually decreases for countries like Indonesia, Spain, El Salvador, and the Dominican Republic, with Nigeria having the lowest number of customers among the listed countries. This suggests a strong market presence in North America and parts of Europe, with relatively lower engagement in some Asian and African countries.


### **Q3 Analyze monthly sales trends over the years and identify peak sales months using date functions.**

![image](https://github.com/user-attachments/assets/1d4bb362-ec2a-4738-8fb2-0a01d59453b1)

- September 2017: Sales were relatively low at 662,852.70.
- October 2017: A sharp increase in sales to 3,869,093.94, indicating a strong positive trend.
- November 2017: Sales declined significantly to 1,252,248.04, suggesting a drop in demand or seasonal effects.
- December 2017: Sales remained almost stable with a slight increase to 1,326,580.81.
- January 2018: A significant spike in sales to 6,017,466.74, showing strong growth.
This pattern suggests a possible seasonal effect, with a peak in October, a dip in November and December, and a major rise in January. This could be due to year-end promotions, new product launches, or other market dynamics.

### **Q4 Identify the top 5 products with the highest sales.**

![image](https://github.com/user-attachments/assets/c33869ab-df61-4d92-8085-6a852ac161f0)

The Field & Stream Sportsman 16 Gun Fire Safe is a clear leader, while the other four products have relatively close sales figures. This insight could be useful for inventory planning, marketing strategies, or further analysis on what makes the top-selling product so successful.

### **Q5 Develop an index to rate product popularity based on sales volume and frequency.**

I have Calculated PPI(product Popularity index) using this formula 
PPI = (Total Sales of Product × 0.5)+(Total Orders of Product × 0.5)

![image](https://github.com/user-attachments/assets/131e8a76-1d87-48dc-9768-8c6e68bdf39b)
fitness, sports, and outdoor products are the most popular, while tech products like the Dell Laptop have significantly lower popularity in this dataset.

### **Q6 Assess customer loyalty by calculating the average number of orders per customer.**
![image](https://github.com/user-attachments/assets/8ed0add8-869f-4c8e-854f-42e1d1d5d4ac)

Mary's orders are extremely high compared to all other customers. This suggests that either Mary is a bulk buyer, a business client, or there is an issue with the data .
The rest of the customers have a much more balanced order distribution, with their orders ranging between 408 and 670.

### **Q7  Use a pivot table to analyze the breakdown of delivery status (e.g., on time, late) by market regions.**

![image](https://github.com/user-attachments/assets/5aa75867-ee7f-4a5a-b265-0502652e7707)

- LATAM (10,775) and Europe (10,724) have the highest late deliveries, suggesting possible logistics challenges in these regions.
- Africa has the lowest total orders (4,521) but still sees a high late delivery rate relative to its total.
- USCA (United States & Canada) has the fewest advance shipments (2,261) and one of the lowest on-time deliveries (1,852), indicating potential inefficiencies in North American operations.

### **Q8 Determine the peak hours of website traffic and which products are most viewed during these times.**

![image](https://github.com/user-attachments/assets/3058dcfb-65b7-4ebc-b9e7-86c775b1fdf4)

- The morning peak (7 AM) suggests high engagement early in the day—possibly users checking the site before work.
- The evening spike (5-7 PM) could indicate users returning after work or school.
- Low traffic between 12-3 PM suggests inactive hours, possibly due to lunch breaks or work commitments.

### **Q9  Use pivot tables to analyze which month is most popular in terms of sales**
![image](https://github.com/user-attachments/assets/bd6ed078-1189-4c84-a46b-10295e604a0c)

- April & July peaks might indicate seasonal promotions, product launches, or market trends.
- May & June drop suggests possible market downturns, off-seasons, or reduced demand.
- November rise could be linked to holiday or pre-festive season sales.

### **Q10 Calculate the average number of product views per IP address to assess user engagement.**
![image](https://github.com/user-attachments/assets/9d87772a-10b8-4fd8-a8da-86331e08ea90)

- The highest engagement comes from IP 85.135.134.214, surpassing 9,000 views.
Other top contributors include:
- 205.138.87.143 (~8,500 views)
- 102.48.80.37 (~8,000 views)
- 198.208.104.94 (~7,500 views)
Engagement gradually declines as we move down the list, with the lowest IP (221.60.70.14) generating around 4,500 views.
A few IP addresses show similar engagement levels, suggesting repeated access from the same sources.


### **Q11  Compare the monthly trends in product views from the Access Logs dataset with the monthly sales trends of those products in the Supply Chain dataset. Identify any lag or lead relationship between interest and sales**

![image](https://github.com/user-attachments/assets/f2dd50e3-9b73-4608-af2a-232ff171dfe6)

Observations :

In early months (January to August), product views and sales follow a synchronized trend, suggesting that purchases occur shortly after viewing.
However, from September onwards, product views decline first, followed by a delayed drop in sales (noticeable in October and November).
This suggests that sales lag behind views by approximately one month, meaning customers browse products before making a purchase decision.

Possible Reasons:

- Customer Decision Time: Buyers may take time to decide before completing a purchase, leading to a delay in sales.
- Marketing Impact: Promotional campaigns or seasonal offers may cause a temporary increase in views before sales pick up.
- Supply Chain Delays: Inventory shortages or logistical delays might prevent immediate purchases, causing a time gap.
- Seasonality Effect: Consumer behaviour may change due to external factors like festivals, discounts, or year-end budget constraints.

## **Dashboard**




























  
     
   



