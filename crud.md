# CRUD operations on books table
select * from Books;

INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id,publisher_id) VALUES  (174855,	'Computer Networks: A Systems Approach',	'Larry L. Peterson',	69.8,	2017,17881);

UPDATE Books 
SET publication_year=2020 
WHERE book_id=174855;

DELETE FROM Books WHERE book_id=174855;



# CRUD operations on customer table

SELECT * FROM Customers;

INSERT INTO Customers (customer_id, name, email, phone) VALUES (1379460428,	'Customer1',	'customer1@gmail.com' ,	+1 (316) 726-0000);

UPDATE Customers SET email='customer12@gmail.com' WHERE customer_id=1379460428;

DELETE FROM Customers WHERE customer_id=1379460428;

# CRUD operations on publisher table

INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (943066,	'Florida Historical Society Press',	'435 Brevard Ave, Cocoa, FL 32922',	+1 (321) 690-1971,	'www.myfloridahistory.org');

SELECT * FROM Publisher;

UPDATE Publisher SET publisher_name='HYderabad historical Press' WHERE publisher_id=943066;

DELETE FROM Publisher WHERE publisher_id=943066;

# CRUD operations on orders
select * from Orders;

INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (12698727, 7323308292, 206166, 1,	2023-07-24,	189.8);

UPDATE Orders SET order_date=2023-08-24 WHERE order_id=12698727;

DELETE FROM Orders WHERE order_id=12698727;

