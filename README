# API

## Schema

All API access is over HTTPS, and accessed from the `YOUR_NETWORK.zepppelin.com/api/3`
domain.  All data is sent and received as JSON.

Times are expressed in GMT+0. All timestamps are returned in format.

	YYYY-MM-DD hh:mm:ss

## HTTP Verbs

Where possible, API strives to use appropriate HTTP verbs for each
action.

GET
: Used for retrieving resources.

POST
: Used for creating resources.

DELETE
: Used for deleting resources.

## Authentication

OAuth2 Token (sent as a parameter):

<pre class="terminal">
$ curl https://demo.zepppelin.com?access_token=OAUTH-TOKEN
</pre>

# OAuth2

OAuth2 is a protocol that lets external apps request authorization to
private details in a user's Zepppelin account without getting their
password. 

All developers need to register their application by sending request for application to api@zepppelin.com before getting
started. A registered OAuth application is assigned a unique Client ID.

## Application Flow

This is a description of the OAuth flow from 3rd party web sites.

### 1. Redirect users to request Zepppelin access

    GET https://YOUR_NETWORK.zepppelin.com/oauth/authorize

### Parameters

client\_id
: _Required_ **string** - The client ID you received from Zepppelin when
you [registered](mailto:api@zepppelin.com).

redirect\_uri
: _Required_ **string** - URL in your app where user's will be sent
after authorization.

response\_type
: _Required_ **string** - Set to "token".

### 2. Zepppelin redirects back to your site

Once the user has authenticated, we'll redirect them to your redirect\_uri with the access\_token 
in the url fragment. It'll look like so:

    https://your-redirect-uri#access_token=ACCESS-TOKEN

### 3. Use the access token to access the API

The access token allows you to make requests to the API on a behalf of a user.

    GET https://YOUR_NETWORK.zepppelin.com/api/3/activity.json?access_token=...