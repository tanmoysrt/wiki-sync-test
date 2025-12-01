---
route: sites/monitoring
allow_guest: 1
published: 1
---

Frappe Cloud logs a lot of data while your site is running like Request Logs, Site Logs, CPU Time, etc.

Site Analytics
--------------

The **Analytics** tabs shows a lot of charts:

1. **Requests** - Number of Requests (per minute)
2. **CPU Usage** - CPU Usage of Requests
3. **Background Jobs** - Number of Background Jobs
4. **Background Jobs CPU Usage** - CPU Usage of Background Jobs
5. **Usage Counter** - Cumulative CPU Usage of Requests. You can also see the Daily CPU Time Limit line, you can monitor this chart to know when you need to upgrade your Plan.
6. **Uptime** - Uptime of the web worker and scheduler. Collected every 3 minutes.

[![Site Analytics](https://cloud.frappe.io/assets/press/images/docs/site-analytics.png)](https://cloud.frappe.io/assets/press/images/docs/site-analytics.png)  


Analytics are only available after Setup Wizard is completed. Uptime status is collected every minute.

Investigating high usage
------------------------

Primarily for investigating high usage, you should look at the **Requests Duration By Path** and **Background Job Duration By Path** graphs. This will give you an idea of which endpoints in your site take most time/requests.

![](https://frappecloud.com../files/gszsZA1.png)  


Here, the red bars are seem to take relatively long and should be looked into.

![](https://frappecloud.com../files/xKtypi1.png)  


It is sorted in descending order, so the first endpoints in the list are usually slowest.

