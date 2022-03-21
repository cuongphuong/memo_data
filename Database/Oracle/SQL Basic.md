---
id: 1647840992144
title: SQL Basic
category: Database/Oracle/
---

1. Search table FK
```sql
SELECT * from USER_CONS_COLUMNS
WHERE CONSTRAINT_NAME = 'SYS_C0055084868';
```
2. Select all object
```sql
select *
from all_objects 
where object_name like 'SEARCH_INDEX_PUT_PK';
```
3. Kill session
```sql
select *
from
   v$session     t1, 
   v$transaction t2
where
   t1.saddr = t2.ses_addr;
```

```sql
ALTER SYSTEM KILL SESSION 'sid#,serial#';
```

4. Set format date
```sql
ALTER SESSION SET NLS_DATE_FORMAT = 'YYYY/MM/DD HH24:MI:SS';
```

```
select sysdate from dual; 
```
5. Ignore oracle paramater
```
set define off
```

6. Set default schema Oracle
```
ALTER SESSION SET CURRENT_SCHEMA=DEVLPMT;
```
7. Xem View có trong table và sql tạo view

```sql
SELECT * FROM USER_VIEWS;
```
8. Xem matterial view:

```sql
SELECT * FROM USER_MVIEWS;
```
9. Xem dblink:

```
SELECT * FROM DBA_DB_LINKS;
```
10. Refresh matterial view:
```
EXEC DBMS_MVIEW.refresh('VIEW_NAME');
```
11. View thông tin table trong schema

```
select * from all_objects where object_name like '%PUSH_NOTIFICATION%';"
```
12. Xem cấu trúc table

```
DESC TABLE_NAME;
```
