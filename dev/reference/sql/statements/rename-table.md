---
title: RENAME TABLE
summary: TiDB 数据库中 RENAME TABLE 的使用概况。
category: reference
---

# RENAME TABLE

`RENAME TABLE` 语句用于对已有表进行重命名。

## 总览

**RenameTableStmt:**

![RenameTableStmt](/media/sqlgram/RenameTableStmt.png)

**TableToTable:**

![TableToTable](/media/sqlgram/TableToTable.png)

## 实例

```sql
mysql> CREATE TABLE t1 (a int);
Query OK, 0 rows affected (0.12 sec)

mysql> SHOW TABLES;
+----------------+
| Tables_in_test |
+----------------+
| t1             |
+----------------+
1 row in set (0.00 sec)

mysql> RENAME TABLE t1 TO t2;
Query OK, 0 rows affected (0.08 sec)

mysql> SHOW TABLES;
+----------------+
| Tables_in_test |
+----------------+
| t2             |
+----------------+
1 row in set (0.00 sec)
```

## MySQL 兼容性

`RENAME TABLE` 语句可视为与 MySQL 完全兼容。如有任何兼容性差异，请在 GitHub 上 提交 [issue](/report-issue.md)。

## 另请参阅

* [CREATE TABLE](/dev/reference/sql/statements/create-table.md)
* [SHOW TABLES](/dev/reference/sql/statements/show-tables.md)
* [ALTER TABLE](/dev/reference/sql/statements/alter-table.md)