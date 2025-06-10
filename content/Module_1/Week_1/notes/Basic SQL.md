## 🍌Thursday: Database SQL (1)

This class provided foundational understanding for Database SQL

---

### 🔍 Part 1: Introduction to Database

- **Definition**: A database is a collection of organized data, stored in a format that allows easy access, management, and retrieval (e.g., a phone book).
    
    ![image.png](media/image%2016.png)
    
- Motivation: Limitations of managing large datasets (e.g., hundreds of thousands of customers) in Excel. It proposes relational database solutions to address data redundancy and improve efficiency.
    
    ![image.png](media/image%2017.png)
    
- **Example Data**: Customer orders with attributes like Customer ID, Name, Address, Product Name, Quantity, and Date.
- **Solutions**: Two approaches are presented:
    1. Splitting data into separate tables (Customer, Product, Order) with primary keys (C_ID, P_ID) to reduce redundancy.
        
        ![image.png](media/image%2018.png)
        
    2. Using an Order Detail table to link orders with quantities, maintaining relationships via primary keys.

### 💻 Part 2: **Database Management Systems (DBMS)**

This portion introduced tools and application for managing Database

- A DBMS is software that enables users to interact with databases through instructions to execute, retrieve, and manage data.
    
    ![image.png](media/image%2019.png)
    
- **Relational DBMS Examples**: MySQL, Microsoft SQL Server, Oracle.
- **Operations**: Create, Read, Update, Delete (CRUD).

### 📚 Part 3: SQL basic command

- The document outlines SQL queries for data analysis, categorized into:
    - **Basic**: SELECT, WHERE, HAVING, GROUP BY, ORDER BY.
    - **Intermediate**: BETWEEN, LIKE, NULL, IN, OFFSET, COALESCE.
    - **Advanced**: WINDOWS, FUNCTIONS, RANK, PIVOT, Common Table Expressions (CTE).
        
        ![image.png](media/image%2020.png)
        
        - Summary:
            
            ![image.png](media/image%2021.png)
            
- **REGEXP Queries**:
    - Regex basic syntaxs in SQL:
        
        ![image.png](media/image%2022.png)
        
    - Examples include filtering customers by:
        - First names (e.g., ELKA or AMBUR: WHERE first_name REGEXP 'ELKA|AMBUR').
        - Last names ending with EY or ON (WHERE last_name REGEXP 'EY$|ON$').
        - Last names starting with MY or containing SE (WHERE last_name REGEXP '^MY|SE').
        - Last names containing B followed by R or U (WHERE last_name REGEXP 'B[RU]').
            - Can use AIO website to visualize search:
                
                ![image.png](media/image%2023.png)
                
- **REGEXP Syntax Table**: Summarizes patterns like . (any character), [abc] (specific characters), ^ (starts with), $ (ends with), and more.
- Example - Retrieve customers with points > 1000:
    
    <aside>
    📝
    
    SELECT first_name, last_name
    FROM customers
    WHERE points > 1000;
    
    </aside>
    
- Example - Retrieve products with names starting with a vowel:
    
    <aside>
    📝
    
    SELECT name, unit_price
    FROM products
    WHERE name REGEXP '^[aeiouAEIOU]';
    
    </aside>
    

### 🔑 Key Takeaways

- Databases are essential for managing large, structured datasets efficiently, overcoming limitations of tools like Excel.
- MySQL is a popular open-source RDBMS, with clear installation steps provided.
- SQL queries range from basic to advanced, with practical examples for filtering and analyzing data using clauses like SELECT, WHERE, REGEXP, and JOINs.
- The document emphasizes relational database design to eliminate redundancy and ensure data integrity using primary keys.

---