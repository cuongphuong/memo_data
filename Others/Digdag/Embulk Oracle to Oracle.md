---
id: 1640665146054
title: Embulk Oracle to Oracle
category: Others/Digdag/
---


> Import data từ oracle sang oracle sử dụng embulk



***wfl.dig***
```
timezone: Asia/Tokyo

_export:
  workflow_name: "test"
  oracle_driver: ${env.oracle_driver}

+load1:
  _export:
    src_oracle_host: "localhost"
    src_oracle_sid: "xxx"
    src_oracle_user: "xxx"
    src_oracle_pass: "xxx"
    src_oracle_table: "table_name"
  +exe_load1:
    sh>: embulk run yml/test_import.yml.liquid
```
***test_import.yml.liquid***

```
exec:
  min_output_tasks: 1

in:
  type: oracle
  driver_path: {{ env.oracle_driver }}
  url: jdbc:oracle:thin:@//{{ env.src_oracle_host }}/{{ env.src_oracle_sid }}
  user: {{ env.src_oracle_user }}
  password: {{ env.src_oracle_pass }}
  select: "*"
  table: {{ env.src_oracle_table }}
  where: "SYSDATE - CREATED_AT <= 30"
  options: {useLegacyDatetimeCode: false, serverTimezone: Asia/Tokyo}
  default_timezone: Asia/Tokyo
  column_options:
    STRING_FIELD: { type: string }
    NUMBER_FIELD: { type: long }
    DATE_FIELD: { type: string, timestamp_format: "%Y-%m-%d %H:%M:%S", timezone: "+0900" }

out:
  type: oracle
  driver_path: {{ env.oracle_driver }}
  url: jdbc:oracle:thin:@//yyy/yyy
  user: yyy
  password: yyy
  schema: yyy
  table: des_table_name
  default_timezone: Asia/Tokyo
  mode: truncate_insert
  insert_method: direct
  column_options:
    STRING_FIELD: {value_type: string, type: 'CHAR(13)'}
    NUMBER_FIELD: {value_type: string, type: 'NUMBER'}
    DATE_FIELD: { value_type: timestamp,  type: 'DATE' }
```
