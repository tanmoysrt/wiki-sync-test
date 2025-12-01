---
route: handbook/ops
allow_guest: 0
published: 1
---

### Restore Offsite backup on site without download

1. Take an **Offsite backup** of the site you want to replicate. Skip this step if last Offsite backup (usually a day old) is fine
 * Open desk page of site you want to copy
 * Go to linked **Site Backup** doctype list. Keep this open in another tab.
 * Create new
 * Check the `with files` and `offsite` option and save
 * Go to dashboard page of site to see progress and wait for it to finish

1. Restore backup on target site
 * Open desk page of site **you want to restore to**. Eg: `xxx-copy.frappe.cloud`. Note that the data in this site **WILL BE LOST**.
 * Go to *Remote Files* section
 * Fill **Remote Database File** , **Remote Private File**, **Remote Public File** fields using value of fields from the tab you kept in previous step
 ![Image of fields you need to copy](/private/files/remote-files.png)
 ![Image of fields you need to paste to](/private/files/site-remote-files.png)
 * Save
 * Actions -> Restore Site. Note that the data in this site **WILL NOW BE OVERWRITTEN** with the data in the backup

