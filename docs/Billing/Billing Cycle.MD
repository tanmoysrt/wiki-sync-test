---
route: billing/billing-cycle
allow_guest: 1
published: 1
---

<div markdown="1"><p>Overview of Frappe Cloud's Billing Process</p><p>Frappe Cloud billing cycles are monthly. Each site is microbilled on a daily basis. When you select a plan, the monthly amount is divided by the number of days in the current calendar month. You are charged every day based on the number of sites you have each day.</p><p><a target="_blank" rel="noopener noreferrer nofollow" href="https://cloud.frappe.io/assets/press/images/docs/account-billing.png"><img class="screenshot" src="https://cloud.frappe.io/assets/press/images/docs/account-billing.png" alt="Billing Dashboard" contenteditable="false" draggable="true"><img class="ProseMirror-separator" alt=""></a><br class="ProseMirror-trailingBreak"></p><p>You can access and update your billing information from <a target="_blank" rel="noopener noreferrer nofollow" href="/dashboard/account/billing">/dashboard/account/billing</a>. The dashboard also shows information regarding the current usage from all your sites.</p><blockquote><p>We finalize invoices on <strong>the last day of each month at 6 PM IST</strong>. Sites created after this point will be a part of next month's billing cycle.</p></blockquote><h2>Use Cases</h2><p>Here's an attempt to explain the process by considering a few use cases:</p><h3>Single <strong>plan </strong>throughout the calendar month</h3><p>When you select the <code>$100</code> plan for your site <code>raftel.frappe.cloud</code>, every day <code>$3.33</code> is accrued to your monthly usage in case of a 30 day month. For the month of April, the estimate would look something like</p><div class="tableWrapper"><table style="min-width: 125px;"><colgroup><col><col><col><col><col></colgroup><tbody><tr><th colspan="1" rowspan="1"><p>-</p></th><th colspan="1" rowspan="1"><p>Base Plan</p></th><th colspan="1" rowspan="1"><p>No. of Days</p></th><th colspan="1" rowspan="1"><p>Rate</p></th><th colspan="1" rowspan="1"><p>Total</p></th></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p>$100</p></td><td colspan="1" rowspan="1"><p>30</p></td><td colspan="1" rowspan="1"><p>$3.33/day</p></td><td colspan="1" rowspan="1"><p>$99.9</p></td></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><strong>$99.9</strong></p></td></tr></tbody></table></div><p>This rate may go to <code>$3.23</code> in case of a 31 day month or <code>$3.57</code> in case of a 28 day month. This means that you are charged no more than <code>$100</code> for hosting your site each month. For February 2024 (leap year), this would look something like</p><div class="tableWrapper"><table style="min-width: 125px;"><colgroup><col><col><col><col><col></colgroup><tbody><tr><th colspan="1" rowspan="1"><p>-</p></th><th colspan="1" rowspan="1"><p>Base Plan</p></th><th colspan="1" rowspan="1"><p>No. of Days</p></th><th colspan="1" rowspan="1"><p>Rate</p></th><th colspan="1" rowspan="1"><p>Total</p></th></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p>$100</p></td><td colspan="1" rowspan="1"><p>29</p></td><td colspan="1" rowspan="1"><p>$3.45/day</p></td><td colspan="1" rowspan="1"><p>$100.05</p></td></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><strong>$100.05</strong></p></td></tr></tbody></table></div><h3>Multiple plans throughout the calendar month</h3><p>Another instance of hosting a site <code>laugh-tale.frappe.cloud</code> on <code>$200</code> plan. After 15 days, you need more CPU time and decide to upgrade to plan <code>$500</code>. For a 31 day month, you get charged <code>$354.84</code> in total. Here's the break up.</p><div class="tableWrapper"><table style="min-width: 125px;"><colgroup><col><col><col><col><col></colgroup><tbody><tr><th colspan="1" rowspan="1"><p>-</p></th><th colspan="1" rowspan="1"><p>Base Plan</p></th><th colspan="1" rowspan="1"><p>No. of Days</p></th><th colspan="1" rowspan="1"><p>Rate</p></th><th colspan="1" rowspan="1"><p>Total</p></th></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p>$200</p></td><td colspan="1" rowspan="1"><p>15</p></td><td colspan="1" rowspan="1"><p>$6.45/day</p></td><td colspan="1" rowspan="1"><p>$96.77</p></td></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p>$500</p></td><td colspan="1" rowspan="1"><p>16</p></td><td colspan="1" rowspan="1"><p>$16.13/day</p></td><td colspan="1" rowspan="1"><p>$258.07</p></td></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><strong>$354.84</strong></p></td></tr></tbody></table></div><h3>Site dropped in the middle of the month</h3><p>If you drop your site <code>arabasta.frappe.cloud</code> 4 days into the month, you will be charged for those 4 days.</p><div class="tableWrapper"><table style="min-width: 125px;"><colgroup><col><col><col><col><col></colgroup><tbody><tr><th colspan="1" rowspan="1"><p>-</p></th><th colspan="1" rowspan="1"><p>Base Plan</p></th><th colspan="1" rowspan="1"><p>No. of Days</p></th><th colspan="1" rowspan="1"><p>Rate</p></th><th colspan="1" rowspan="1"><p>Total</p></th></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p>$200</p></td><td colspan="1" rowspan="1"><p>4</p></td><td colspan="1" rowspan="1"><p>$6.45/day</p></td><td colspan="1" rowspan="1"><p>$25.8</p></td></tr><tr><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><br class="ProseMirror-trailingBreak"></p></td><td colspan="1" rowspan="1"><p><strong>$25.8</strong></p></td></tr></tbody></table></div><blockquote><p>Even if you might drop all your sites mid-way, you will receive the invoice at the end of the month.</p></blockquote></div>

Frappe Cloud billing cycles are monthly. Each site is microbilled on a daily basis. When you select a plan, the monthly amount is divided by the number of days in the current calendar month. You are charged every day based on the number of sites you have each day.

[![Billing Dashboard](https://cloud.frappe.io/assets/press/images/docs/account-billing.png)](https://cloud.frappe.io/assets/press/images/docs/account-billing.png)

You can access and update your billing information from </dashboard/account/billing>. The dashboard also shows information regarding the current usage from all your sites.


> We finalize invoices on **the last day of each month at 6 PM IST**. Sites created after this point will be a part of next month's billing cycle.
> 
> 

Use Cases
---------

Here's an attempt to explain the process by considering a few use cases:

### Single plan throughout the calendar month

When you select the `$100` plan for your site `raftel.frappe.cloud`, every day `$3.33` is accrued to your monthly usage in case of a 30 day month. For the month of April, the estimate would look something like



| - | Base Plan | No. of Days | Rate | Total |
| --- | --- | --- | --- | --- |
|  | $100 | 30 | $3.33/day | $99.9 |
|  |  |  |  | **$99.9** |

This rate may go to `$3.23` in case of a 31 day month or `$3.57` in case of a 28 day month. This means that you are charged no more than `$100` for hosting your site each month. For February 2024 (leap year), this would look something like



| - | Base Plan | No. of Days | Rate | Total |
| --- | --- | --- | --- | --- |
|  | $100 | 29 | $3.45/day | $100.05 |
|  |  |  |  | **$100.05** |

### Multiple plans throughout the calendar month

Another instance of hosting a site `laugh-tale.frappe.cloud` on `$200` plan. After 15 days, you need more CPU time and decide to upgrade to plan `$500`. For a 31 day month, you get charged `$354.84` in total. Here's the break up.



| - | Base Plan | No. of Days | Rate | Total |
| --- | --- | --- | --- | --- |
|  | $200 | 15 | $6.45/day | $96.77 |
|  | $500 | 16 | $16.13/day | $258.07 |
|  |  |  |  | **$354.84** |

### Site dropped in the middle of the month

If you drop your site `arabasta.frappe.cloud` 4 days into the month, you will be charged for those 4 days.



| - | Base Plan | No. of Days | Rate | Total |
| --- | --- | --- | --- | --- |
|  | $200 | 4 | $6.45/day | $25.8 |
|  |  |  |  | **$25.8** |


> Even if you might drop all your sites mid-way, you will receive the invoice at the end of the month.
> 
> 

