---
title: Data Analytic Tools for Business Decision Making
---


# Interactive Lessons
__Week 1:__ The overall objective of this class is to provide students with practical experience in handling the tools required in a Data Science project. One of the most common requirements of Data Scientists is that they have an understanding of `SQL` and relational databases. Understanding the difference between data types, how to provide 'permission' levels based on different users and to easily import any dataset into a SQL Table are all critical skills for a Data Scientist. Although databases are typically managed by a Database Analyst in the real-world, a Data Scientist will be intimately involved with the database and therefore, should be comfortable around them. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/e1LPfehYSgg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

--- 

__Week 2:__ Following up on this lesson, we move into the realm of transforming data - which is often the role that a Data Scientist becomes heavily involved in. Tools such as `pandas` and `numpy` will become increasingly important as they make the lives of Data Scientists much easier. We will discuss concepts around manipulation of data, including best practices, optimizing for-loops, data chunking and more. 


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
