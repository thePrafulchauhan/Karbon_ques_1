# Karbon_ques_1
The SQL script provides the structure of the following tables:

users:

user_id: Primary key, integer.
username: Username of the user, varchar.
email: Email of the user, varchar.
registration_date: Date the user registered, date.

products:
product_id: Primary key, integer.
product_name: Name of the product, varchar.
category: Category of the product, varchar.
price: Price of the product, decimal.

orders:
order_id: Primary key, integer.
user_id: Foreign key referencing users(user_id), integer.
order_date: Date the order was placed, date.
total_amount: Total amount for the order, decimal.

order_items:
order_item_id: Primary key, integer.
order_id: Foreign key referencing orders(order_id), integer.
product_id: Foreign key referencing products(product_id), integer.
quantity: Quantity of the product in the order, integer.

Task A: Find the top 5 customers by total spend in the last 30 days.
To achieve this, we'll:
Filter orders from the last 30 days.
Calculate the total spend for each user.
Order by total spend in descending order.
Limit the results to the top 5 users.

Task B: Find the most purchased product to date.
To achieve this, we'll:
Aggregate the total quantity sold for each product.
Identify the product with the maximum quantity sold.
