# Super Market Sales Project


## Table of Contents
1. [Introduction](#introduction)
2. [Column Descriptions](#column-descriptions)
3. [Data Analysis](#data-analysis)
4. [Insights](#insights)
5. [Conclusion](#conclusion)

## Introduction
This dataset contains sales transaction data from a supermarket chain with branches in three major cities: Yangon, Naypyitaw, and Mandalay. The dataset includes information on customer demographics, purchase details, payment methods, and customer satisfaction ratings. Key aspects such as product lines, unit prices, quantities, and total purchase amounts (including tax) are also captured, providing a comprehensive view of sales and customer behavior.

## Column Descriptions

1. **Invoice ID**  
   A unique identifier for each transaction or purchase.

2. **Branch**  
   Indicates the branch location of the supermarket (e.g., Yangon, Naypyitaw, Mandalay).

3. **Yangon, Naypyitaw, Mandalay**  
   These columns may contain geographical or branch-specific data, though further inspection is needed to clarify their exact role.

4. **Customer type**  
   Describes the type of customer (e.g., Member or Normal).

5. **Gender**  
   Gender of the customer (Male or Female).

6. **Product line**  
   The category or type of product purchased (e.g., Health and beauty, Electronics).

7. **Unit price**  
   The price of a single unit of the product.

8. **Quantity**  
   The number of units purchased in the transaction.

9. **Tax 5%**  
   The tax amount applied to the total purchase (calculated as 5%).

10. **Total**  
    The total amount of the purchase, including tax.

11. **Date**  
    The date of the transaction.

12. **Time**  
    The time the transaction took place.

13. **Payment**  
    The payment method used (e.g., Cash, Credit card, E-wallet).

14. **Rating**  
    The customer satisfaction rating, typically on a scale from 1 to 10.
    

# Data Analysis

## Data Wrangling

1. **Loading the Dataset**  
   - The dataset was loaded into a pandas DataFrame for easy manipulation.

2. **Handling Missing Values**  
   - Checked for missing or null values in columns such as `Branch`, `Gender`, `Product line`, etc. If any missing data were found, they were either imputed (e.g., with mean values for numeric columns or mode for categorical columns) or removed.

3. **Correcting Data Types**  
   - Ensured that data types for each column were appropriate, such as converting `Date` and `Time` to `datetime` objects for easier manipulation and calculations.

4. **Removing Duplicates**  
   - Any duplicate records, if found, were removed to ensure each transaction was unique.

5. **Tax and Total Calculation Check**  
   - Verified that the `Tax 5%` column correctly reflected 5% of the purchase `Total` and fixed any discrepancies in these calculations if needed.

6. **Outlier Detection**  
   - Identified and handled potential outliers in columns like `Unit price`, `Quantity`, and `Rating` that could skew analysis results.

7. **Standardizing Categorical Data**  
   - Ensured consistency in categorical columns such as  `Customer type` by correcting any inconsistencies or misspellings.

8. **Datetime Feature Engineering**  
   - Extracted useful features from the `Date` and `Time` columns, such as day of the week or time of day, for deeper analysis of sales patterns.





## Insights

1. *% Customer Type*:
   - *Description*: This chart shows the distribution of customer types, comparing the percentage of normal customers versus members. It helps identify the proportion of different customer categories.

 <p align="center">
  <img src="IMG/customer_type.png" alt="% Customer by Type"/>
</p>

2. *% Customer by Gender*:
   - *Description*: This visual displays the percentage of customers by gender, highlighting the ratio of male to female customers. It provides insights into the gender demographics of the customer base.


<p align="center">
  <img src="IMG/customer_gender.png" alt="% Customer by Gender"/>
</p>


3. *% Customer by Shift Type*:
   - *Description*: This chart illustrates the preference of customers for different shift types (first or second shift). It shows which shift is more popular among customers for their purchases.


<p align="center">
  <img src="IMG/customer_shift.png" alt="% Customer by shift"/>
</p>


4. *Preferred Payment Methods for Customers*:
   - *Description*: This chart compares different payment methods and shows which method is preferred by customers. The stacked format reveals preferences segmented by customer type.


<p align="center">
  <img src="IMG/payment_method.png" alt="% Payment_Method"/>
</p>


5. *Distribution of Customer by Cities*:
   - *Description*: This visual breaks down the number of customers by city and customer type (normal or member). It helps understand customer distribution across various cities.


<p align="center">
  <img src="IMG/customer_by_city.png" alt=" Dist_by_Citites"/>
</p>


6. *Distribution of Product Line by Customers*:
   - *Description*: This tree map categorizes product lines and shows the number of invoices for each product line. It highlights which product lines are most popular based on customer purchases.


<p align="center">
  <img src="IMG/customer_by_city.png" alt=" Dist_by_Citites"/>
</p>


7. *Peak and Low Selling Hours by Product Line*:
   - *Description*: This table lists each product line along with its peak and low selling hours. It identifies the times of day when products are sold the most and least.


<p align="center">
  <img src="IMG/peak_selling_hours.png" alt="Peak_Hours"/>
</p>


8. *Rating for Products*:
   - *Description*: This chart displays the count of products based on their rating categories (Good, Fair, Excellent, Very Good). It provides an overview of product ratings and their distribution.


<p align="center">
  <img src="IMG/rating_of_products.png" alt="Rating_Of_Prouct"/>
</p>


9. *Distribution of Products by Quantity Sold*:
   - *Description*: This visual compares the total quantity sold for each product line. It shows which product lines have higher or lower sales volumes.


<p align="center">
  <img src="IMG/dist_product_by_qty.png" alt=" Dist_Product_By_QtySold"/>
</p>


10. *% Sales for Each City*:
    - *Description*: This chart represents the percentage of total sales generated by each city. It provides insights into the sales contribution of different cities.


<p align="center">
  <img src="IMG/sale_for_each_city.png" alt=" Sales_for_Each_City"/>
</p>


11. *Distribution of Sales by Product Line Across Shift Types*:
    - *Description*: This chart compares sales performance for different product lines across various shifts. It shows which product lines achieve higher sales during each shift type.


<p align="center">
  <img src="IMG/product_line_across_shift.png" alt="Dist_Product_Across_Shift_Type"/>
</p>


12. *Average Sales by Hour (10 AM - 9 PM)*:
    - *Description*: This line chart tracks average sales throughout the day from 10 AM to 9 PM. It provides a view of sales trends by hour.


<p align="center">
  <img src="IMG/avg_sales_by_hour.png" alt="Avg_Sales_Per_Hour"/>
</p>


13. *Average Sales Comparison: Weekends vs Weekdays*:
    - *Description*: This chart compares average sales on weekends versus weekdays. It helps assess the impact of day type on sales performance.


<p align="center">
  <img src="IMG/sales_comparison.png" alt=" WeekDay_VS_WeekEnd"/>
</p>


14. *Sales Trend Over 3 Months*:
    - *Description*: This line chart illustrates the sales trend over the past three months. It provides insights into how sales have fluctuated month by month.


<p align="center">
  <img src="IMG/total_sales_over_3_months.png" alt=" Sales_Over_3_Months"/>
</p>


15. *Sales Distribution by Days of Week*:
    - *Description*: This chart shows sales distribution across different days of the week. It helps identify which days generate higher or lower sales.


<p align="center">
  <img src="IMG/sales_dist_by_days_of_week.png" alt=" Sales_By_Day"/>
</p>

## Business Report 
Data Storytelling for Infinity Market
We approached this data analysis as if it belongs to a business we’ve recently launched three months ago, aiming to assess the sales and performance in this first quarter. The purpose of our analysis was to evaluate the current state of the business and devise strategic recommendations to improve our market performance.

*First, we named our market "Infinity Market" and designed a logo for it. Following our data analysis, we uncovered several key insights that will help us shape our business strategy:

1- *Low Customer Numbers:
As a newly opened market, the number of customers is still low, likely due to our limited brand awareness.
Recommendation:
We suggest launching an online market to expand our customer base and increase our reach, making it easier for people to discover and shop with us.

2- *Low Member Customer Ratio:
We found that the number of member customers is significantly lower than that of normal customers, and we aim to increase membership.
Recommendation:
Offer unique perks for members, such as special discounts, early access to sales, and member-only events to attract more customers to sign up for membership.

2- *Low Product Ratings for Specific Items:
We noticed that certain products have lower customer ratings, and we still have a significant stock of these items.
Recommendation:
We will offer discounts on these products to clear the stock and consider switching to a new vendor to ensure we offer higher quality products moving forward.

4- *Low Sales for Certain Product Lines:
Certain product lines are underperforming in terms of sales.
Recommendation:
We will strategically place the top-selling products at the end of the aisles so that customers pass through the less popular product lines on their way in and out, increasing their exposure and potentially boosting sales.

5- *High Sales on Saturdays:
Our data shows that Saturdays have the highest sales compared to other weekdays, as customers typically shop for their weekly needs during the weekend.
Recommendation:
Ensure all products are fully stocked and sufficient staff are available on weekends to meet the higher demand.

6- *Increased Sales During Holiday Seasons:
There are certain times of the month when sales spike due to holidays and special occasions.
Recommendation:
We will plan special promotions and ensure ample stock of products related to the holiday to capture this additional demand.

*Next Steps:
After implementing these strategies, we will reassess our sales and performance in three months to evaluate the effectiveness of our recommendations and determine whether our strategies have led to significant improvements in customer satisfaction and overall sales.

## Conclusion
The report highlights key insights into customer behavior and sales trends at Infinity Supermarket, with Naypyitaw being the top-performing city. Popular product categories include accessories, food, and beverages, and peak sales occur in the morning and evening. These findings offer strategic opportunities for improving customer satisfaction and boosting revenue.

