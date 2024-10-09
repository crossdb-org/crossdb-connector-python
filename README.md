# Python Connector for CrossDB

Install
```
python setup.py install
```

Example
```
import crossdb

conn = crossdb.connect(database=":memory:")
cursor = conn.cursor()
cursor.execute("CREATE TABLE student (name CHAR(16), age INT, class CHAR(16))")
cursor.execute("INSERT INTO student (name,age,class) VALUES ('jack',10,'3-1'), ('tom',11,'2-5')")
cursor.execute("SELECT * from student")
for row in cursor:
	print (row)
```
