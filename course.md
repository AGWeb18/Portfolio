---
title: Transforming Data
---
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
