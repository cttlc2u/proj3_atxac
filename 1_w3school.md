# Part 1: W3Schools SQL Lab 

*Introductory level SQL*

--

This challenge uses the [W3Schools SQL playground](http://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all). Please add solutions to this markdown file and submit.

1. Which customers are from the UK?
Thomas Hardy
Victoria Ashworth
Elizabeth Brown
Ann Devon
Helen Bennett
Simon Crowther
Hari Kumar

2. What is the name of the customer who has the most orders?
Ernst Handel has the most orders.

3. Which supplier has the highest average product price?
Aux joyeux ecclésiastiques has the highest average product price.

4. How many different countries are all the customers from? (*Hint:* consider [DISTINCT](http://www.w3schools.com/sql/sql_distinct.asp).)
There are twenty-one (21) distinct countires customers are from.

5. What category appears in the most orders?
Dairy Products appear the most in orders.

6. What was the total cost for each order?
Not sure I'm supposed to post all 196 orders.
My query was:
SELECT OrderDetails.OrderID, (OrderDetails.Quantity*Products.Price) AS total_price FROM OrderDetails LEFT JOIN Products ON OrderDetails.ProductID = Products.ProductID GROUP BY OrderID;

7. Which employee made the most sales (by total price)?
Margaret Peacock made the most sales.

8. Which employees have BS degrees? (*Hint:* look at the [LIKE](http://www.w3schools.com/sql/sql_like.asp) operator.)
Two employees have BS degrees.

9. Which supplier of three or more products has the highest average product price? (*Hint:* look at the [HAVING](http://www.w3schools.com/sql/sql_having.asp) operator.)
Plutzer Lebensmittelgroßmärkte AG is the supplier with three or more products with the highest average product price.
