-- select all columns from products table
SELECT * FROM mydb.products;


-- select name and phone columns from shippers table
SELECT name, phone FROM shippers;

-- select average, min and max price from products table
SELECT AVG(price) as avg_price, MIN(price) as min_price, MAX(price) as max_price FROM products;

-- select 10 unique combinations of category_id and price sorted by descent price
SELECT DISTINCT category_id, price FROM products
ORDER BY price DESC
LIMIT 10; 


-- define products quantity in the price range from 20 to 100
SELECT COUNT(*) as products_count FROM products WHERE price >= 20 AND price <= 100;

-- define products quantity and average price for each supplier_id 
SELECT supplier_id, COUNT(*) as prod_count, AVG(price) as avg_price FROM products
GROUP BY supplier_id; 
