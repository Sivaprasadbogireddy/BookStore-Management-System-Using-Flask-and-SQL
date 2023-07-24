INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id) 
VALUES  (174855,	'Computer Networks: A Systems Approach',	'Larry L. Peterson',	69.8,	2017,178881);

INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id) 
VALUES  (175258	,'Artificial Intelligence: A Modern Approach',	'Stuart Russell'	,320.0	,2016,290289);

INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id) 
VALUES    (180021,'Introduction to Civil Engineering',	'Michael R. Lindeburg',	178.0	,2020,290289);

INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id) 
VALUES     (206166,	'Introduction to Algorithms',	'Thomas H. Cormen',189.8	2019,239344);

INSERT INTO Books (book_id, title, author, price, publication_year,publisher_id) 
VALUES   (290423,	'Introduction to Electrical Engineering',	'John D. Ryder'	,129.0,	2019,239344);

INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (178881,	'HarperWave',	'195 Broadway, New York, NY 10007',	+1 (212) 207-7000,	'www.harperwave.com');
INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (290289,'Texas A&M University Press',	'4234 TAMU, College Station, TX 77843'	,+1 (979) 845-1436,	'www.tamupress.com');
INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (239344,	'Oregon State University Press',	'121 The Valley Library, Corvallis, OR 97331',	+1 (541) 737-3166,	osupress.oregonstate.edu);

INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (943066,	'Florida Historical Society Press',	'435 Brevard Ave, Cocoa, FL 32922',	+1 (321) 690-1971,	'www.myfloridahistory.org');
INSERT INTO Publisher (publisher_id, publisher_name, publication_address, publication_phone, publication_web) VALUES (335590,	'University of California Press'	,'2120 Berkeley Way, Berkeley, CA 94704',	+1 (510) 642-4247	,'www.ucpress.edu');

INSERT INTO Customers (customer_id, name, email, phone) VALUES (1379460428,	'Customer1',	'customer1@gmail.com' ,	+1 (316) 726-0000);	
INSERT INTO Customers (customer_id, name, email, phone) VALUES (1415962885,	'Customer 4',	'customer4@gmail.com'	 ,            +1 (300) 000-8000);
INSERT INTO Customers (customer_id, name, email, phone) VALUES (3171915338,	'Customer3',	'customer3@gmail.com	'  ,            +1 (010) 000-1100);

INSERT INTO Customers (customer_id, name, email, phone) VALUES (7323308292,	'Customer 5',	'customer5@gmail.com	'   ,           +1 (002) 000-2000);

INSERT INTO Customers (customer_id, name, email, phone) VALUES (9789084544,	'Customer2',	'Customer2@gmail.com',	+1 (000) 000-0000);

INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (10308240,	3171915338,	312938,	2,	2023-07-18,	262);

INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (12698727,	7323308292,	206166,	1,	2023-07-24,	189.8);

INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (14531385, 3171915338,	175258,	2,	2023-07-14,	640);

INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (16324697,	1379460428,	175258,	3,	2023-07-14,	960)
INSERT INTO Orders (order_id, customer_id, book_id, quantity, order_date, Total_price) VALUES (17182864,	7323308292,	180021,	3,	2023-07-27,	534);

