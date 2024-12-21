# I Chose Not to Complete the Dashboard
Because uncovering the insights behind the problem was far more important than simply finishing it.

This is a Zomato project. You may have seen many people showcasing their own unique ways of presenting this visualization. Similarly, I decided to give it a try, BUT.....
The Observation: Total sales were 986M, but the breakdown of Veg (122M), Non-Veg (106M), and Other (24M) didn’t add up. This sparked a deep dive into the data.

![1](https://github.com/user-attachments/assets/dab7c3e4-9181-4c22-b031-2b055276369f)


# The Investigation
As an analyst or BI developer
This is where we really need to be able to jump in, figuring out what's missing by starting to think logically.

1. Identifying Missing Data: Created a measure "distinct food ID" and by this I uncovered a significant missing record impacting total sales and customer sales.

![3](https://github.com/user-attachments/assets/c7da575f-cc71-4a95-af17-acf97a5ef518)

2. Customer Sales Check: Total sales and customer sales should align, but they didn’t. (created that customer_sales measure just to compare this)

![6271666242855224121](https://github.com/user-attachments/assets/fae7b3e0-6266-49a5-8985-9802bb032244)

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
