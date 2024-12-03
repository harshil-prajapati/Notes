<div align="center"><b><h1>Index</h1></b></div>

[[#1. What is DBMS? Discuss the structure of DBMS.]]
[[#2. Advantage of DBMS.]]
[[#3. Differentiate RDBMS and DBMS.]]
[[#4. What is database? Explain three levels of database architecture.]]
[[#5. Explain external level and internal level Database System Architecture.]]
[[#6. Write a short note on 5NF.]]
[[#7. What is SQL? Describe and analyze the components of SQL.]]
[[#8. Differentiate Delete Vs. Truncate command.]]
[[#9. What is scalar function? Illustrate any six numeric functions with proper example.]]
[[#10. Discuss brief about Sequence object in Oracle.]]
[[#11. Discuss various data types in Oracle.]]
[[#12. What is DBA? Determine roles of DBA.]]
[[#13. Differentiate DBMS Vs. RDBMS.]]
[[#14. Illustrate E/R Diagram in details.]]
[[#15. List out types of Constraints. Explain check constraint with proper example.]]
[[#16. Demonstrate Oracle group functions with example.]]
[[#17. Differentiate SQL Vs. SQL*Plus.]]
[[#18. Explain various options of SET command.]]
[[#19. Discuss brief about index object in Oracle.]]
[[#20. Explain DR E.F. Cold rules of RDBMS.]]
[[#21. Short note on data model.]]
[[#22. Discuss 3NF and 2NF with example.]]
[[#23. Discuss aggregate function.]]
[[#24. Short note on set operation.]]
[[#25. Explain foreign key and primary key with example.]]
[[#26. Discuss DDL command? Explain in brief.]]
[[#27. Discuss DML command? Explain in brief.]]
[[#28. Explain index in detail. Types of index.]]
[[#29. Discuss sequence syntax with an example.]]
[[#30. Explain ER-model and its component.]]
[[#31. What is Join? Explain with example and list out its type.]]
[[#32. Components of DBMS.]]
[[#33. What is constraint? Types of constraint.]]
[[#34. Group by and having clause in SQL.]]
[[#35. What is the difference between GRANT and REVOKE in SQL?]]

---
---
### 1. What is DBMS? Discuss the structure of DBMS.

A **Database Management System (DBMS)** is a software system that provides an interface to interact with databases, allowing users to store, retrieve, and manipulate data efficiently. It helps in managing and organizing large amounts of data while ensuring data integrity, security, and consistency.

### Structure of DBMS:

The structure of a DBMS can be broadly categorized into the following components:

1. **Database Engine:**
    - The core part of DBMS that handles data storage, retrieval, and updating. It manages data access, indexing, and query processing.
2. **Database Schema:**
    - It defines the logical design and structure of the database, including tables, views, relationships, and constraints. It provides a blueprint for how the data is organized.
3. **Database Query Processor:**
    - This component translates user queries (written in a query language like SQL) into low-level instructions that the database engine can understand and execute.
4. **Data Dictionary:**
    - A metadata repository that stores information about the database structure, such as tables, columns, data types, and constraints. It helps in data integrity and query optimization.
5. **Transaction Management:**
    - It ensures that all database operations (insert, update, delete) are processed in a way that guarantees the ACID properties (Atomicity, Consistency, Isolation, Durability), maintaining data accuracy and consistency.
6. **Database Users:**
    - DBMS supports different types of users, such as:
        - **Database Administrators (DBAs):** Manage the overall database system, including maintenance, performance optimization, and security.
        - **End-users:** Interact with the system through application software or queries.
        - **Application Developers:** Build applications that interact with the database.
---
---
### 2. Advantages of DBMS

A Database Management System (DBMS) offers several advantages over traditional file-based systems. Some key benefits include:

1. **Data Redundancy Control:**
    - DBMS reduces data redundancy by storing data in a centralized manner. It ensures that data is not duplicated unnecessarily, leading to efficient use of storage.
2. **Data Integrity:**
    - DBMS enforces data integrity constraints (like primary keys, foreign keys, and unique constraints), ensuring that the data remains accurate, consistent, and reliable.
3. **Data Security:**
    - DBMS provides various security features like user authentication, access control, and encryption to protect data from unauthorized access and ensure privacy.
4. **Data Consistency:**
    - DBMS ensures that data remains consistent across different parts of the database through transaction management and adherence to ACID properties (Atomicity, Consistency, Isolation, Durability).
5. **Improved Data Access:**
    - DBMS supports powerful query languages (such as SQL) that make it easier and faster to retrieve, insert, update, and delete data, enhancing user efficiency.
6. **Data Independence:**
    - DBMS provides data abstraction, separating data from application programs. This allows changes to the database structure without affecting the application software.
7. **Backup and Recovery:**
    - DBMS provides automatic backup and recovery mechanisms that ensure the database can be restored in case of a failure, preventing data loss.
8. **Multi-user Access:**
    - DBMS allows multiple users to access and work with the database simultaneously, supporting concurrent operations while ensuring data consistency through transaction management.
---
---
### 3. Differentiate RDBMS and DBMS

|**Feature**|**DBMS (Database Management System)**|**RDBMS (Relational Database Management System)**|
|---|---|---|
|**Data Structure**|DBMS stores data in a file-based structure, often in the form of hierarchical, network, or object-oriented models.|RDBMS stores data in a tabular format, using tables (relations) that are linked through primary and foreign keys.|
|**Data Relationship**|DBMS may not support data relationships or enforce constraints between data.|RDBMS enforces relationships between tables using primary keys, foreign keys, and integrity constraints.|
|**Normalization**|Data normalization may or may not be supported in DBMS.|RDBMS supports normalization to eliminate redundancy and ensure efficient data storage.|
|**Data Redundancy**|Higher chances of data redundancy as DBMS may store data in an unstructured manner.|RDBMS minimizes data redundancy by storing data in normalized tables with well-defined relationships.|
|**Query Language**|DBMS may not have a standardized query language; data may be accessed using procedural or low-level languages.|RDBMS uses Structured Query Language (SQL), a standard language for querying and managing data.|
|**ACID Properties**|DBMS may not fully support ACID properties (Atomicity, Consistency, Isolation, Durability).|RDBMS fully supports ACID properties, ensuring reliable and consistent transaction management.|
|**Scalability**|DBMS systems may not handle large-scale data efficiently.|RDBMS is designed to efficiently manage large datasets and can scale well for complex queries and large applications.|
|**Examples**|Examples include file-based systems, hierarchical databases, and network databases.|Examples include MySQL, PostgreSQL, Oracle, and SQL Server.|

---
---
### 4. What is a database? Explain three levels of the database architecture.

A **database** is an organized collection of data that is stored and accessed electronically. It provides a systematic way to store, manage, and retrieve data efficiently and securely.

### Three Levels of Database Architecture:

1. **Internal Level (Physical Level):**
    - This level defines how data is physically stored in the storage medium (e.g., hard drives). It deals with the organization of data files, indexes, and the storage structure (tablespaces, blocks, etc.).
2. **Conceptual Level (Logical Level):**
    - This level provides a view of the entire database as a whole without showing details of physical storage. It defines the logical structure, such as tables, views, and relationships, but abstracts away implementation details.
3. **External Level (User Level):**
    - This level defines how individual users or user groups view the data. It provides a personalized or customized view of the database, ensuring data privacy and security by restricting access to specific parts of the database.
---
---
### 5. Explain External Level and Internal Level of Database System Architecture.

1. **External Level (User Level):**
    - It refers to the different views of the database presented to individual users or user groups. Each user may see a different part of the database depending on the requirements and access permissions. The external schema hides the complexity of the internal structure.
    - Example: A user may only see the customer’s table and not the internal file storage.
2. **Internal Level (Physical Level):**
    - The internal level defines how data is stored on physical media like hard drives or disks. It involves defining the storage structure, file organization, indexing methods, and how data is stored efficiently to ensure performance.
    - Example: Data is stored in tablespaces, and index structures like B-trees are used for quick retrieval.
---
---
### 6. Write a short note on 5NF.

**5NF (Fifth Normal Form)** is the highest level of normalization in relational database design, aimed at reducing redundancy and ensuring that data dependencies are strictly maintained. A table is in **5NF** if it is in **4NF** (fourth normal form) and does not contain any join dependencies that can be decomposed into smaller tables without losing data.

- It ensures that no information is duplicated unnecessarily and that all data relationships are represented logically.
- Example: A table with columns (student_id, course, instructor) might be split into two tables (student_id, course) and (course, instructor) to avoid redundancy.
---
---
### 7. What is SQL? Describe and analyze the components of SQL.

**SQL (Structured Query Language)** is a standardized language used to manage and manipulate relational databases. It is used for querying, inserting, updating, and deleting data, as well as for database schema creation and modification.

#### Components of SQL:

1. **DML (Data Manipulation Language):**
    - Used for querying and modifying data within the database.
    - Examples: `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
2. **DDL (Data Definition Language):**
    - Defines the structure of the database, including tables, indexes, and schemas.
    - Examples: `CREATE`, `ALTER`, `DROP`.
3. **DCL (Data Control Language):**
    - Manages access controls and permissions for database users.
    - Examples: `GRANT`, `REVOKE`.
4. **TCL (Transaction Control Language):**
    - Controls transactions in the database.
    - Examples: `COMMIT`, `ROLLBACK`, `SAVEPOINT`.

SQL allows for both data manipulation and schema management, ensuring that data can be queried, modified, and maintained securely and efficiently.

---
---
### 8. Differentiate Delete vs. Truncate command.

|**Feature**|**DELETE**|**TRUNCATE**|
|---|---|---|
|**Operation Type**|A DML (Data Manipulation Language) command.|A DDL (Data Definition Language) command.|
|**Data Removal**|Deletes rows one by one; can be filtered with a WHERE clause.|Removes all rows in a table without any condition.|
|**Transaction Log**|Each row deletion is logged in the transaction log.|Minimal logging; only the deallocation of data pages is logged.|
|**Performance**|Slower, especially for large datasets.|Faster, as it does not log each row deletion.|
|**Rollback Capability**|Can be rolled back (if within a transaction).|Cannot be rolled back in most databases.|
|**Trigger Activation**|Triggers (like `ON DELETE`) are activated.|Triggers are not activated.|
|**Space Reclamation**|Does not immediately release the storage space.|Immediately frees the allocated space.|

---
---
### 9. What is a scalar function? Illustrate any six numeric functions with proper example.

A **scalar function** is a function in SQL that operates on a single value and returns a single value. It can be used in queries to perform calculations or transformations on data.

### Six Numeric Functions in SQL:

1. **ABS(x):**
    - Returns the absolute value of `x`.
    - Example: `SELECT ABS(-10);` returns `10`.
2. **ROUND(x, d):**
    - Rounds the number `x` to `d` decimal places.
    - Example: `SELECT ROUND(123.4567, 2);` returns `123.46`.
3. **CEIL(x):**
    - Returns the smallest integer greater than or equal to `x`.
    - Example: `SELECT CEIL(12.3);` returns `13`.
4. **FLOOR(x):**
    - Returns the largest integer less than or equal to `x`.
    - Example: `SELECT FLOOR(12.8);` returns `12`.
5. **MOD(x, y):**
    - Returns the remainder when `x` is divided by `y`.
    - Example: `SELECT MOD(10, 3);` returns `1`.
6. **POWER(x, y):**
    - Returns `x` raised to the power of `y`.
    - Example: `SELECT POWER(2, 3);` returns `8`.
---
---
### 10. Discuss briefly about Sequence object in Oracle.

A **sequence** in Oracle is a database object used to generate unique numbers, often used for creating primary key values. It automatically increments the number each time it is used.

### Key Features:

- **Creation**: A sequence is created using the `CREATE SEQUENCE` statement, specifying parameters like increment value, starting value, and maximum value.
    
- **Usage**: Sequences are used with the `NEXTVAL` (to get the next number) and `CURRVAL` (to retrieve the current number) functions.
    Example:
    ```sql
    CREATE SEQUENCE emp_seq
    START WITH 1
    INCREMENT BY 1;
    
    SELECT emp_seq.NEXTVAL FROM dual;
    ```
    
- **Customization**: Sequences can be customized to define the minimum and maximum value, caching, and cycling options.
---
---
### 11. Discuss various data types in Oracle.

Oracle provides various data types to store different kinds of data in a database. Here are the main data types:

1. **Numeric Data Types:**
    - **NUMBER(p,s):** Stores numbers with precision `p` and scale `s`. For example, `NUMBER(5,2)` can store values like 123.45.
    - **INTEGER:** Stores whole numbers.
    - **FLOAT:** Stores floating-point numbers.
2. **Character Data Types:**
    - **CHAR(n):** Stores fixed-length character strings of length `n`.
    - **VARCHAR2(n):** Stores variable-length character strings, with a maximum length of `n`.
    - **CLOB:** Used to store large text data (up to 4 GB).
3. **Date and Time Data Types:**
    - **DATE:** Stores date and time up to the second.
    - **TIMESTAMP:** Stores date and time with fractional seconds.
    - **INTERVAL:** Stores a time span (e.g., INTERVAL '10' DAY).
4. **Binary Data Types:**
    - **BLOB:** Stores large binary data (up to 4 GB), such as images or audio files.
    - **RAW:** Stores variable-length binary data.
5. **Other Data Types:**
    - **BOOLEAN:** Represents true or false values (in PL/SQL).
    - **ROWID:** A unique identifier for a row in a database table.
    - **XMLType:** Stores XML data.
---
---
### 12. What is DBA? Determine roles of DBA.

A **DBA (Database Administrator)** is responsible for managing and maintaining a database system. The DBA ensures that databases are running efficiently, securely, and reliably.

### Roles of DBA:

1. **Database Design:** The DBA is responsible for designing the database schema, ensuring that it meets business requirements and is efficient.
2. **Installation and Configuration:** Installs and configures the database software, ensuring optimal settings.
3. **Data Security:** Defines user roles, access controls, and security measures to protect data.
4. **Backup and Recovery:** Implements regular backup procedures and disaster recovery plans.
5. **Performance Tuning:** Monitors and optimizes database performance by adjusting parameters, indexing, and querying techniques.
6. **Data Integrity:** Ensures the integrity of data through validation rules and constraints.
7. **Database Maintenance:** Performs regular updates, patches, and ensures that the system is running smoothly.
8. **Monitoring:** Keeps track of database activity, usage, and system health.
---
---
### 13. Differentiate DBMS vs. RDBMS.

| **Feature**           | **DBMS (Database Management System)**                                                   | **RDBMS (Relational DBMS)**                                           |
| --------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Data Structure**    | Stores data in various formats like hierarchical or network models.                     | Stores data in tables (relations) using a relational model.           |
| **Data Relationship** | May not enforce relationships between data entities.                                    | Enforces relationships between tables using primary and foreign keys. |
| **Normalization**     | Does not necessarily support normalization.                                             | Supports normalization to reduce redundancy.                          |
| **Query Language**    | May not support a standardized query language.                                          | Uses SQL (Structured Query Language) for querying and managing data.  |
| **ACID Compliance**   | May not guarantee full ACID properties (Atomicity, Consistency, Isolation, Durability). | Guarantees ACID properties for transaction management.                |
| **Examples**          | File systems, hierarchical databases.                                                   | Oracle, MySQL, PostgreSQL, SQL Server.                                |

---
---
### 14. Illustrate E/R Diagram in details.

An **Entity-Relationship (E/R) diagram** is a visual representation of the entities within a database and their relationships.

#### Components:

1. **Entities:** Represent objects or things that have data stored about them. Example: `Student`, `Course`.
2. **Attributes:** Characteristics or properties of an entity. Example: `Student Name`, `Course Code`.
3. **Relationships:** The associations between entities. Example: A `Student` **enrolls in** a `Course`.
4. **Primary Key (PK):** Uniquely identifies an entity. Example: `Student ID` for `Student`.
5. **Foreign Key (FK):** A key from one entity that is used to establish a relationship with another entity. Example: `Course ID` in `Student_Course` table.
6. **Cardinality:** Specifies how many instances of one entity are associated with instances of another entity (one-to-many, many-to-many, etc.).
---
---
### 15. List out types of Constraints. Explain CHECK constraint with proper example.

#### Types of Constraints:

1. **NOT NULL:** Ensures that a column cannot have a NULL value.
2. **PRIMARY KEY:** Ensures that a column or set of columns uniquely identifies each record.
3. **FOREIGN KEY:** Enforces a relationship between tables.
4. **UNIQUE:** Ensures that all values in a column are distinct.
5. **CHECK:** Ensures that all values in a column satisfy a specific condition.
6. **DEFAULT:** Assigns a default value to a column if no value is specified.

#### CHECK Constraint:

The **CHECK** constraint ensures that the values entered into a column satisfy a specified condition.

##### Example:
```sql
CREATE TABLE Employees (
  EmployeeID INT,
  Name VARCHAR(50),
  Age INT,
  CHECK (Age >= 18)
);
```

In this example, the **CHECK** constraint ensures that only employees aged 18 or older are inserted into the `Employees` table.

---
---
### 16. Demonstrate Oracle Group Functions with example.

Oracle **Group Functions** (also known as aggregate functions) operate on a set of rows and return a single value.

#### Common Group Functions:

1. **COUNT():** Returns the number of rows.
    - Example: `SELECT COUNT(*) FROM Employees;`
2. **SUM():** Returns the sum of values in a column.
    - Example: `SELECT SUM(Salary) FROM Employees;`
3. **AVG():** Returns the average value of a column.
    - Example: `SELECT AVG(Salary) FROM Employees;`
4. **MIN():** Returns the smallest value.
    - Example: `SELECT MIN(Salary) FROM Employees;`
5. **MAX():** Returns the largest value.
    - Example: `SELECT MAX(Salary) FROM Employees;`
6. **GROUP_CONCAT():** Concatenates values from multiple rows into a single string.
---
---
### 17. Differentiate SQL vs. SQL*Plus.

| **Feature**     | **SQL**                                                                                               | **SQL*Plus**                                                                             |
| --------------- | ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| **Definition**  | SQL (Structured Query Language) is a standard language used to query and manage relational databases. | SQL*Plus is an Oracle command-line tool for interacting with Oracle databases using SQL. |
| **Purpose**     | SQL is used for querying, updating, inserting, and managing databases.                                | SQL*Plus is used to run SQL commands, scripts, and manage database sessions.             |
| **Environment** | SQL is used in many environments (MySQL, PostgreSQL, etc.).                                           | SQL*Plus is specifically used with Oracle databases.                                     |
| **Interface**   | SQL is a language used across multiple interfaces.                                                    | SQL*Plus provides a command-line interface to interact with Oracle.                      |

---
---
### 18. Explain various options of SET command.

The `SET` command in SQL*Plus is used to configure various options that affect the environment.
#### Common `SET` Options:

1. **SET ECHO ON/OFF:** Displays the SQL commands as they are executed. (`SET ECHO ON`)
2. **SET LINESIZE n:** Sets the number of characters per line for output. Example: `SET LINESIZE 100`.
3. **SET PAGESIZE n:** Sets the number of lines per page for query results. Example: `SET PAGESIZE 20`.
4. **SET FEEDBACK ON/OFF:** Shows the number of records returned by a query. (`SET FEEDBACK ON`)
5. **SET VERIFY ON/OFF:** Determines whether SQL*Plus displays the substitution variable values in the SQL command before execution.
---
---
19. Discuss briefly about index object in Oracle.

An **index** in Oracle is an optional structure that enhances database performance by speeding up data retrieval operations. It is typically created on columns that are frequently used in query conditions.

#### Types of Indexes:

1. **B-tree Index:** The default and most commonly used index type.
2. **Bitmap Index:** Useful for columns with low cardinality (few distinct values).
3. **Clustered Index:** Organizes data rows in the table based on the index order.
4. **Unique Index:** Ensures uniqueness of the indexed column's values.

#### Creating an Index:
```sql
CREATE INDEX emp_idx ON Employees (EmployeeName);
```
---
---
### 20. Explain Dr. E.F. Codd's Rules of RDBMS.

Dr. **E.F. Codd** proposed 12 rules for relational database systems, often referred to as **Codd's 12 Rules**. These rules define the key characteristics that an RDBMS must have to be considered truly relational.

Some important rules include:

1. **Rule 1:** The information rule: All information in the database should be represented in tables (relations).
2. **Rule 2:** The guaranteed access rule: All data should be accessible without ambiguity.
3. **Rule 3:** Systematic treatment of null values: A DBMS must be able to handle NULL values effectively.
4. **Rule 5:** The relational view rule: A DBMS must provide a relational view for interacting with data.
5. **Rule 9:** The logical data independence rule: The logical schema of the database should be independent of the physical schema.
---
---
### 21. Short note on Data Model.

A **data model** is a conceptual framework used to define and structure the data within a database. It defines how data is stored, related, and manipulated.

#### Types of Data Models:

1. **Hierarchical Model:** Organizes data in a tree-like structure where each record has a single parent. Example: File systems.
2. **Network Model:** Similar to the hierarchical model but allows more complex relationships (many-to-many) between records.
3. **Relational Model:** Data is organized in tables (relations), and each table has rows and columns. This is the most widely used model (e.g., RDBMS).
4. **Object-Oriented Model:** Represents data as objects, similar to object-oriented programming.
5. **Entity-Relationship Model:** Describes data and its relationships using entities, attributes, and relationships.
---
---
### 22. Discuss 3NF and 2NF with Example.

##### Second Normal Form (2NF):

A relation is in **2NF** if it is in **1NF** (First Normal Form) and all non-key attributes are fully functionally dependent on the primary key.

#### Example of 2NF:

Consider a table storing student details:

| StudentID | CourseID | CourseName | Instructor |
| --------- | -------- | ---------- | ---------- |
| 101       | C01      | Math       | Dr. Smith  |
| 101       | C02      | Physics    | Dr. Lee    |

Here, the combination of `StudentID` and `CourseID` forms the primary key, but `CourseName` and `Instructor` depend only on `CourseID`, not on the full primary key. To bring it to 2NF, we split the table:

**Student Table:**

| StudentID | CourseID |
| --------- | -------- |
| 101       | C01      |
| 101       | C02      |

**Course Table:**

| CourseID | CourseName | Instructor |
| -------- | ---------- | ---------- |
| C01      | Math       | Dr. Smith  |
| C02      | Physics    | Dr. Lee    |

### **Third Normal Form (3NF):**

A relation is in **3NF** if it is in **2NF** and all transitive dependencies are removed. That is, non-key attributes should not depend on other non-key attributes.

#### Example of 3NF:

Consider the following table:

| StudentID | CourseID | Instructor | InstructorPhone |
| --------- | -------- | ---------- | --------------- |
| 101       | C01      | Dr. Smith  | 123-4567        |
| 101       | C02      | Dr. Lee    | 987-6543        |

Here, `InstructorPhone` depends on `Instructor`, which is a non-key attribute. To convert to 3NF, we split the table:

**Student_Course Table:**

| StudentID | CourseID | Instructor |
| --------- | -------- | ---------- |
| 101       | C01      | Dr. Smith  |
| 101       | C02      | Dr. Lee    |

**Instructor Table:**

| Instructor | InstructorPhone |
| ---------- | --------------- |
| Dr. Smith  | 123-4567        |
| Dr. Lee    | 987-6543        |

Now, the data is in 3NF.

---
---
### 23. Discuss Aggregate Function.

**Aggregate functions** in SQL perform a calculation on a set of values and return a single result. These functions are often used with the `GROUP BY` clause to summarize data.

#### Common Aggregate Functions:

1. **COUNT():** Counts the number of rows.
    - Example: `SELECT COUNT(*) FROM Employees;`
2. **SUM():** Returns the sum of the values in a column.
    - Example: `SELECT SUM(Salary) FROM Employees;`
3. **AVG():** Returns the average value of a column.
    - Example: `SELECT AVG(Salary) FROM Employees;`
4. **MIN():** Returns the smallest value in a column.
    - Example: `SELECT MIN(Salary) FROM Employees;`
5. **MAX():** Returns the largest value in a column.
    - Example: `SELECT MAX(Salary) FROM Employees;`
---
---
### 24. Short note on Set Operation.

**Set operations** in SQL allow combining the results of two or more SELECT queries. The main set operations are:

1. **UNION:** Combines the results of two queries, eliminating duplicates.
    - Example: `SELECT Name FROM Employees UNION SELECT Name FROM Managers;`
2. **INTERSECT:** Returns only the common records between two queries.
    - Example: `SELECT Name FROM Employees INTERSECT SELECT Name FROM Managers;`
3. **EXCEPT (or MINUS in Oracle):** Returns records from the first query that are not present in the second query.
    - Example: `SELECT Name FROM Employees EXCEPT SELECT Name FROM Managers;`
---
---
### 25. Explain Foreign Key and Primary Key with Example.

- **Primary Key:** A primary key uniquely identifies each record in a table. A table can have only one primary key, which may consist of one or more columns.
    
    **Example:**   
    ```sql
    CREATE TABLE Employees (
        EmployeeID INT PRIMARY KEY,
        Name VARCHAR(50)
    );
    ```
    
- **Foreign Key:** A foreign key is a column (or a set of columns) that creates a link between two tables. It references the primary key of another table to establish a relationship.
    
    **Example:**
    ```sql
    CREATE TABLE Orders (
        OrderID INT PRIMARY KEY,
        EmployeeID INT,
        FOREIGN KEY (EmployeeID) REFERENCES Employees(EmployeeID)
    );
    ```   
---
---
### 26. Discuss DDL Command? Explain in Brief.

**DDL (Data Definition Language)** commands are used to define, modify, and delete database objects such as tables, indexes, and schemas. The key DDL commands are:

1. **CREATE:** Used to create new tables, views, or other objects.
    - Example: `CREATE TABLE Employees (EmployeeID INT, Name VARCHAR(50));`
2. **ALTER:** Used to modify existing database objects.
    - Example: `ALTER TABLE Employees ADD COLUMN Age INT;`
3. **DROP:** Used to delete tables or other objects.
    - Example: `DROP TABLE Employees;`
4. **TRUNCATE:** Removes all rows from a table without logging individual row deletions.
    - Example: `TRUNCATE TABLE Employees;`
---
---
### 27. Discuss DML Command? Explain in Brief.

**DML (Data Manipulation Language)** commands are used for manipulating data in tables. The main DML commands are:

1. **SELECT:** Retrieves data from one or more tables.
    - Example: `SELECT * FROM Employees;`
2. **INSERT:** Adds new rows to a table.
    - Example: `INSERT INTO Employees (EmployeeID, Name) VALUES (1, 'John Doe');`
3. **UPDATE:** Modifies existing data in a table.
    - Example: `UPDATE Employees SET Age = 30 WHERE EmployeeID = 1;`
4. **DELETE:** Removes rows from a table.
    - Example: `DELETE FROM Employees WHERE EmployeeID = 1;`
---
---
### 28. Explain Index in Detail. Types of Index.

An **index** is a database object that improves the speed of data retrieval operations. It works like a book's index, helping to locate rows quickly.

#### Types of Indexes:

1. **B-tree Index:** The default index type, used for most queries.
2. **Bitmap Index:** Efficient for columns with few distinct values (e.g., gender, status).
3. **Clustered Index:** Organizes data in the table based on the index.
4. **Unique Index:** Ensures that the values in the indexed column are unique.
5. **Composite Index:** An index on multiple columns.
6. **Full-text Index:** Used for text searching within large text columns.
---
---
### 29. Discuss Sequence Syntax with an Example.

A **sequence** is a database object used to generate a sequence of unique numeric values, often used for auto-incrementing primary keys.
#### Syntax:
```sql
CREATE SEQUENCE seq_name
START WITH start_value
INCREMENT BY increment_value
[MINVALUE min_value]
[MAXVALUE max_value]
[CYCLE | NOCYCLE];
```
### Example:
```sql
CREATE SEQUENCE emp_seq
START WITH 1
INCREMENT BY 1;
```

To get the next value from the sequence:
```sql
SELECT emp_seq.NEXTVAL FROM dual;
```
---
---
### 30. Explain ER-Model and Its Components.

The **Entity-Relationship (ER) Model** is a conceptual framework for modeling data. It uses diagrams to describe entities, their attributes, and the relationships between them.

#### Components of ER Model:

1. **Entity:** Represents a real-world object (e.g., `Employee`, `Course`).
2. **Attributes:** Properties or details of an entity (e.g., `EmployeeName`, `CourseCode`).
3. **Relationship:** Describes associations between entities (e.g., `Employee` works on a `Project`).
4. **Primary Key:** Uniquely identifies an entity instance.
5. **Foreign Key:** An attribute that creates a relationship between two entities.
6. **Cardinality:** Specifies the number of instances of one entity that can be associated with instances of another entity (e.g., one-to-many, many-to-many).
---
---
### 31. What is Join? Explain with Example and List Out Its Types.

A **JOIN** is used in SQL to combine data from two or more tables based on a related column between them. It allows us to retrieve data that is spread across multiple tables.

#### Types of Joins:

1. **INNER JOIN:** Returns only the rows where there is a match in both tables.    
    - Example:
        ```sql
        SELECT Employees.EmployeeID, Employees.Name, Orders.OrderID
        FROM Employees
        INNER JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID;
        ```
        
2. **LEFT JOIN (or LEFT OUTER JOIN):** Returns all rows from the left table, and the matching rows from the right table. If there is no match, NULL values are returned for columns from the right table.
    - Example:
        ```sql
        SELECT Employees.EmployeeID, Employees.Name, Orders.OrderID
        FROM Employees
        LEFT JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID;
        ```
        
3. **RIGHT JOIN (or RIGHT OUTER JOIN):** Returns all rows from the right table, and the matching rows from the left table. If there is no match, NULL values are returned for columns from the left table.
    - Example:
        ```sql
        SELECT Employees.EmployeeID, Employees.Name, Orders.OrderID
        FROM Employees
        RIGHT JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID;
        ```
        
4. **FULL OUTER JOIN:** Returns all rows when there is a match in one of the tables. If there is no match, NULL values are returned for columns from the table without a match.
    - Example:
        ```sql
        SELECT Employees.EmployeeID, Employees.Name, Orders.OrderID
        FROM Employees
        FULL OUTER JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID;
        ```
        
5. **SELF JOIN:** A self join is a join where a table is joined with itself.
    - Example:
        ```sql
        SELECT A.EmployeeID, A.Name, B.Name AS ManagerName
        FROM Employees A, Employees B
        WHERE A.ManagerID = B.EmployeeID;
        ```
---
---
### 32. Components of DBMS.

A **DBMS** (Database Management System) consists of several key components that work together to manage the database effectively:

1. **DBMS Engine:** The core service that handles data storage, retrieval, and modification. It interacts directly with the hardware to execute queries and manage data.
2. **Database Schema:** Defines the structure of the database, including tables, columns, relationships, and constraints.
3. **Query Processor:** Interprets and executes SQL queries. It breaks down queries and passes them to the DBMS engine for processing.
4. **Database Manager:** Responsible for managing the database's internal operations such as locking, concurrency control, and transaction management.
5. **Data Dictionary:** Contains metadata about the structure of the database, including definitions of tables, views, columns, etc.
6. **Transaction Manager:** Ensures that transactions are processed reliably, managing concurrency and maintaining data integrity.
7. **Security Manager:** Manages user access, authentication, and permissions to secure data and maintain privacy.
8. **Backup and Recovery Manager:** Ensures that data is regularly backed up and provides recovery tools in case of failure or corruption.
9. **Interface/User Interface:** Allows users to interact with the DBMS through a graphical interface or command-line interface.
---
---
### 33. What is Constraint? Types of Constraints.

A **constraint** is a rule or restriction applied to a column or a table to ensure data integrity and accuracy in a database.

#### Types of Constraints:

1. **NOT NULL:** Ensures that a column cannot have a NULL value.
    - Example: `CREATE TABLE Employees (EmployeeID INT NOT NULL, Name VARCHAR(50));`
2. **PRIMARY KEY:** Uniquely identifies each record in a table. It combines **NOT NULL** and **UNIQUE** constraints.
    - Example: `CREATE TABLE Employees (EmployeeID INT PRIMARY KEY, Name VARCHAR(50));`
3. **FOREIGN KEY:** Establishes a relationship between columns in two tables. It ensures that the value in the column matches a value in another table’s primary key.
    - Example: `CREATE TABLE Orders (OrderID INT, EmployeeID INT, FOREIGN KEY (EmployeeID) REFERENCES Employees(EmployeeID));`
4. **UNIQUE:** Ensures that all values in a column are unique, but unlike primary key, it allows NULL values.
    - Example: `CREATE TABLE Employees (EmployeeID INT UNIQUE, Name VARCHAR(50));`
5. **CHECK:** Ensures that the values in a column satisfy a specific condition.
    - Example: `CREATE TABLE Employees (EmployeeID INT, Age INT CHECK (Age >= 18));`
6. **DEFAULT:** Provides a default value for a column when no value is specified.
    - Example: `CREATE TABLE Employees (EmployeeID INT, Status VARCHAR(10) DEFAULT 'Active');`
7. **INDEX:** Improves the speed of data retrieval operations on a table by creating an index on one or more columns.
    - Example: `CREATE INDEX idx_emp_name ON Employees(Name);`
---
---
### 34. Group by and Having Clause in SQL.

The `GROUP BY` and `HAVING` clauses in SQL are used together to group rows that have the same values in specified columns and filter the results of aggregate functions.

1. **GROUP BY:** Groups rows that have the same values into summary rows (e.g., sum, average).    
    - Example:
        ```sql
        SELECT Department, COUNT(EmployeeID)
        FROM Employees
        GROUP BY Department;
        ```
        
2. **HAVING:** Used to filter groups created by the `GROUP BY` clause. It is similar to the `WHERE` clause but applies to groups rather than individual rows.
    - Example:
        ```sql
        SELECT Department, COUNT(EmployeeID)
        FROM Employees
        GROUP BY Department
        HAVING COUNT(EmployeeID) > 10;
        ```
The `HAVING` clause is used to filter the results of aggregate functions like `COUNT()`, `SUM()`, etc., after grouping the data.


---
---
### 35. What is the Difference Between GRANT and REVOKE in SQL?

In SQL, **GRANT** and **REVOKE** are used to manage permissions on database objects.

1. **GRANT:** The `GRANT` statement is used to give specific privileges (like SELECT, INSERT, UPDATE) to a user or role for a database object.
    - Example:
        ```sql
        GRANT SELECT, INSERT ON Employees TO User1;
        ```
        
2. **REVOKE:** The `REVOKE` statement is used to remove or revoke previously granted privileges from a user or role.
    - Example:
        ```sql
        REVOKE SELECT, INSERT ON Employees FROM User1;
        ```

In summary:
- **GRANT** allows a user to perform specific actions on database objects.
- **REVOKE** removes previously granted permissions, limiting the user’s ability to perform those actions.
---
---
