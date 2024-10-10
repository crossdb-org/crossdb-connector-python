# Python Driver for CrossDB

## Pre-requirement
You need to [install](https://crossdb.org/get-started/install/) crossdb lib first 

## Import

It's a single python file lib, you can just include in your project folder and import directly, or you can install to python.

```
python setup.py install
```

## Example
```python
import crossdb

conn = crossdb.connect(database=":memory:")
cursor = conn.cursor()
cursor.execute("CREATE TABLE student (name CHAR(16), age INT, class CHAR(16))")
cursor.execute("INSERT INTO student (name,age,class) VALUES ('jack',10,'3-1'), ('tom',11,'2-5')")
cursor.execute("SELECT * from student")
for row in cursor:
	print (row)
```
