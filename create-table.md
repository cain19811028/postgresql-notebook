# create table 相關語法

```
create table t1 (
    id uuid default gen_random_uuid() primary key,
    data json default '{}'::jsonb,
    createdTime timestamptz default now()
);
```

gen\_random\_uuid\(\)：自動產生 UUID

'{}'::jsonb：自動產生空的 JSON

now()：取得現在時間
