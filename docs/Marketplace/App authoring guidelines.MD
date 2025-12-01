---
route: marketplace/app-authoring-guidelines
allow_guest: 1
published: 1
---

This page contains guidelines for publishers who are writing Frappe apps to publish on the Frappe Cloud Marketplace

If you are new to Frappe apps, learn more about it on [frappeframework.com](https://frappeframework.com). You can also get started by following the [Tutorial](https://frappeframework.com/docs/user/en/tutorial).

1. We recommend having a settings doctype in your app to configure global behaviour of your app's functionality.
1. Make sure your app supports the current stable version of Frappe and ERPNext (if applicable).
 You can also write version specific code by checking the version of these apps in your python code:

 ```py
 from frappe import __version__ as frappe_version
 from semantic_version import Version
 
 if Version(frappe_version).major >= 13:
 # version 13 or above
 else:
 # version 12 or below
 ```
1. Don't override base functionalities provided by Frappe. For e.g., Frappe ships with authentication pages like /login for Login & Sign Up, /update for resetting passwords. If you override these, you will have to implement their functionality again.
1. Extend base functionalities by using [hooks](https://frappeframework.com/docs/v13/user/en/python-api/hooks) provided by the framework.


