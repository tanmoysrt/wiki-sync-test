---
route: ant-connect-to-mysql-server
allow_guest: 1
published: 1
---


```
ERROR 2002 (HY000): Can't connect to MySQL server on '10.1.1.1' (115)
```
You may see this error when restoring a site or during a migrate job. This likely happened as the mysql server restarted as it didn't have sufficient memory for the operation. Changing the **database server** plan for more memory should fix this. To change plan of your dedicated database server, refer [this guide](https://frappecloud.com/docs/servers/plan)

