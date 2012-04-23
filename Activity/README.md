# Activity

## Messages in this network. Corresponds to the "Activity" tab on the website.

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/activity.json
</pre>

### Parameters

* flow\_id: _Optional_ - Flow id

### Response

<pre class="terminal">
[
  {
    "created_at":"2012-01-23 09:33:37",
    "id":31781,
    "text":"@User1 this is just a sample message text",
    "in_reply_to_status_id":null,
    "favorited":false,
    "type":1,
    "via":"web",
    "liked":false,
    "like_count":0,
    "comment_count":2,
    "tags":[
      
    ],
    "can_delete":true,
    "documents":[
      
    ],
    "message_data":null,
    "new":false,
    "share_with":{
      "type":"everyone",
      "id":null
    }
  }
]
</pre>