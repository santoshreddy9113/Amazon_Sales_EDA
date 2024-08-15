# Amazon_Sales_EDA
The provided text appears to be a detailed explanation of a Python script for Exploratory Data Analysis (EDA) on an Amazon Sales dataset. Here's a breakdown of the key points:

## Dataset Information:

### Source:
Scraped from Amazon's official website.Contains data for over 1000 products with ratings and reviews

### Script Steps:
Import Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scipy

### Data Loading:
Reads the CSV file using pd.read_csv

### Data Exploration:

Checks for missing values with df.isnull().sum()

Analyzes column data types with df.info()

### Data Cleaning:

Drops unnecessary columns like about_product, user_id, etc.

### Data Type Conversion:

Converts discounted_price, actual_price to float by removing currency symbol (₹) and commas.

Converts discount_percentage to float by removing percentage symbol (%) and dividing by 100.

Attempts to fix an anomaly in the rating column (row 458) by replacing the strange character with a value (commented out).

Considers converting rating_count to float (commented out).

## Overall, the script seems to be a well-structured approach to cleaning and preparing the Amazon Sales dataset for further analysis

## Summary of Data VIsualization

This EDA provides valuable insights into product categories, prices, ratings, and sales patterns within the Amazon sales data. Key findings include:

### Product Categories:

Electronics dominates the product mix, followed by Home & Kitchen and Computers & Accessories.

Other categories present potential for expansion or product diversification based on lower product counts.

### Rating Distribution:

Ratings are skewed towards higher values (around 4.25), indicating generally positive customer sentiment.

A smaller tail towards lower ratings suggests areas for improvement.

### Product Discounts:

Top discounted products are identified, providing insights for promotional strategies and pricing optimization.

### Correlations:

Strong positive correlation between discounted_price and actual_price indicates a linear relationship.

Weak positive correlation between rating and rating_count suggests a slight tendency for higher-rated products to have more reviews.

### Grouping and Aggregation:

Mean and median rating are calculated by category and sub-category, revealing potential variations in customer satisfaction across different product segments.

### Statistical Tests:

Chi-square test revealed no statistically significant association between actual price and product rating.

### Data Transformation:

Label encoding was used on categorical variables for heatmap visualization but reversed before further analysis.

*Optimizing product offerings based on category popularity and customer preferences.

*Developing targeted marketing campaigns based on product discounts and customer sentiment.

*Identifying areas for product improvement based on lower ratings.

### Some of the important aspects of EDA opererations:

1. What is the average rating for each product category

2. Top rating_count products by category

3.  Average discount percentage across categories

4.  The most popular product name

5.  The most popular product keyword

6.  Top 5 sub_categories based with highest ratings

7.  Sub-categories have the lowest average rating

8.  Sub-category offers the best value for money (rating per unit of price)

9.  Category has the highest total sales value (discounted price * rating_count)

10.  Sub-category has the highest average rating
