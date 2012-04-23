
## List of users

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/user/all.json
</pre>

## User detail

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/user/:user_id.json
</pre>

## Follow user

<pre class="terminal">
POST https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/user/follow/:user_id.json
</pre>

## Unfollow user

<pre class="terminal">
DELETE https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/user/follow/:user_id.json
</pre>

## Get list of streams user can access

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/user/streams.json
</pre>

## User detail for current user

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/me.json
</pre>
