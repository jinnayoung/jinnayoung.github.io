---
title: "'as of timestamp' SQL"
tag: 
    - oracle 
    - sql
---
Starting in Oracle9i R2, the AS OF timestamp clause has been added to the SELECT statement to enable flashback query on a specific table or set of tables. Developers are able to specify the AS OF clause for a single-table, multiple-tables (joins) as well as specify different times for different tables. The AS OF timestamp clause can also be used inside INSERT or CREATE TABLE AS SELECT statements.


Oracle flashback has an 'as of timestamp' WHERE clause to allow point-in-time SQL queries:


> create table [new_table_name] as
> select * from  [old_table_name]
> as of timestamp to_timestamp('20190131 13:30:00','yyyyMMdd hh24:mi:ss')

