---
route: webhook-introduction
allow_guest: 1
published: 1
---

Frappe Cloud Webhooks help deliver events related to various resources directly to your backend service.

![webhook-slide](/files/webhook-slide.png "webhook-slide.png")  


This makes it easier to build tools and custom SaaS workflows on top of Frappe Cloud using the Frappe Cloud API and webhook events.

Notes
-----

1. Webhook configurations are specific to each team.
2. A team can have a maximum of 5 webhook endpoints configured.
3. If 70% of webhook requests to your endpoint fail within the past hour, the webhook will be disabled, and the team will be notified. You can re-enable the webhook from the dashboard after resolving the issue on your end.
