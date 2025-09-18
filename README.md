# Orders-Customer_csv

# This fix using Basic DAX 


# Orders 

--DAX OF Orders TABLE

Count of orders = COUNT(Customers[Order ID])
// Count all rows in the column form orders table 

Count of unique Order ID = DISTINCTCOUNT(Orders[Order ID])

Order Category = IF(Orders[Quantity] < 30,"Small Order","Big Order")
// Condition if quantity < 30 "Small Order","Big Order"

Profit = 
SUM('Orders'[Selling Price]) - SUM('Orders'[Product Cost])
// Sum of selling price - sum of product cost Result is profit

Profit cost = sum(Orders[Selling Price])- sum(Orders[Product Cost])

Total profit = (SUM(Orders[Selling Price]) - SUM(Orders[Product Cost])) *sum(Orders[Quantity])

Total profit Column = (SUM(Orders[Selling Price]) - SUM(Orders[Product Cost])) *(Orders[Quantity])

Total quantity = SUM(Orders[Quantity])
// Sum of quantity form the Orders table 

Unique count = DISTINCTCOUNT(Orders[Product])
// Count unique product in the product column from orders table 


--DAX OF Customer TABLE 

Order day = WEEKDAY(Customers[Order Date],2)
// in this dax forumal returns which day product most salling 

------ Only Practice Purpuse for dax 
