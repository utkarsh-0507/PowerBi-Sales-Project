<img width="955" height="550" alt="Screenshot 2026-05-26 193355" src="https://github.com/user-attachments/assets/902458fc-38f7-4933-a534-46e063899d42" />

# PowerBi-Sales-Project

1. Show all customer records
   SELECT * FROM customers;

2. Show total number of customers
   SELECT count(*) FROM customers;

3. Show transactions for Chennai market (Market code for Chennai is Mark001)
   SELECT * FROM transactions where market_code = 'Mark001';

4. Show distinct product codes that were sold in Chennai
   SELECT distinct product_code FROM transactions where market_code = 'Mark001';

5. Show transactions where currency is US dollars
   SELECT * FROM transactions where currency = "USD";

6. Show transactions in 2020 join by date table
   SELECT transactions.*,date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year = 2020;

7. Show total revenue in year 2020 in Chennai
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and
   transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020,January Month
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date on transactions.order_date=date.date where
   date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or
   transactions.currency= "USD\r");

9. Show total revenue in year 2020 in Chennai
   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where
   date.year = 2020 and transactions.market_code ="Mark001";
   
   
