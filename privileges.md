# 權限管理（Privileges）

## 權限類型

SELECT, INSERT, UPDATE, DELETE, TRUNCATE, REFERENCES, TRIGGER, CREATE, CONNECT, TEMPORARY, EXECUTE, and USAGE.

## 基本設定

建立一個可以登入的角色

`CREATE ROLE admin LOGIN PASSWORD 'admin123';`

建立一個 DB 並且設定擁有者

`CREATE DATABASE db WITH owner = admin;`

## 給予權限（GRANT）

GRANT 指令可以設定權限給特定角色

`GRANT some_`_`privilege TO some_role;`_



