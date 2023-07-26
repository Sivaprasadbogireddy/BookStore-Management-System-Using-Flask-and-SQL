
The database in the this Web Application represents a basic schema for a bookstore. It consists of the following tables with their attributes, primary keys, foreign keys, foreign key constraints, and sample data:

1.	Publisher Table:
    •   Attributes: publisher_id, publisher_name, publication_address, publication_phone, publication_web
    •	The primary key is publisher_id, which uniquely identifies each publisher.
    •	All non-key attributes (publisher_name, publication_address, publication_phone, and publication_web) are functionally dependent on the primary key publisher_id.
    •	There are no transitive dependencies, meaning no non-key attribute is dependent on another non-key attribute.
   Sample Data: 
publisher_id | publisher_name | publication_address | publication_phone | publication_web
-----------------------------------------------------------------------------
472001      | ABC Publishers  | 123 Main St.       | +1 123-456-7890   | www.abcpub.com
019002      | XYZ Publications | 456 Park Ave.      | +1 987-654-3210   | www.xyzpubs.com


2.	Books Table:
    •   Atributes: book_id, title, author, price, publication_year, Publisher_id
    •	The primary key is book_id, which uniquely identifies each book.
    •	All non-key attributes (title, author, price, and publication_year) are functionally dependent on the primary key book_id.
    •	There are no transitive dependencies in this table.
    •   Foreign Key: publisher_id (References Publisher table). 

Sample Data:
    
book_id | title             | author        | price | publication_year | publisher_id
--------------------------------------------------------------------------------------
100001  | Book A            | John Doe      | 25.99 | 2020             | 546001
100002  | Book B            | Jane Smith    | 19.95 | 2019             | 726002

3.	Publisher_Books_Junction Table: 
    •   Attributes: publisher_id, book_id
    •   Primary Key: (publisher_id, book_id)
    •   Foreign Keys: publisher_id (References Publisher table), book_id (References Books table)
    •   This table represents a many-to-many relationship between publishers and books.
    •	This table serves as a junction table to represent the many-to-many relationship between publishers and books.
    •	The combination of publisher_id and book_id forms the primary key, ensuring that each book can be associated with multiple publishers, and each publisher can have multiple books.
    •	There are no non-key attributes in this table, so no non-key attribute is functionally dependent on another non-key attribute.

Sample data:

publisher_id | book_id
---------------------
456001      | 100001
8739002      | 100002

4.	Customers 
    •   Atributes: customer_id, name, email, phone):
    •	The primary key is customer_id, which uniquely identifies each customer.
    •	All non-key attributes (name, email, and phone) are functionally dependent on the primary key customer_id.
    •	There are no transitive dependencies in this table.

Sample Data:

customer_id | name            | email                  | phone
------------------------------------------------------------
100000001   | John Smith      | john.smith@example.com | +1 555-123-4567
100000002   | Jane Doe        | jane.doe@example.com   | +1 555-987-6543

5.	Orders Table:
    •   Atributes: order_id, customer_id, book_id, quantity, order_date, Total_price):
    •	The primary key is order_id, which uniquely identifies each order.
    •	customer_id and book_id are foreign keys that reference the Customers and Books tables, respectively, establishing relationships between orders and customers, as well as orders and books.
    •	All other non-key attributes (quantity, order_date, and Total_price) are functionally dependent on the primary key order_id, and there are no transitive xdependencies in this table.

Sample Data:
order_id  | customer_id | book_id | quantity | order_date  | Total_price
-----------------------------------------------------------------------
100000001 | 100000001   | 100001  | 2        | 2023-07-20  | 51.98
100000002 | 100000002   | 100002  | 1        | 2023-07-21  | 19.95


Overall, the tables follow the principles of 3rd Normal Form(3NF) by ensuring that each table has a primary key, all non-key attributes are fully functionally dependent on the primary key, and there are no transitive dependencies. It eliminates transitive dependencies by breaking down the tables into smaller, logically related entities. The foreign keys maintain referential integrity by referencing the primary keys of other related tables. This schema allows for efficient storage and retrieval of data related to publishers, books, customers, and their respective orders. This design helps to reduce data redundancy and improve data integrity in the database.
