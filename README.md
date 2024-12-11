# Customer-Segmentation

## Project Overview

The objective of this project is to segment a company's customer base in order to enhance targeted marketing strategies and gain deeper insights into customer buying behaviors. By analyzing customer, product, and order data, we aim to create a segmentation model that identifies distinct customer groups based on their purchasing patterns. This segmentation will help understand how different customer segments interact with the company's products and services.

The project employs **KMeans clustering** to segment customers and includes the creation of an **RFM (Recency, Frequency, Monetary)** table to analyze customer behavior. The RFM analysis categorizes customers based on:
- **Recency**: The time since the customer's last purchase.
- **Frequency**: How often the customer makes a purchase.
- **Monetary**: The total amount spent by the customer.

The resulting segmentation provides valuable insights into customer engagement and purchasing behavior, helping guide marketing decisions.

## Data Overview

The dataset used in this project contains customer, order, and product information. Below is a description of the columns available in the dataframe:

### Customer Information
- **Customers.id**: Unique identifier for each customer.
- **Customers.fname**: Customer's first name.
- **Customers.lname**: Customer's last name.
- **Customers.company**: Company associated with the customer.
- **Customers.create_date**: Timestamp when the customer account was created.
- **Customers.status**: Customer's account status (active, inactive).
- **Customers.mailing**: Mailing address (may be null).
- **Customers.reminders**: Any reminders set for the customer.
- **Customers.tax_exempt**: Tax-exemption status (may be null).
- **Customers.account_id**: Account identifier (may be null).
- **Customers.sales_rep**: Assigned sales representative.
- **Customers.rewards**: Customer's reward points.
- **Customers.last_modified**: Last modified timestamp.
- **Customers.customer_type**: Type of customer (e.g., individual, business).

### Order Information
- **Orders.id**: Unique identifier for each order.
- **Orders.customer_id**: Customer ID associated with the order.
- **Orders.order_number**: Order tracking number.
- **Orders.subtotal**: Subtotal amount before taxes and shipping.
- **Orders.total**: Total order amount after discounts and fees.
- **Orders.payment_status**: Status of the payment (e.g., pending, completed).
- **Orders.payment_date**: Date when the payment was made.

### Product Information
- **Products.seo_description**: SEO description for the product.
- **Products.unit**: Unit of measure for the product (e.g., EA).
- **Products.markup**: Markup price for the product.
- **Products.size**: Size of the product.
- **Products.material**: Material used in the product.

## RFM Analysis

The **RFM** analysis was conducted to segment customers based on their recent behavior, frequency of purchases, and monetary value spent. The **RFM Score** for each customer was calculated by combining the three metrics: Recency, Frequency, and Monetary. Based on the RFM score, customers were classified into different segments using the following criteria:

### RFM Score Segmentation
The customers were segmented into three distinct value groups based on their RFM scores using the following bins:

- **Low**: RFM scores between 0 and 8.
- **Mid**: RFM scores between 9 and 11.
- **High**: RFM scores between 12 and 14.

## Clustering Results

The **KMeans clustering** algorithm was used to segment customers based on the RFM scores. The silhouette score for the clustering model was **0.587**, indicating a moderate to strong separation between the clusters. This score suggests that the clustering model effectively distinguishes customer groups based on purchasing behavior.

## Conclusion

This customer segmentation model provides valuable insights into customer behavior. By focusing on high-value customers and implementing targeted marketing strategies for low-value customers, the company can improve customer engagement and increase revenue.

