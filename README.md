# Database-Systems-for-Data-Science (Fall 2022)
**MS Applied Data Science**

**Instructor:** Dimitri Yatsenko, Ph.D.

**TA:** Juan Gallegos

## Syllabus

Organization concepts and terminology of data models and the underlying data architectures needed to support them. 
Presentation of the relational database management systems including an introduction to SQL programming: relational database design and data queries with integration into application programming languages, with Python used for examples. 

I will assume basic Python proficiency: we want to use databases directly from Python. 

The course will include practical exercises and will be graded based on several indvidual and group projects using real-world datasets.

## Class and attendance

Class participation is required and much of the material will be presented. The class will be held in room Malloy 241 and also broadcast in Zoom.
We will also use a Slack channel. If you have not received access to any of these resources, please notify your instructor.

## Textbook 

The University provided you with a [Safari Books](https://www.oreilly.com) subscription account. Readings, examples, and projects will be selected primarily from the following references:

1. Jan L. Harrington, *Relational Database Design and Implementation*: 4th edition (2016)

  * https://learning.oreilly.com/library/view/relational-database-design/9780128499023/

2. Alan Beaulieu, Learning SQL, 3rd Edition (2020)

  * https://learning.oreilly.com/library/view/learning-sql-3rd/9781492057604/

3. Michael Hernandez, *Database Design for Mere Mortals: A Hands-On Guide to Relational Database Design*; 4th edition (2020).  ISBN-13: 978-0136788041 ISBN-10: 0136788041

  * https://learning.oreilly.com/library/view/database-design-for/9780136788133/

4. Josephine Bush, *Learn SQL Database Programming* (2020)

  * https://learning.oreilly.com/library/view/learn-sql-database/9781838984762/

Additional slides and notes will be provided in class.


## Grading 
10-12 Assignments/Projects

|grade| percent |
|---|---|
|**A** |>=94%|
|**A-**|>=90%|
|**B+**|>=86%|
|**B**|>=82%|
|**B-**|>=78%|
|**C+**|>=74%|
|**C**|>=70%|
|**C-**|>=66%|
|**D+**|>=62%|
|**D**|>=58%|
|**F**|>=0%|


## Weeks 1-2: (Aug 23, Aug 30)
Databases in data science. Data models: diverse ways to think about data: hiearchical, network, relational, object, graph, and document data models.
History of datatabases and database technologies. Next-generation databases.

Database access. Creating SQL tables and inserting data. Simple queries. sqlite and mysql.

Issue SQL queries from Jupyter using SQL Magic.

Issuing SQL queries from Python code using a database client library, (`pymysql`). 

`CREATE SCHEMA`, `CREATE TABLE`, `INSERT`, `DELETE`, `DROP TABLE`, `DROP SCHEMA`. 

Create schemas and tables, insert rows, delete, and drop.

Using the `faker` module to populate tables.

Using `datajoint` as a high-level interface. 

Datatypes: numerical, character strings, and enum. 

### Homework 1 (due Sep 1)
1. [Installation of SQL Magic for Jupyter](https://nbviewer.jupyter.org/github/msds-5315/Database-Systems-for-Data-Science/blob/master/notebooks/Install-SQL-Magic.ipynb)
2. [Connecting to the database from Jupyter](https://nbviewer.jupyter.org/github/msds-5315/Database-Systems-for-Data-Science/blob/master/notebooks/Connect-SQL.ipynb)

2. On the MySQL server, create a database named `<username>_university` and define a table named `person`. Make sure it has a well chosen primary key. 
 * Connect to the database server 
 * Create a schema, a table within it, and insert at least one row. 


### Readings: 
  * Harrington, Chapter 1, "The Database Environment"
  * Hernandez, Chapter 1, "The Relational Database" 
  * Beauliue, Chapter 2: "Creating and Populating a Database"
  * Generating fake data: https://towardsdatascience.com/generating-fake-data-with-python-c7a32c631b2a
1. Create a `university` database 
2. Create a table named `person` with basic attributes: name, date of birth, address, phone, 
3. Insert at least one record into the person table.

### Key terms
Database, database system, database server, data model, data integrity, data consistency, ACID, relational data model, SQL, imperative queries, schema.

### Key skills
* Connect to the MySQL database provided for the class, create a simple table, and insert data into it.
* Issue queries in SQL (using the SQL magic in jupyter for quick SQL scripting) 
* Execute queries with a client library (`pymysql`). Generate fake data. See notebook `Fake-It.ipynb`
* Execute queries using DataJoint. See notebooks `DataJoint-config` and `DataJoint-Intro`.

### Homework 2 (due Sep 8)

1. Answer questions in [Block 1](Block1.md). Submit as a PDF file as a direct message to the TA and the instructor on Slack.  

## Weeks 3-5: (Sep 6, Sep 13, Sep 20)

### Key concepts 

* Data models: structured (schema) and self-desccribing (schema-less). 
* How a database table works. 
* Schema design. Simple queries. Primary key. Foreign keys. Entity integrity. Referential integrity. 
* Normalization. First normal form.  Entity normalization.
* Diagramming. Entity-Relationship Diagrams. DataJoint diagrams. 
* See the `Language` notebook used in Lecture 3.
* Relational algebra: restriction and projection. The structure of the `SELECT` Statement.
* `SELECT ... FROM ... WHERE ... ORDER BY ... LIMIT ...`
* Fetch. Order by. Offset and Limit.
* Declarative queries vs. imperative queries
* Default values. Nullable attributes. Nullable foreign keys.
* UUID, surrogate keys, secondary unique constraints


### Readings:
  * Harrington, Chapters 3-7
  * Hernandez, Chapters 2-3
  * Beaulieu, Chapters 3-4
  * Beaulieu [Appendix A. ER Diagram](https://learning.oreilly.com/library/view/learning-sql-3rd/9781492057604/app01.html)
  * Example databases: https://dev.mysql.com/doc/index-other.html
  * https://www.datajoint.com/blog/2021-09-28-data-needs-direction

[Assignment 3](Assign3.md) -- Due Sep 22 (extended by one week)

### Resources and exercises
* [SimpleQueries](notebooks/SimpleQueries.ipynb)
* http://www.w3resource.com/mysql-exercises/ 
* http://www.w3resource.com/sql-exercises/
* [PersonAccounts](notebooks/PersonAccounts.ipynb)


* [Assignment 4](Assign4.md) -- Due Sep 22
* [Assignment 5](Assign5.md) -- Due Sep 29


## Weeks 6-8 (Sep 27, Oct 4, Oct 11 (Fall Break), Oct 18)

Surrogate keys / Natural keys. 
Indexes, secondary unique keys.
Data serialization - blobs.

Notebooks 
* [Joins](notebooks/Joins.ipynb)
* [GroupBy](notebooks/GroupBy.ipynb)
* [Indexes](notebooks/Indexes.ipynb)
* [Using BLOBS](notebooks/Using-BLOBs.ipynb)
* [Division](notebooks/Relational-Division.ipynb)

Advanced Queries: 

* Subqueries
* Inner Joins: cross join, theta join, equijoin, natural join
* Aggregations 

Reading: Harrington  Chapters 16-19

* [Assignment 6](Assign6.md) -- Due Oct 20 
* [Assignment 7](Assign7.md) -- Due Oct 27 
* [Assignment 8](Assign8.md) -- Due Nov 3

## Weeks 9, 10 (Oct 25, Nov 1, Nov 8)


Modeling relationships: 

* Sequences and workflows.
* Specialization / generalization.
* Hierarchies (ownership, composite keys, partial keys)
* Groupings 
* Directed Graphs (including trees)
* Unidrected Graphs.
* Master-part relationships

Transaction processing.

* [Hotel Database](notebooks/Hotel.ipynb) -- a sample database project solution.

* [Assignment 9](Assign9.md) -- Due Nov 10 

Reading: 

* Harrington: Chapters 13, 14, 15 (case studies), 22 (concurrency and transactions)


## Weeks 10-11 (Nov 15, Nov 22):
Putting it all together. Practical examples

* [Final](Final.md) -- Due Dec 12 

Practice projects. Final Project
