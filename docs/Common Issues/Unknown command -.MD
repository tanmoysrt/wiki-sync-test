---
route: nknown-command-
allow_guest: 1
published: 1
---

When restoring a backup, you may see a command like so:


```
Restoring Database file...
ERROR at line 7: Unknown command '\-'.
```
This happens when backup from newer MariaDB is attempted to restore on an older version. This has been fixed in [**frappe**](https://github.com/frappe/frappe/) already. To rectify this, you should update your site to latest [supported](https://github.com/frappe/erpnext/wiki/Supported-Versions) version of frappe and try again.

  


