# Databases and SQL
## Introduction to databases

- **Database**:
	- An organized collection of information or data.

- **Spreadsheets:**
	- Designed for a single user or a small team.
	- Store less data.

- **Databases:**
	- Accessed by multiple people simultaneously.
	- Store massive amounts of data.
	- Perform complex tasks while accessing data.

- **Relational database:**
	- A structured database containing tables that are related to each other.

- **Primary key:**
	- A column where every row has a unique entry.

- **Foreign key:**
	- A column in a table that is a primary key in another table.

---
## Query databases with SQL

- **SQL (Structured Query Language):**
	- A programming language used to create, interact with, and request information from a database.

- **Query:**
	- A request for data from a database table or a combination of tables.

- **Log:**
	- A record of events that occur within an organization's systems.

---
## SQL Filtering vs. Linux Filtering

### Accessing SQL from Linux

- Use the Linux command line to access SQL by typing the command for the specific SQL version (e.g., `sqlite3` for SQLite).
- Once in the SQL environment, commands typed will be interpreted as SQL commands.

### Differences between Linux and SQL Filtering

#### Purpose

- **Linux Filtering:**
  - Manages files and directories on a computer system.
  - Used for searching specific files, manipulating file permissions, managing processes.
- **SQL Filtering:**
  - Filters data within a database management system.
  - Queries and manipulates data stored in tables.

#### Syntax

- **Linux Filtering:**
  - Uses various commands and command-line options.
  - Examples: `find`, `sed`, `cut`, `grep`.
- **SQL Filtering:**
  - Uses Structured Query Language (SQL) with standardized keywords and clauses.
  - Examples: `SELECT`, `WHERE`, `JOIN`.

#### Structure

- **Linux:**
  - More free-form; data is printed as lines of text.
  - Less organized; harder to manipulate specific parts of data.
- **SQL:**
  - Organized structure; data is separated into columns and rows within tables.
  - Easier to analyze and manipulate specific parts of data efficiently.

#### Joining Tables

- **Linux:**
  - Does not directly join data from different sources or files.
  - Requires manual scripting to combine outputs.
- **SQL:**
  - Supports joining multiple tables using `JOIN` clauses.
  - Allows for comprehensive and relational data analysis.

#### Best Uses

- **Linux Filtering:**
  - Ideal for data stored in text files or logs not in a database format.
  - Useful for system administration tasks and quick, file-based data searches and manipulations.
- **SQL Filtering:**
  - Best for structured data stored in databases.
  - Excels in complex queries requiring data from multiple related tables.

#### Practical Implications for Security Analysts

- **SQL:**
  - Use for structured data in databases.
  - Efficient querying, filtering, and joining of related data.
- **Linux Filtering:**
  - Essential for unstructured data in files (e.g., system logs, configuration files).
  - Quick search, filter, and manipulation of files.

### Key Takeaways

- **Linux Filtering:**
  - Focuses on file and directory management with a less structured approach.
- **SQL Filtering:**
  - Concentrates on structured data manipulation within databases.
  - Provides organized data handling and ability to join tables.
- **Choosing the Right Tool:**
  - Depends on the data format and task requirements.
  - Both tools are complementary in data and security analysis.

---
## Querying a Database

### Basic SQL Query

- **Essential Keywords:** `SELECT` and `FROM`.
  - **SELECT:** Indicates which columns to return.
  - **FROM:** Indicates which table to query.

#### Example Query

```sql
SELECT employee_id, device_id
FROM employees;
```

### Chinook Database

- Used in this course for queries in readings and quizzes.
- Simulates data from a digital media company.
- Contains eleven tables including `employees`, `customers`, and `invoices`.

#### Example Query on Customers Table

```sql
SELECT customerid, city, country
FROM customers;
```

### SELECT Keyword

- **Single Column:**

	```sql
	SELECT customerid
	```

- **Multiple Columns:**

	```sql
	SELECT customerid, city
	```

- **All Columns:**

	```sql
	SELECT *
	```

### FROM Keyword

- Indicates the table to query.
- **Example:**

	```sql
	SELECT *
	FROM customers;
	```

### ORDER BY Keyword

- Organizes the data extracted from a table.
- Can be used for ascending or descending order.

#### Sorting in Ascending Order

- **Example:**

	```sql
	SELECT customerid, city, country
	FROM customers
	ORDER BY city;
	```

#### Sorting in Descending Order

- **Example**

	```sql
	SELECT customerid, city, country
	FROM customers
	ORDER BY city DESC;
	```

#### Sorting Based on Multiple Columns

- **Example:**

	```sql
	SELECT customerid, city, country
	FROM customers
	ORDER BY country, city;
	```

### Key Takeaways

- **SELECT and FROM:** Indicate which columns to return and which table to query.
- **ORDER BY:** Used to organize the output of the query.
- Foundational SQL skills are essential for more advanced queries.

---
## The WHERE Clause and Basic Operators

### How Filtering Helps

- As a security analyst, filtering is essential for managing large and complicated security logs.
- Examples of filtering use cases:
  - Finding login attempts by a specific user.
  - Identifying login attempts during a security issue.
  - Finding devices running a specific version of an application.

### WHERE Clause

- **Purpose:** Indicates the condition for a filter in an SQL query.
- **Example:** 

  ```sql
  SELECT firstname, lastname, title, email
  FROM employees
  WHERE title = 'IT Staff';
	```

### Filtering for Patterns

- **Key Elements:**
    - Wildcards
    - LIKE operator

#### Wildcards

- **Percentage Sign (%):** Substitutes for any number of characters.
- **Underscore (_):** Substitutes for one character.

#### Pattern Examples

|Pattern|Results that could be returned|
|---|---|
|`a%`|apple123, art, a|
|`a_`|as, an, a7|
|`a__`|ant, add, a1c|
|`%a`|pizza, Z6ra, a|
|`_a`|ma, 1a, Ha|
|`%a%`|Again, back, a|
|`_a_`|Car, ban, ea7|

### LIKE Operator

- **Purpose:** Used with WHERE to search for a pattern in a column.    
- **Example:**

	```sql
	SELECT lastname, firstname, title, email
	FROM employees
	WHERE title LIKE 'IT%';
	```

- **Example with Underscore:**

	```sql
	SELECT firstname, lastname, state, country
	FROM customers
	WHERE state LIKE 'N_';
	```

### Key Takeaways

- **Filters:** Crucial for refining query results.
- **WHERE Clause:** Essential for adding filters to queries.
- **LIKE Operator and Wildcards:** Useful for pattern-based filtering using `%` and `_`.

### Additional Examples

#### Filtering by Specific Title

- **Query:**
 
	```sql
	SELECT firstname, lastname, title, email
	FROM employees
	WHERE title = 'IT Staff';
	```

#### Filtering Titles Starting with 'IT'

- **Query:**

	```sql
	SELECT lastname, firstname, title, email
	FROM employees
	WHERE title LIKE 'IT%';
	```

#### Filtering States with Pattern 'N_'

- **Query:**

	```sql
	SELECT firstname, lastname, state, country
	FROM customers
	WHERE state LIKE 'N_';
	```

---
## Operators for Filtering Dates and Numbers

### Common data types

- String
- Numeric
- Date and time

### Numbers, Dates, and Times in Cybersecurity

- Security analysts work with various types of data:
  - **Numeric Data:** 
    - Number of login attempts
    - Count of a specific type of log entry
    - Volume of data sent from a source
    - Volume of data sent to a destination
  - **Date and Time Data:**
    - Timestamps on logs
    - Login dates and times
    - Dates for patches
    - Duration of connections

### Comparison Operators

- Used in SQL to filter numeric and date/time data.
- **Operators:**

| Operator | Use                        |
| -------- | -------------------------- |
| `<`      | less than                  |
| `>`      | greater than               |
| `=`      | equal to                   |
| `<=`     | less than or equal to      |
| `>=`     | greater than or equal to   |
| `<>`     | not equal to               |
| `!=`     | not equal to (alternative) |

### Incorporating Operators into Filters

- Comparison operators are used in the WHERE clause.
- **Example:**
  ```sql
  SELECT firstname, lastname, birthdate
  FROM employees
  WHERE birthdate > '1970-01-01';
	```
- This query returns employees born after January 1, 1970.
- **Note:**
    - `>` is exclusive (does not include '1970-01-01').
    - `>=` is inclusive (includes '1970-01-01').

### BETWEEN Operator

- Used for filtering within a range.
- **Example:**
	```sql
	SELECT firstname, lastname, hiredate
	FROM employees
	WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
	```
- This query returns employees hired between January 1, 2002, and January 1, 2003.
- **Note:**
	 - `BETWEEN` is inclusive (includes '2002-01-01' and '2003-01-01').

### Key Takeaways

- **Operators:** Important for filtering numeric and date/time data.
    - Exclusive operators: `<`, `>`.
    - Inclusive operators: `<=`, `>=`.
- **BETWEEN Operator:** Helps filter data within a specific range inclusively.

### Additional Examples
#### Filtering Birthdates After a Certain Date

- **Query:**

	```sql
	SELECT firstname, lastname, birthdate
	FROM employees
	WHERE birthdate > '1970-01-01';
	```

#### Filtering Hire Dates Within a Range

- **Query:**

	```sql
	SELECT firstname, lastname, hiredate
	FROM employees
	WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
	```

---
## More on Filters with AND, OR, and NOT

### Logical Operators

- **AND, OR, and NOT** allow you to filter your queries to return specific information.
- These are considered logical operators.

### AND

- **Purpose:** Filters on two conditions, both of which must be met simultaneously.
- **Example:**
  ```sql
  SELECT firstname, lastname, email, country, supportrepid
  FROM customers
  WHERE supportrepid = 5 AND country = 'USA';
	```

- This query returns customers handled by support representative with ID 5 and located in the USA.

### OR

- **Purpose:** Filters on two conditions, where either one or both conditions can be met.
- **Example:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE country = 'Canada' OR country = 'USA';
	```
- This query returns customers in either Canada or the USA.

### NOT

- **Purpose:** Negates a single condition, returning records that do not match the specified condition.
- **Example:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE NOT country = 'USA';
	```
- This query returns customers who are not from the USA.
- **Pro tip:**
    - Alternative ways to use NOT:
		```sql
		WHERE country <> 'USA'
		WHERE country != 'USA'
		```

### Combining Logical Operators

- **Purpose:** Combine logical operators to create more specific filters.
- **Example:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE NOT country = 'Canada' AND NOT country = 'USA';
	```
- This query returns customers in all countries except Canada and the USA.

### Key Takeaways

- **AND Operator:** Requires two conditions to be true simultaneously.
- **OR Operator:** Requires either one or both conditions to be true.
- **NOT Operator:** Negates a condition, returning records that do not match the condition.
- Logical operators can be combined to create even more specific queries.

### Additional Examples

#### Filtering for Specific Conditions with AND

- **Query:**
	```sql
	SELECT firstname, lastname, email, country, supportrepid
	FROM customers
	WHERE supportrepid = 5 AND country = 'USA';
	```
#### Filtering with OR for Multiple Conditions

- **Query:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE country = 'Canada' OR country = 'USA';
	```

#### Negating a Condition with NOT

- **Query:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE NOT country = 'USA';
	```

#### Combining NOT with AND for Multiple Conditions

- **Query:**
	```sql
	SELECT firstname, lastname, email, country
	FROM customers
	WHERE NOT country = 'Canada' AND NOT country = 'USA';
	```

---
## Compare Types of Joins

### Inner Joins
- INNER JOIN returns rows matching on a specified column that exists in more than one table.
- It only returns the rows where there is a match.
- Returns all specified columns from all joined tables.
  - Note: If a column exists in both tables, it is returned twice when `SELECT *` is used.

#### Syntax of an Inner Join

```sql
SELECT *
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```
- Specify the two tables to join:
    - First table after `FROM`
    - Second table after `INNER JOIN`
- Use the `ON` keyword and the `=` operator to indicate the column to join on.
    - Specify both table and column names (`table.column`).

#### Selecting Specific Columns

```sql
SELECT username, operating_system, employees.device_id
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```
- Columns only in one table are written with just the column name.
- Columns in both tables need both table and column name.

### Outer Joins

- Outer joins expand what is returned from a join.
- Each type of outer join returns all rows from either one table or both tables.

#### Left Joins

- LEFT JOIN returns all the records of the first table, but only matching rows from the second table.

![Venn diagram of Left Join](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/GsYCwSiOSMmymUqPUAQJ5w_5beed7e470c546fca088a83dfd9465f1_CS_R-080_Left-joins.png?expiry=1716249600000&hmac=EsPKgWlr5MeRX3MCPPFeYQOcTCItgnc7otPsTUhLXQs)

#### Syntax of a Left Join

```sql
SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;
```

- Specify the first table after `FROM` and the second table after `LEFT JOIN`.

#### Right Joins

- RIGHT JOIN returns all the records of the second table, but only matching rows from the first table.

![Venn diagram of Right Join](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/YHXRMOLiQheppUjthmM5yQ_cfb18a8315e34357bd1299f7eefafcf1_CS_R-080_Right-joins.png?expiry=1716249600000&hmac=5OEOpEUIVwW2RQ_bkCrwBV6qHuNz5bH78hR865yWz4A)

#### Syntax of a Right Join

```sql
SELECT *
FROM employees
RIGHT JOIN machines ON employees.device_id = machines.device_id;
```
- Same syntax as LEFT JOIN, with `RIGHT JOIN` instead of `LEFT JOIN`.

#### Left Join and Right Join Equivalence

- LEFT JOIN and RIGHT JOIN can return the same results if tables are swapped.
	```sql
	SELECT *
	FROM machines
	RIGHT JOIN employees ON employees.device_id = machines.device_id;
	```
- Swap the order of tables before and after the join keyword to switch between left and right joins.

#### Full Outer Joins

- FULL OUTER JOIN returns all records from both tables.
- Merges two tables completely.

![Venn diagram of Full Outer Join](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oRzF__GaTqSGMmUqXKbSrQ_92db9841a00244c2aa214e60bb07f1f1_CS_R-080_FULL-OUTER-JOIN.png?expiry=1716249600000&hmac=Wq-gODxbFc-Na2phzIfsSDPsn5riFt3G6fnr7bwR4wU)

#### Syntax of a Full Outer Join

```sql
SELECT *
FROM employees
FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
```
- Includes all records from both tables.
- Order of tables does not change the results.

### Key Takeaways

- INNER JOIN returns only the matching records.
- LEFT JOIN returns all records from the first (left) table and matching records from the second (right) table.
- RIGHT JOIN returns all records from the second (right) table and matching records from the first (left) table.
- FULL OUTER JOIN returns all records from both tables.

---
## Continuous Learning in SQL

### Aggregate Functions
- Aggregate functions perform calculations over multiple data points and return the result.
- Examples include:
  - COUNT: Returns the number of rows returned from a query.
  - AVG: Returns the average of numerical data in a column.
  - SUM: Returns the sum of numerical data in a column.
- Syntax: Place the aggregate function after SELECT, followed by the column name in parentheses.

#### Aggregate Function Syntax
- Example of using COUNT function to count the number of records in a column.

	```sql
	SELECT COUNT(firstname)
	FROM customers;
	```

- Example of using COUNT function with a filter to count records based on a condition.

	```sql
	SELECT COUNT(firstname)
	FROM customers
	WHERE country = 'USA';
	```

### Continuing to Learn SQL

- SQL is widely used and has many applications beyond basic querying.
- Approach new tasks with curiosity and a willingness to learn.
- Look for accurate and easy-to-follow resources online to extend your knowledge.
- Practice with real databases to gain practical experience.

#### Key Takeaways

- Aggregate functions like COUNT, SUM, and AVG allow for new ways of working with SQL.
- Continuously exploring SQL on your own can expand your capabilities as an analyst in a cybersecurity context.

---
## **Cybersecurity Terms and Concepts**

| Term                            | Definition                                                                                    |
| ------------------------------- | --------------------------------------------------------------------------------------------- |
| Database                        | An organized collection of information or data                                                |
| Date and time data              | Data representing a date and/or time                                                          |
| Exclusive operator              | An operator that does not include the value of comparison                                     |
| Filtering                       | Selecting data that match a certain condition                                                 |
| Foreign key                     | A column in a table that is a primary key in another table                                    |
| Inclusive operator              | An operator that includes the value of comparison                                             |
| Log                             | A record of events that occur within an organization's systems                                |
| Numeric data                    | Data consisting of numbers                                                                    |
| Operator                        | A symbol or keyword that represents an operation                                              |
| Primary key                     | A column where every row has a unique entry                                                   |
| Query                           | A request for data from a database table or a combination of tables                           |
| Relational database             | A structured database containing tables that are related to each other                        |
| String data                     | Data consisting of an ordered sequence of characters                                          |
| SQL (Structured Query Language) | A programming language used to create, interact with, and request information from a database |
| Syntax                          | The rules that determine what is correctly structured in a computing language                 |
| Wildcard                        | A special character that can be substituted with any other character                          |

---