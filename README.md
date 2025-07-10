# DSA_Capstone_Project__2

## Amazon Product Review Analysis

- Company Overview

----------

You are working as a Junior Data Analyst at RetailTech Insights, **a company that provides e-commerce analytics solutions to sellers on platforms like Amazon.** Your team has been
tasked with analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

- Dataset Description

The dataset contains information scraped from Amazon product pages, including:

  - Product details: name, category, price, discount, and ratings

 Customer engagement: user reviews, titles, and content
 
 Each row represents a unique product, with aggregated reviewer data stored as comma-separated values

Total Records: 1,465 rows TotalFields: 16 columns


 - Analysis Tasks
--------------
Use pivot tables and calculated columns where necessary to answer the following:
1. What is the average discount percentage by product category?
2. How many products are listed under each category?
3. What is the total number of reviews per category?
4. Which products have the highest average ratings?
5. What is the average actual price vs the discounted price by category?
6. Which products have the highest number of reviews?
7. How many products have a discount of 50% or more?
8. What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
9. What is the total potential revenue (actual_price × rating_count) by category?
10. What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
----------------
## Steps:
- First I have to clean the data to remove possile duplicates.
- To achieve the above I applied **Ctrl + A** to highligjht all the data
- Click on **Data Tab** to locate **Remove Duplicate** tool that is "Data Tool" group.
- Click to **Unselect All** first, then only select **product_id**
- Click ok
- Now that you have your Unique/Distinct Products, NEXT is **Category**
**Note that** at this point I choose to split the Category Column details for easy refrence. This is because the Category column is **a multi-level Category.** To achieve this;
- Copy and Paste the Category Column on a **new worksheet**
- Click any of the details and go into the formula bar. Highlight it and copy it.
- Then, highlight your **column A** where you now have your category details, and click **Text to Columns**.
- click Next
- Paste the copied delimiter into this Other space
- Then click on **Finish**
- At this point the category column is now spread across **5 columns**
- On the main dataset, Highlight columns **D to G**
- Then right-click on the highlight columns to Insert
- Confirm that all columns values are reliable.
- Use filter tool to validate eah column values
- Removed all Blanks
- Insert a new column beside Column L and name it as Total Potential Revenue which is euual to **actual_price** multiplied by **rating_count**
- Insert a new conditional column beside Column  beside **discount_percentage** which is calculated as **=IF(J2>=50%,"50% or More","<50%")*=IF(J2>=50%,"50% or More","<50%")**
- Insert a new column beside Discouunted_Price which is calculated as **=IF(H2<200,"<₹200",IF(OR(H2=200,H2<=500),"₹200 - ₹500",">₹500"))**
- Note that at this point the dataset is ready for summarization

### DATA VISUALIZATION
---------
### Below is pictorial presentation of PIVOT TABLE AND CHARTS showing the following results;

(1) Average Discount Perentage By Category

(2) Count of Produts Per Category

(3) Total number of Reviews per Category

(4) Products with Highest Rating

(5) Average Actual Price By Discounted Price Per Category

(6) Products with Highest Reviews

(7) Products with 50% or more Discount

(8) Distribution of Products Rating

(9) Total Potential Revenue By Category

(10) Number of unique Products per Price Range Bucket etc









![Pivot_Table_1](https://github.com/user-attachments/assets/ebfab2e2-710c-46d0-9753-618332c28382)









