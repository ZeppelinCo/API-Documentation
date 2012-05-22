## Retrieve list of active networks

Users may have accounts in multiple networks and with this API you can get access to the list of networks that the user is a member of.
You will also get API-KEY for any of the returned network. POST request to api/3/network/logins.json with user credentials.

```
POST https://api.zepppelin.com/api/3/network/logins.json
```

### Request headers
* **x-api-clientid** - The client ID you received from Zepppelin when you [registered](mailto:api@zepppelin.com).

### Request parameters
* **email** - user email
* **password** - user password

### Response

``` json
[
  {
    "network_name":"My Company",
    "network_url":"https:\/\/mycompany.zepppelin.com",
    "api_key":"API_KEY"
  }
]
```
