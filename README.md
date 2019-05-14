
add class MysqlRow and class MySQLCursorMysqlRow

example

#!/usr/bin/env python
# coding=utf-8

import mylib.mysql.connector as mysql

conn = mysql.connect(host='localhost', user='root',passwd='admin',db='test',charset='utf8')

c = conn.cursor(mysqlrow=True)

c.execute("SELECT name,age FROM student;")

for row in c.fetchall():
    print row[1]
    print row["name"]
