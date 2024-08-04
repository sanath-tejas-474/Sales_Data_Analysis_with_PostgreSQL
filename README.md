# Sales Data Analysis with PostgreSQL

This project involves analyzing a comprehensive sales dataset using PostgreSQL. The dataset contains detailed information about sales transactions, including product details, customer demographics, sales dates and times, and financial metrics. This analysis aims to extract valuable insights to inform business decisions.

## Project Overview

### Table Creation

We begin by creating the `sales` table, which is designed to store detailed sales data. The table includes the following columns:

- **invoice_id**: A unique identifier for each sale.
- **branch**: The branch where the sale occurred.
- **city**: The city in which the branch is located.
- **customer_type**: The type of customer (e.g., Member, Normal).
- **gender**: The gender of the customer.
- **product_line**: The category of the product sold.
- **unit_price**: The price per unit of the product.
- **quantity**: The number of units sold.
- **tax_pct**: The tax percentage applied to the sale.
- **total**: The total amount of the sale (including tax).
- **date**: The date of the sale.
- **time**: The time of the sale.
- **payment**: The payment method used (e.g., Cash, Credit Card).
- **cogs**: Cost of Goods Sold for the sale.
- **gross_margin_pct**: The gross margin percentage.
- **gross_income**: The gross income from the sale.
- **rating**: Customer rating of the sale experience.

### Data Enhancement

To enhance our analysis, we add three additional columns:

1. **time_of_day**: This column categorizes the sale time into Morning, Afternoon, or Evening.
2. **day_name**: This column captures the day of the week for each sale.
3. **month_name**: This column captures the month for each sale.

The `time_of_day` column is added using a `CASE` statement that categorizes times into three periods. The `day_name` and `month_name` columns are added by extracting the day and month names from the sale date.

### Analysis Queries

#### General Information
- **Unique Cities**: Count the number of unique cities in the dataset.
- **City-Branch Mapping**: List each branch and its corresponding city.

#### Product Analysis
- **Unique Product Lines**: Count the number of unique product lines.
- **Top Selling Product Line**: Identify the product line with the highest sales quantity.
- **Monthly Revenue**: Calculate total revenue for each month.
- **Top COGS Month**: Identify the month with the highest Cost of Goods Sold.
- **Top Revenue Product Line**: Determine which product line generates the most revenue.
- **Top Revenue City**: Identify the city that generates the most revenue.
- **Average VAT by Product Line**: Calculate the average VAT percentage for each product line.
- **Product Line Performance**: Classify product lines as "Good" or "Bad" based on average sales.
- **Branch Performance**: Identify branches that sold more than the average number of products.
- **Gender Preferences**: Determine the most common product lines for each gender.
- **Product Line Ratings**: Calculate the average rating for each product line.

#### Customer Analysis
- **Customer Types**: Count the number of unique customer types.
- **Common Customer Type**: Identify the most common customer type.
- **Top Buying Customer Type**: Determine which customer type buys the most.
- **Gender Distribution**: Analyze the gender distribution of customers.
- **Branch Gender Distribution**: Compare gender distribution across branches.
- **Ratings by Time of Day**: Identify the time of day when customers give the highest ratings.
- **Branch Time of Day Ratings**: Compare ratings by time of day for each branch.
- **Best Rating Day**: Determine which day of the week has the best average ratings.
- **Sales by Time of Day and Day**: Analyze sales volume by time of day and day of the week.

#### Sales Analysis
- **Revenue by Customer Type**: Identify which customer type generates the most revenue.
- **City Tax Percentage**: Determine which city has the highest average tax percentage.
- **Customer Type VAT**: Identify which customer type pays the most in VAT.

## Getting Started

### Prerequisites

Ensure you have PostgreSQL installed and properly set up on your machine.

### Setting Up the Database

1. **Create the Table**: Use the provided SQL script to create the `sales` table.
2. **Insert Data**: Populate the table with your sales data.
3. **Add Columns**: Run the ALTER TABLE and UPDATE statements to add and populate the `time_of_day`, `day_name`, and `month_name` columns.

### Running the Queries

Execute the provided SQL queries to perform various analyses on the sales data. These queries will help you understand sales trends, customer behaviors, and product performance.

## Analysis Insights

The analysis provided by these queries can help businesses:

- Identify top-performing products and categories.
- Understand customer demographics and preferences.
- Optimize inventory and stock based on sales trends.
- Improve marketing strategies by targeting the right customer segments.
- Enhance operational efficiency by analyzing branch performance.

## Contributing

Contributions are welcome! If you have suggestions for additional queries or improvements to the existing analysis, please fork the repository, create a new branch, and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
