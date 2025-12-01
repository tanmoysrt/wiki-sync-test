---
route: recent-issues
allow_guest: 1
published: 1
---

Frankfurt sites down issue (2025-07-22)
-----------------------------------------
Sites were reported being down and agent jobs failing on the sites with a 404 error.
The issue had happened due to an nginx config limit being reached. We've updated the same on all proxies to prevent same issues going forward.


\*.frappe.cloud redirect issue (2025-07-15)
-----------------------------------------

Around midnight 2025-07-15 IST time, frappe.cloud sites started to not resolve correctly and redirect to the Frappe Cloud dashboard instead. We identified the source as a bug in a DNS cleanup job.

Only **x.frappe.cloud** sites that are not in Mumbai region were affected. **erpnext.com** and **frappe.cloud** subdomain sites (**abc.m.frappe.cloud**, **abc.k.frappe.cloud**,etc.) were unaffected. Sites with custom domains that had A records were also unaffected.

The same has been resolved as of 1:34 am IST time. Missing DNS records were re-added for the sites affected to resolve the issue.


----------------------------------------
# New deployment issue in KSA region (2025-04-30)
KSA region has some issues with the networking in orcale cloud and impacting new deployments. [Refernece](https://ocistatus.oraclecloud.com/#/incidents/ocid1.oraclecloudincident.oc1.phx.amaaaaaavwew44aag4f4xhfscggbw74x3sff6jadk73e2rwjbpwykpyipa) 

Our technical team is actively investigating the same and will keep you posted once fixed.


----------------------------------------

# Frappe Cloud dashboard slow (2025-03-12)
We have noticed Frappe Cloud dashboard being slow due to some resource constraints from our end. We're performing an upgrade of the same. The analytics page may not load for some time


Slow deploys (2025-03-10)
-------------------------

There is an i/o block on our build server causing the deploys slow/stuck, our technical team is investigating this further, The ongoing deploys will take some time to complete. Once the load get reduced on the build server, it will be completed automatically.

Builds with Marley (healthcare) app broken (2025-02-19)
-------------------------------------------------------

Due to new release of [flit](https://flit.pypa.io/en/stable/history.html#version-3-11), deploys of benches with Marley app is now broken. Please wait until Marley team fixes the issue.  
Edit:- The issue has been [resolved](https://github.com/earthians/marley/commit/924d48185a216ba559b96d10e199c1bb0621414c) by the Marley team, redeploying the update on your bench group should work.

Issue with pending jobs on 1 server in Mumbai region (2025-10-02)
-----------------------------------------------------------------

A server had an incident where all jobs were stuck. This had gone on for 4 days until it came to our attention on 2025-10-02. We're unsure of the cause of this. We have fixed it and jobs have continued for time being. Further investigation is pending.

Issue with pending jobs on some servers (2024-12-15)
----------------------------------------------------

A few of our shared servers are having issues processing Jobs. If you're affected, you'll see the jobs going to **Pending**.

This is because of some traffic restrictions imposed by our cloud provider due to an abuse report. We're working with them to resolve this as soon as possible.  
  
Edit: Due to the lack of response from the provider. We fixed the issue ourselves by performing an emergency replacement of the virtual machines. This caused **downtime** between 10:00 AM GMT to 10:41 AM GMT across the 5 servers that were affected.

Downtime in Frankfurt region (2024-12-09)
-----------------------------------------

There was an issue affecting one of our proxy servers, in the Frankfurt region due to which sites in the region were affected from 16:20 GMT to 16:44 GMT during which we resolved the same. We are taking preventive measures.

Sites unreachable in KSA region (2024-11-24)
--------------------------------------------

Between 10:48 GMT and 11:08 GMT. One of our proxy servers in the KSA region was down which resulted in downtime for all the sites in the region. We suspect the cause to be a memory spike of an internal service and applied controls to mitigate the same. We continue to monitor the server

Sites down with internal server error (2024-10-29)
--------------------------------------------------

Between Tue, 29 Oct 2024 10:29:06 GMT and Tue, 29 Oct 2024 10:58:00 GMT, a subset of EC2 instances were unavailable in the **Mumbai** Region. The issue has been resolved by AWS and the service is operating normally.  
  


Reduced uptime for sites hosted in Virginia Region (2024-10-18)
---------------------------------------------------------------

We've observed a network connectivity issue due to which uptime monitoring of sites in the Virginia region is affected and may show as **red** in the dashboard even when the site is still up. We expect the network providers to fix this soon.  
edit: The issue has been resolved

