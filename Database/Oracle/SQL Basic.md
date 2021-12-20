---
id: 1639963730543
title: SQL Basic
category: Database/Oracle/
---

1. Search table FK
```
SELECT * from USER_CONS_COLUMNS
WHERE CONSTRAINT_NAME = 'SYS_C0055084868';
```
2. Select all object
```
select *
from all_objects 
where object_name like 'MV_KOKYAKU_SEARCH_INDEX_PUT_PK';
```
3. Kill session
```
select *
from
   v$session     t1, 
   v$transaction t2
where
   t1.saddr = t2.ses_addr;
```
```
ALTER SYSTEM KILL SESSION 'sid#,serial#';
```

4. Set format date
```
ALTER SESSION SET NLS_DATE_FORMAT = 'YYYY/MM/DD HH24:MI:SS';
```
```
select sysdate from dual; 
```
5. Ignore oracle paramater
```
set define off
```