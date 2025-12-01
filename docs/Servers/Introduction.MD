---
route: servers/servers-introduction
allow_guest: 1
published: 1
---

Unlike with Public or Private benches, with Servers on Frappe Cloud you now get dedicated compute resources for your sites. Even on private benches, your bench is still on a shared server consuming shared resources along with other benches. This is not the case here.

Servers on Frappe Cloud come in pairs (Application + Database), both the servers can have different plan/size, however both are created within the same region.

Since you're paying for the servers, sites on these servers don't cost you anything extra. That means you can run as many sites and bench groups as you want on these servers.

All other features like [Private Bench Groups](https://frappecloud.com/docs/benches), [SSH Access](https://frappecloud.com/docs/ssh), Database Access work as is with servers. All Frappe Cloud servers are powered by AWS (Amazon Web Services) EC2 instances.

FAQ
---

### How many servers do I buy? Do I need to buy 2?

Yes, you always need to buy pair of servers:

* Application: This is where your code and your "site" directory will sit. All your attachments (photos, videos) will go here unless configured otherwise. Eg: [s3-attachements](https://github.com/shridarpatil/Frappe-attachments-s3)
* Database: This is where your database (MariaDB) and all "doctype" data will sit.

### How many bench groups can I create? Can I create testing and production bench group on same server?

You can create as many bench groups as you want on your server. Though the performance will get affected as you create many. [Here](https://frappecloud.com/docs/servers/guidelines-for-choosing-a-server-plan) is a guide for the same

