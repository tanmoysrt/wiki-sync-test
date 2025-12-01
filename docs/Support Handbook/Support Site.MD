---
route: handbook/support-handbook-site
allow_guest: 0
published: 1
---

### Suspend and Unsuspend a site

* To suspend a site, click on **Suspend** from *Actions* button.

![Suspend a site](/files/Screenshot%202022-08-24%20at%206.47.47%20PM.png)  


* To unsuspend a site, click on **Unsuspend** from *Actions* button.

![Unsuspend a site](/files/Screenshot%202022-08-24%20at%206.48.33%20PM.png)  


> Once a site is suspended, it will be archived after 30 days.

### Archive/Drop a site

* To archive or drop a site, click on **Archive** from *Actions* button.

![Archive Site](/files/Screenshot%202022-08-24%20at%206.49.37%20PM.png)  


> Once a site is archived, it can't be restored back again.</db*name></db*name></bench-name>

### Add app to Site

From the dashboard page of the site, go to apps section and click on **Add app**

![App List](../files/apps.png)  


Then you can select an app from the list shown. If the app you desire is not found on the list, contact a Frappe Cloud developer.

### Change Plan

* In the Site’s Desk page, Subscription -> Change Plan

![Change plan](../files/image6.png)  


### Change Ownership of a Site

* In the Site's Desk page, Subscription -> Change Team

![Change Site team](/files/Screenshot%202022-08-11%20at%207.33.29%20PM.png)  


* Enter the team name you want to transfer the ownership to along with the reason to transfer.

![Change team dialog box](/files/Screenshot%202022-08-11%20at%207.34.00%20PM.png)  


### Extend trial date of a site

* In the Site's desk page, click Subscription -> **Extend Trial**

### Update limits/expiry of Central/ERPNext Site

* Open the **Support Profile** doc on `frappe.io`

![Support Profile](../files/image5.png)  


* Update the limits or expiry as per requirement and click Save.

### Resetting the Usage Limit for a Site

> For consultants, please take a help of an Engineer.

* SSH into the site server using User SSH Certificate.
* Once you are in the site bench ie. after running `docker exec -it <bench-name> bash`
* Start redis-cli by running `redis-cli -p 13000` command.
* Usage limit can be reset by deleting the latest redis rate-limit-counter keys
* To see the avalaible keys,


```
KEYS <db_name>|rate-limit-counter*
  

```
* To delete a key,


```
DEL <db_name>|rate-limit-counter-XXXXX
  

```
> db*name can be found in site*config file of the site

### Transferring Central Site to Frappe Cloud customer

1. From Site doc, go to Subscription > Change Team and select the team you want to move the account to
2. From Site doc, go to Subscription > Change Plan and select desired plan
3. From dashboard page of site config, remove `limits` key and values
4. Uninstall Journeys app and ERPNext Support app
5. Uncheck free site checkbox if checked (Billing Section)
6. Move them to a non ERPNext Release Group (`bench-0001`, `bench-0020`) so they don’t get free emails and other things in `common_site_config` (You may skip this step for now)

### Replicate a Site

1. Take an **Offsite backup** of the site you want to replicate. Skip this step if last Offsite backup (usually a day old) is fine


	* Open desk page of site you want to copy
	* Go to linked **Site Backup** doctype list
	* Create new
	* Check the `with files` and `offsite` option and save
	* Go to dashboard page of site to see progress and wait for it to finish
2. Open [Site Replication](/app/site-replication) doctype list


	* Enter name of the site
	* Enter new subdomain. Eg: `xxx-copy` if you want to create `xxx-copy.frappe.cloud`
	* Save. This will replicate site in the same bench.

> Be careful when taking backup of large sites (>15G) as it might slow the site down depending on what server it's on.

