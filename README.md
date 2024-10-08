# SQL_Database_Creation_and_Analysis
A sql project consisting of creating a database schema according to the needs of a hypothetical small business that sells Pizzas! 

## Task
Create a database schema for a small pizza buisness based on the following requirements
1. The business is only doing take-out and delivery (no dine-ins)
2. main areas of focus are: Orders, Stock Control, and Staff.

### Orders
Required Data:
1. Item name
2. Item price
3. Quantity
4. Customer name
5. Delivery address

As an analyst I know that the Orders Table needs to have a primary key that is not null and not duplicated, therefore we need to create an 'Order ID' field
that handles grouping multiple items under one order and we need to create a 'Row ID' field that will be the unique identifier for each row. we also could add in when the order was placed and splitting some of these fields into:

### New Orders Tables
1. Row ID
2. Order ID
3. Order_Time
4. Item Name
5. Item Price
6. Quantity
7. Customer First Name
8. Customer Last Name
9. Delivery Address (1) 'street name'
10. Delivery Address (2) 'Apartment number etc'
11. Delivery Address (3) City
12. Delivery Address (4) Zip Code

However this is redundent and we can create separate tables to handle the Customer,Delivery, address, and item Information

The below diagram fixes that issue.
![Pizzaria Orders DB](https://github.com/user-attachments/assets/2ea10ccd-90f0-4398-b596-69946ab1425a)

### Stock Control Tables
Assuming the lead time for delivery by all supliers is the same for all ingredients.
Need to be able to know when to place orders for new stock - 

1. identify quantities for each ingredient and set alarms for when quantity reaches a certain level per ingredient (this is mostly backend but the schema can help with identifying quantities and inventory rotations).
2. being able to identify which ingredients are used for which recipe.


Stock Control will look like this:
![Pizzaria Stock Control](https://github.com/user-attachments/assets/1bc544ee-ffed-486b-abee-1e14ba588779)




### Staff Tables
Owner wants to be able to know : 
1. which staff member is working when
2. staff salary information


This will help understand the pizza costs (ingredients + staff+ delivery)
we also need to seperate the information about staff and their salaries from shift information and time information so I created the below per the requirements

![Pizzaria DB Schema](https://github.com/user-attachments/assets/a695ea47-028f-428e-a8a0-9775bed9645e)


