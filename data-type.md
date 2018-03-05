# 資料類型（Data Type）

官網：[https://www.postgresql.org/docs/10/static/datatype.html](https://www.postgresql.org/docs/10/static/datatype.html)

## 數字類型（Numeric Types）

| Name | Storage Size | Description | Range |
| :--- | :--- | :--- | :--- |
| `smallint` | 2 bytes | small-range integer | -32768 to +32767 |
| `integer` | 4 bytes | typical choice for integer | -2147483648 to +2147483647 |
| `bigint` | 8 bytes | large-range integer | -9223372036854775808 to +9223372036854775807 |
| `decimal` | variable | user-specified precision, exact | up to 131072 digits before the decimal point; up to 16383 digits after the decimal point |
| `numeric` | variable | user-specified precision, exact | up to 131072 digits before the decimal point; up to 16383 digits after the decimal point |
| `real` | 4 bytes | variable-precision, inexact | 6 decimal digits precision |
| `double precision` | 8 bytes | variable-precision, inexact | 15 decimal digits precision |
| `smallserial` | 2 bytes | small autoincrementing integer | 1 to 32767 |
| `serial` | 4 bytes | autoincrementing integer | 1 to 2147483647 |
| `bigserial` | 8 bytes | large autoincrementing integer | 1 to 9223372036854775807 |

## 貨幣類型（Monetary Types）

| Name | Storage Size | Description | Range |
| :--- | :--- | :--- | :--- |
| `money` | 8 bytes | currency amount | -92233720368547758.08 to +92233720368547758.07 |



## 字元類型（Character Types）

| Name | Description |
| :--- | :--- |
| `character varying(n),　varchar(n)` | variable-length with limit |
| `character(n),　char(n)` | fixed-length, blank padded |
| `text` | variable unlimited length |



