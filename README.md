# I chose not to complete the dashboard
Because uncovering the insights behind the problem was far more important than simply finishing it.

This is a Zomato project. You may have seen many people showcasing their own unique ways of presenting this visualization. Similarly, I decided to give it a try, BUT.....
The Observation: Total sales were 986M, but the breakdown of Veg (122M), Non-Veg (106M), and Other (24M) didn’t add up. This sparked a deep dive into the data.

# The Investigation
As an analyst or BI developer
This is where we really need to be able to jump in, figuring out what's missing by starting to think logically.

1. Identifying Missing Data: Created a measure "distinct food ID" and by this I uncovered a significant missing record impacting total sales and customer sales.
![3](https://github.com/user-attachments/assets/b12b2f81-53a6-4ce4-9db5-8bc0943e9f77)

2. Customer Sales Check: Total sales and customer sales should align, but they didn’t. (created that customer_sales measure just to compare this)
![4](https://github.com/user-attachments/assets/65e21a03-14d6-4777-a2d5-509f0237495c)

3. City-Wise Analysis: Created a matrix for comparing sales across cities, customer sales, total orders, and sales quantities revealed more inconsistencies.
![5](https://github.com/user-attachments/assets/684bca8c-292b-4b12-8d07-42bbca89fb17)


# The Solution
1. I created a consolidated dataset (View Table) using PostgreSQL to clean and analyze the data, uncovering the missing links.
Although real-time updates weren’t possible, the cleaned dataset offered valuable insights into the discrepancies.
![6](https://github.com/user-attachments/assets/23c9e26e-ece1-4194-9bb5-947a92ecf279)

2. Using that view table, I calculated total sales, total Veg and Non-Veg sales, total orders, and total sales quantity to derive authentic insights.
![7](https://github.com/user-attachments/assets/e4fcfe29-9a1c-46d4-87b0-a36eeed00165)

This is where SQL truly proves to be a powerful tool for a Data Analyst.

# Key Takeaway
This analysis highlighted the importance of accurate data entry and relationships between tables.
Even small gaps can uncover big issues, reinforcing the need for thorough data checks.