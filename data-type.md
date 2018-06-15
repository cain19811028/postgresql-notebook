# 資料類型（Data Type）

官網：[https://www.postgresql.org/docs/10/static/datatype.html](https://www.postgresql.org/docs/10/static/datatype.html)

## 數字類型（Numeric Types）

| Name | Storage Size | Description | Range |
| :--- | :--- | :--- | :--- |
| smallint | 2 bytes | small-range integer | -32768 to +32767 |
| integer | 4 bytes | typical choice for integer | -2147483648 to +2147483647 |
| bigint | 8 bytes | large-range integer | -9223372036854775808 to +9223372036854775807 |
| decimal | variable | user-specified precision, exact | up to 131072 digits before the decimal point; up to 16383 digits after the decimal point |
| numeric | variable | user-specified precision, exact | up to 131072 digits before the decimal point; up to 16383 digits after the decimal point |
| real | 4 bytes | variable-precision, inexact | 6 decimal digits precision |
| double precision | 8 bytes | variable-precision, inexact | 15 decimal digits precision |
| smallserial | 2 bytes | small autoincrementing integer | 1 to 32767 |
| serial | 4 bytes | autoincrementing integer | 1 to 2147483647 |
| bigserial | 8 bytes | large autoincrementing integer | 1 to 9223372036854775807 |

## 貨幣類型（Monetary Types）

| Name | Storage Size | Description | Range |
| :--- | :--- | :--- | :--- |
| money | 8 bytes | currency amount | -92233720368547758.08 to +92233720368547758.07 |

## 字元類型（Character Types）

| Name | Description |
| :--- | :--- |
| character varying\(n\),　varchar\(n\) | variable-length with limit |
| character\(n\),　char\(n\) | fixed-length, blank padded |
| text | variable unlimited length |

## 二進制資料類別（Binary Data Types）

| Name | Storage Size | Description |
| :--- | :--- | :--- |
| bytea | 1 or 4 bytes plus the actual binary string | variable-length binary string |

## 日期時間類別（Date/Time Types）

| Name | Storage Size | Description | Low Value | High Value | Resolution |
| :--- | :--- | :--- | :--- | :--- | :--- |
| timestamp \[ \(p\) \] \[ without time zone \] | 8 bytes | both date and time \(no time zone\) | 4713 BC | 294276 AD | 1 ms |
| timestamp \[ \(p\) \] with time zone | 8 bytes | both date and time, with time zone | 4713 BC | 294276 AD | 1 ms |
| date | 4 bytes | date \(no time of day\) | 4713 BC | 5874897 AD | 1 day |
| time \[ \(p\) \] \[ without time zone \] | 8 bytes | time of day \(no date\) | 00:00:00 | 24:00:00 | 1 ms |
| time \[ \(p\) \] with time zone | 12 bytes | time of day \(no date\), with time zone | 00:00:00+1459 | 24:00:00-1459 | 1 ms |
| interval \[ fields \] \[ \(p\) \] | 16 bytes | time interval | -178000000 years | 178000000 years | 1 ms |

## 布林類別（Boolean Types）

| Name | Storage Size | Description |
| :--- | :--- | :--- |
| boolean | 1 byte | state of true or false |

## 幾何類型（**Geometric Types）**

| Name | Storage Size | Description | Representation |
| :--- | :--- | :--- | :--- |
| point | 16 bytes | Point on a plane | \(x,y\) |
| line | 32 bytes | Infinite line | {A,B,C} |
| lseg | 32 bytes | Finite line segment | \(\(x1,y1\),\(x2,y2\)\) |
| box | 32 bytes | Rectangular box | \(\(x1,y1\),\(x2,y2\)\) |
| path | 16+16n bytes | Closed path \(similar to polygon\) | \(\(x1,y1\),...\) |
| path | 16+16n bytes | Open path | \[\(x1,y1\),...\] |
| polygon | 40+16n bytes | Polygon \(similar to closed path\) | \(\(x1,y1\),...\) |
| circle | 24 bytes | Circle | &lt;\(x,y\),r&gt; \(center point and radius\) |



