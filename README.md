# Database:
* A Data base is an organized collection of structured information, or data, typically stored electronically in a computer system.
* Example: The Oracle, MySQL, MS SQL Server, postgresql, MongoDB.
## SQL:
* SQL stands for Structured Query Language.
* SQL is used to communicate with a database.
## SQLite3:
* The SQLite3 module is a Python standard library. It lets us work with SQL database without installing any additional software.
* To perform any SQL related operation in Python we use SQLite3 module/library.
## Benifits of SQL for Data Analysis
* SQL for Data Analysis is a powerful programming language that helps data analysts interact with data stored in Relational databases. By using SQL several companies have built their proprietary tools to fetch information from databases quickly.
* This data-driven approach has enabled the industry to channel its growth by analyzing meaningful information to make critical business decissions. Data Analysis has played a vital role in identifying trends and patterns as orginizations forecast their business goals by extracting their historical data in databases.
# SQLite3 Topics:
## Connecting to the Database
* Connecting to the SQLite Database can be established using the connect() method, passing the name of the database to be accessed as a parameter.
## Defining a function to read queries
```
def read(query):
    return pd.read_sql_query(query, connection)
```
## The Schema Table
* Every SQLite database contains a single "schema table" that stores the schema for that database. The schema for a database is a description of all of the other tables, indexes, triggers, and views that are contained within the database
* It contains one row for each table, index, view, and trigger (collectively "objects") in the schema, except there is no entry for the sqlite_schema table itself.
* The schema table can always be referenced using the name "sqlite_schema"
## Select Data from Table
* Select statement is used to retrieve data from an SQLite table and this returns the data contained in the table.
## Column Alias
* You can rename a table or a column temporarily by giving another name, which is known as ALIAS
* The use of table aliases means to rename a table in a particular SQLite statement
* Renaming is a temporary change and the actual table name does not change in the database
* The column aliases are used to rename a table's columns for the purpose of a particular SQLite query
## Aggregate functions
* An aggregate function is a function that groups the values of numerous rows into a single summary value
* SQLite provides us with many aggregate functions used for statistical analysis
* AVG (i.e., arithmetic mean), SUM, MAX, MIN, COUNT are common aggregation functions
## Subquery
* A subquery is a SQL query nested inside a larger query
  * For emample: SELECT statement nested in another statement
* You must use a pair of parentheses to enclose a subquery
* Typically, a subquery returns a single row as an atomic value, though it may return multiple rows for comparing values with the IN operator
* You can use a subquery in the SELECT, FROM, WHERE, and JOIN clauses
## Operators:
* ### Comparison Operators
    * == Checks if the values of two operands are equal or not, if yes then the condition becomes true
    * != Checks if the values of two operands are equal or not, if the values are not equal, then the condition becomes true
    * <> Checks if the values of two operands are equal or not, if the values are not equal, then the condition becomes true.
    * etc.
* ### Logical Operators
    * AND - The AND operator allows the existence of multiple conditions in an SQL statement's WHERE clause
    * BETWEEN - The BETWEEN operator is used to search for values that are within a set of values, given the minimum value and the maximum value
    * IN - The IN operator is used to compare a value to a list of literal values that have been specified
    * OR - The OR operator is used to combine multiple conditions in an SQL statement's WHERE clause
    * UNIQUE - The UNIQUE operator searches every row of a specified table for uniqueness (no duplicates)
    * etc.
* ### Arithmetic Operators
    * "+" - Adds the values present on both sides of the operator
    * "–" - Subtracts the right hand operand from left hand operand.
    * "*" - Multiplies the values of both sides.
    * "/" - Divides the left hand operand by right hand operand.
    * "%" - Divides the left hand operand by right hand operand and returns the remainder.
## Clauses:
* ### WHERE Clause
    * Where clause is used in order to make our search results more specific, using the where clause in SQL/SQLite we can go ahead and specify specific conditions that have to be met when retrieving data from the database.
    * If we want to retrieve, update or delete a particular set of data we can use the where clause. If we don’t have condition matching values in your database tables we probably didn’t get anything returned.
* ### ORDER BY Clause
    * The ORDER BY statement is a SQL statement that is used to sort the data in either ascending or descending according to one or more columns. By default, ORDER BY sorts the data in ascending order.
    * DESC is used to sort the data in descending order.
    * ASC to sort in ascending order.
* ### LIMIT Clause
    * LIMIT keyword is used to limit the data given by the SELECT statement
    * If there are many tuples satisfying the query conditions, it might be resourceful to view only a handful of them at a time
* ### GROUP BY clause
    * The GROUP BY clause is an optional clause of the SELECT statement. The GROUP BY clause a selected group of rows into summary rows by values of one or more columns
    * The GROUP BY clause returns one row for each group. For each group, you can apply an aggregate function such as MIN, MAX, SUM, COUNT, or AVG to provide more information about each group
* ### HAVING clause
    * SQLite HAVING clause is an optional clause of the SELECT statement. The HAVING clause specifies a search condition for a group
    * You often use the HAVING clause with the GROUP BY clause. The GROUP BY clause groups a set of rows into a set of summary rows or groups. Then the HAVING clause filters groups based on a specified condition
    * If you use the HAVING clause, you must include the GROUP BY clause; otherwise, you will get the error
* ### Join Clause
    * A JOIN clause combines the records from two tables on the basis of common attributes.
    * The different types of joins are as follows:
      * INNER JOIN (OR JOIN) – Gives the records that have common attributes in both tables.
      * LEFT JOIN – Gives all records from the left table and only the common records from the right table.
      * RIGHT JOIN – Gives all records from the right table and only the common records from the left table.
      * FULL OUTER JOIN – Gives all records when there is a common attribute in either the left or the right table.
      * CROSS JOIN – Gives records of one table with all other records of another table.

