# 與 MySQL 的比較

## 對 JSON 的支援

MySQL：5.7 版之後支援原生 JSON

PostgreSQL：支援 JSON 和 JSONB 的資料型態（勝）

| JSON | JSONB |
| :--- | :--- |
| 儲存方式：純文字<br>內容：與輸入的資料完全相同<br>操作：可以查詢<br>索引：類似 TEXT，索引會比較慢<br>對比 MongoDB：JSON 模式 | 儲存方式：二進位<br>內容：儲存前會濾掉空格、換行等字元<br>操作：可以新增、修改、刪除 Key-Value<br>索引：比較有效<br>對比 MongoDB：BSON 模式 |

## 對地理資訊的支援

MySQL：MySQL Spatial Extensions 僅支援二維

PostgreSQL：PostGIS 可支援二維、三維和曲線（勝）

## 構建 REST API

PostgREST 可以為 PostgreSQL 提供完全的 RESTful API 服務

