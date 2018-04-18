# upsert（on\_conflict\_do\_update）

官網說明：[http://docs.sqlalchemy.org/en/latest/dialects/postgresql.html?highlight=conflict\#insert-on-conflict-upsert](http://docs.sqlalchemy.org/en/latest/dialects/postgresql.html?highlight=conflict#insert-on-conflict-upsert)

```
from sqlalchemy.dialects.postgresql import insert

insert_stmt = insert(my_table).values(
    id='some_existing_id',
    data='inserted value')

do_nothing_stmt = insert_stmt.on_conflict_do_nothing(
    index_elements=['id']
)

conn.execute(do_nothing_stmt)

do_update_stmt = insert_stmt.on_conflict_do_update(
    constraint='pk_my_table',
    set_=dict(data='updated value')
)

conn.execute(do_update_stmt)
```



