---
title: Data Analytic Tools for Business Decision Making
---


# Interactive Lessons
# Week 3: 

The overall objective of this class is to provide students with practical experience in handling the tools required in a Data Science project. One of the most common requirements of Data Scientists is that they have an understanding of **`SQL`** and **`relational databases`**. Understanding the difference between data types, how to provide 'permission' levels based on different users and to easily import any dataset into a SQL Table are all critical skills for a Data Scientist. Although databases are typically managed by a Database Analyst in the real-world, a Data Scientist will be intimately involved with the database and therefore, should be comfortable around them. 

### Short video on Getting Started with MySQL
<iframe width="560" height="315" src="https://www.youtube.com/embed/e1LPfehYSgg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


### Steps to Create a SCHEMA/TABLE

1. Install [MySQL Server + Workbench](https://dev.mysql.com/downloads/installer/) 
2. Create a SCHEMA 
3. Create a TABLE  
4. Import data through Workbench


### MySQL Data Type Cheat Sheet
#### Numeric

| Data Type  | Definition |  
| ------- | ------- |
| TINYINT  | A very small integer |
| SMALLINT  | A small integer |
| MEDIUMINT  | A medium-sized integer |
| INT  | A standard integer |
| BIGINT  | A large integer |
| DECIMAL  | A fixed-point number |
| FLOAT  | A number with decimals, single precision |
| DOUBLE  | A number with decimals, double precision |
| BIT  | A bit field |
 
 
#### String

| Data Type  | Definition  |
|---|---|
| CHAR  | A fixed-length string  |
| VARCHAR  | A variable-length string  |
| BINARY  | A fixed-length binary string  |
| BLOB  | A small BLOB (binary large object)  |
| TINYTEXT  | A very small non-binary string  |
| TEXT  | A small binary string  |
| ENUM  | enumeration, each column value is assigned an enum  |


#### Date/Other

| Data Type  | Definition  |
|---|---|
| DATE  | A date value `YYYY-MM-DD` format  |
| TIME  | A time value: `hh:mm:ss` format  |
| DATETIME  | A date/time value: `YYYY-MM-DD hh:mm:ss` format  |
| TIMESTAMP  | A timestamp: ` YYYY-MM-DD hh:mm:ss ` format  |
| TINYTEXT  | A very small non-binary string  |
| YEAR  | A year value: `YYYY` or `YY` format  |
| BOOL/TINYINT  | MySQL does not have BOOL or BOOLEAN built-in, TINYINT(1) is used.  |




--- 

# Week 4 

Following up on this lesson, we move into the realm of transforming data - which is often the role that a Data Scientist becomes heavily involved in. Tools such as `pandas` and `numpy` will become increasingly important as they make the lives of Data Scientists much easier. We will discuss concepts around manipulation of data, including best practices, optimizing for-loops, data chunking and more. 


First, let's talk about extracting data out of your MySQL database: 

## PyMySQL - `create_engine` Snippet

The snippet below covers the steps involved to create an engine. The engine is what you `execute` queries on. 

We will walk through some practical examples: 

```python
import pymysql
from sqlalchemy import create_engine

user = 'yourUserName'
passw = 'password'
host =  'hostName'  # either localhost or ip e.g. '172.17.0.2' or hostname address 
port = 3306 
database = 'dataBaseName'

mydb = create_engine('mysql+pymysql://' + user + ':' + passw + '@' + host + ':' + str(port) + '/' + database , echo=False)
```
