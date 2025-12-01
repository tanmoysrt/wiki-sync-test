---
route: hybrid-cloud-introduction
allow_guest: 1
published: 1
---

 Hybrid Model of hosting your ERPNext Sites with Frappe Cloud.

Frappe Cloud Hybrid leverages "your server, your data" ideology by setting up the basic requirements to run an ERPNext Site(s) controlled from FC Dashboard. This way you can run ERPNext sites on your own infrastructure and can leverage all the features of Frappe Cloud.

We use Ansible Playbooks to set up the server and our in-house developed orchestrator called [Agent](https://github.com/frappe/agent) to do site related activities like updates, backups, restores and migrations. Agent is extensively used to control all the 6000+ sites and 100+ servers currently on Frappe Cloud.

All new sites on these servers won't cost you anything extra since you are paying for these servers and we just help you out in achieving the best from those servers. You can create unlimited private bench groups and sites on these servers.

## Difference from FC Servers

The difference of Self Hosted Servers from Frappe Cloud servers is that, one single server which the user provides will be used as both App and Database Server. Wherein in Frappe Cloud Servers, one server is used as the App Server and the other is used as the Database Server.

> These servers won’t be in Frappe’s control and its maintenance will be completely on the owner of the server.

## Benefits and Features
1. Control and Security: Frappe Cloud Hybrid allows customers to maintain complete control over their infrastructure and data, which is especially important for customers who have strict security requirements or are subject to regulatory compliance.

2. Flexibility: Frappe Cloud Hybrid allows customers to scale their infrastructure up or down as needed, without having to worry about capacity constraints or other limitations.

3. All features of Frappe Cloud including
 * Offsite Backups
 * Server Monitoring
 * Frappe Cloud Hosting Support
 * Multiple Sites on Same Server
 * Auto Updates on Site