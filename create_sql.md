CREATE TABLE IF NOT EXISTS Publisher (
                        publisher_id TEXT PRIMARY KEY,
                        publisher_name TEXT,
                        publication_address TEXT,
                        publication_phone TEXT,
                        publication_web TEXT
                    )

CREATE TABLE IF NOT EXISTS Books (
                        book_id INTEGER PRIMARY KEY AUTOINCREMENT,
                        title TEXT,
                        author TEXT,
                        price REAL,
                        publication_year INTEGER
                    )

CREATE TABLE IF NOT EXISTS Publisher_Books_Junction (
                        publisher_id TEXT,
                        book_id INTEGER,
                        FOREIGN KEY (publisher_id) REFERENCES Publisher (publisher_id),
                        FOREIGN KEY (book_id) REFERENCES Books (book_id),
                        PRIMARY KEY (publisher_id, book_id)
                    )

CREATE TABLE IF NOT EXISTS Customers (
                        customer_id INTEGER PRIMARY KEY,
                        name TEXT,
                        email TEXT,
                        phone TEXT
                    )
                    
CREATE TABLE IF NOT EXISTS Orders (
                        order_id INTEGER PRIMARY KEY,
                        customer_id INTEGER,
                        book_id INTEGER,
                        quantity INTEGER,
                        order_date TEXT,
                        Total_price INTEGER,
                        FOREIGN KEY (customer_id) REFERENCES Customers (customer_id),
                        FOREIGN KEY (book_id) REFERENCES Books (book_id)
                    )