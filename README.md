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

### Q1. Calculate the average shipping delay (difference between 'Days for shipping (real)' and 'Days for shipment (scheduled)') for each product category.
![image](https://github.com/user-attachments/assets/158a8c46-bd5c-4e5b-94f0-2c3984e7c727)

The chart shows that "As Seen on TV" has the longest shipping delays, followed by Soccer, Crafts, and Pet Supplies. Music and Tennis & Racquet have the shortest delays. This suggests possible supply chain issues, high demand, or inventory problems in certain categories, impacting customer satisfaction and delivery efficiency.

### Q2. Use COUNTIF and other functions to analyze the distribution of customers across different cities and countries.

#### Top 20 Cities 
![image](https://github.com/user-attachments/assets/bc488043-fb71-470c-9daa-fcce95287dde)
The chart shows the distribution of customers across various cities, with Santo Domingo and New York City having the highest number of customers, followed by Tegucigalpa and Los Angeles. The customer base gradually decreases across other cities, with Houston, Chicago, and Sydney having the lowest numbers among the listed cities. This suggests that the business has a strong presence in certain metropolitan areas, while other cities may have lower engagement or market penetration

#### Top 20 Countries
![image](https://github.com/user-attachments/assets/a7838270-33d2-4b8c-b99a-35ea0668d920)
The chart displays the distribution of customers across different countries. The United States has the highest number of customers, followed by Mexico and France. Other countries such as Germany, Australia, Brazil, and the UK also have a significant number of customers. The customer count gradually decreases for countries like Indonesia, Spain, El Salvador, and the Dominican Republic, with Nigeria having the lowest number of customers among the listed countries. This suggests a strong market presence in North America and parts of Europe, with relatively lower engagement in some Asian and African countries.










  
     
   



