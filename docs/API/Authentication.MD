---
route: api/authentication
allow_guest: 1
published: 1
---

You'll need to use `Authorization` and `X-Press-Team` HTTP headers to use Frappe Cloud API. 

Since you could be a member of multiple teams on Frappe Cloud, it is necessary to set the team using the `X-Press-Team` header. 

Refer to [API / Create an Access Token](https://frappecloud.com/docs/api/create\_an\_access\_token) to create an API key and API secret.

```bash
Authorization: Token <api-key>:<api-secret>
X-Press-Team: <team>
```

**Request**
```python
import requests

headers = {
 "Authorization": "Token <api-key>:<api-secret>",
 "X-Press-Team": "<team>"
}
requests.get("https://frappecloud.com/api/method/press.api.account.me", headers=headers).json()
```

**Response**
```json
{
 "message": {
 "user": "<user>",
 "team": "<team>"
 }
}
```
