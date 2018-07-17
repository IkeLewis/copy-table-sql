copy-table-sql
==============

Copy text tables produced by SQL queries as various types of formatted
text, e.g. markdown, org, etc.  Currently, only query results for db2
tables are supported and may be converted to ORG tables or (GitHub
flavored) markdown tables.

Installation
------------

Simply place the path to copy-table-sql in you load path and `(require
'copy-table-sql)` in your init file.

Example
-------

Suppose that a Db2 query produces the following table.

```
First     Last        Batting Avg
--------- ----------- -----------
Nicholas  Castellanos        .305
Miguel        Cabrera        .299
John            Hicks        .278
```

Select the table.  Type **M-x copy-table-sql-db2-as-org** and then
**C-y** to paste the table in Org format:

```
| First    | Last        | Batting Avg |
|----------+-------------+-------------|
| Nicholas | Castellanos |        .305 |
| Miguel   | Cabrera     |        .299 |
| John     | Hicks       |        .278 |
```

Alternatively, type **M-x copy-table-sql-db2-as-markdown** and then
**C-y** to paste the table in GitHub flavored Markdown format:

```
First    | Last        | Batting Avg
---------|-------------|------------
Nicholas | Castellanos |        .305
Miguel   | Cabrera     |        .299
John     | Hicks       |        .278
```