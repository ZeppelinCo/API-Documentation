# API

## Schema

API access is only over `HTTPS`. Base entry point is from `https://api.zepppelin.com/api/3` or from the `https://YOUR_NETWORK.zepppelin.com/api/3`
domain. All data is sent and received as `JSON`.

Times are expressed in GMT+0. All timestamps are returned in format.
```
YYYY-MM-DD hh:mm:ss
```

## HTTP Verbs

Where possible, API strives to use appropriate HTTP verbs for each
action.

* `GET`    Used for retrieving resources.
* `POST`   Used for creating resources.
* `DELETE` Used for deleting resources.

# Register application

Before getting started you need to register your application by sending request to api@zepppelin.com. Please provide application name, your fullname and your email. A registered application have a unique **Client ID**.

# Authentication
Zepppelin supports two authentication mechanism
* OAuth2
* API key based authentication and

# OAuth2

OAuth2 is a protocol that lets external apps request authorization to
private details in a user's Zepppelin account without getting their
password. 

## Authentication

OAuth2 Token (sent as a parameter):

```
$ curl https://demo.zepppelin.com?access_token=OAUTH-TOKEN
```

## Application Flow

This is a description of the OAuth flow from 3rd party web sites.

### 1. Redirect users to request Zepppelin access

```
GET https://api.zepppelin.com/oauth/authorize
```

### Parameters

* `client_id`     - The client ID you received from Zepppelin when you [registered](mailto:api@zepppelin.com).
* `redirect_uri`  - URL in your application where user's will be sent after authorization.
* `response_type` - Set to `token`.

### 2. Zepppelin redirects back to your site

Once the user has authenticated, we'll redirect them to your `redirect_uri` with the `access_token` in the url fragment. It'll look like so:

```
https://your-redirect-uri#access_token=ACCESS-TOKEN
```

### 3. Use the access token to access the API

The access token allows you to make requests to the API on a behalf of a user.

```
curl https://api.zepppelin.com/api/3/activity.json?access_token=REPLACE_WITH_ACCESS_TOKEN
```
or
```
curl https://api.zepppelin.com/api/3/activity.json \
-H "x-api-key:REPLACE_WITH_ACCESS_TOKEN"
```

# API key based authentication

The api key is associated with specific account in specific network. This key should be passed as a `HTTP` request header with each request.

## How can I get this key?
You have to authenticate user throught `/network/logins.json` entry point. Because all requests are through `HTTPS` user credentials are securely encrypted by the `SSL` channel.

#### Request headers
* `x-api-clientid` - The client ID you received from Zepppelin when you [registered](mailto:api@zepppelin.com).

#### Request parameters
* `email` - user email
* `password` - user password

#### Example with `curl`
```
curl https://api.zepppelin.com/api/3/network/logins.json \
-H "x-api-clientid:REPLACE_WITH_CLIENT_ID" \
-d email=REPLACE_WITH_USER_EMAIL \
-d password=REPLACE_WITH_USER_PASSWORD
```

In response you will recieve list of networks that the user is a member of.

#### Get user streams with API key
To make a successful Zepppelin API request, you must include a valid api key in the request. This can be done by using the `HTTP` header **x-api-key**:

```
curl https://api.zepppelin.com/api/3/user/streams.json \
-H "x-api-key:REPLACE_WITH_API_KEY"
```