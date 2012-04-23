
## Activity

<pre class="terminal">
GET https://{YOUR_NETWORK_URL}.zepppelin.com/api/3/activity.json
</pre>

Return messages in particular network. Corresponds to the "Activity" tab on the website.

### Parameters

* flow\_id: _Optional_ - Flow id

### Response

<pre class="terminal">
[
  {
    "created_at":"2012-04-23 09:33:37",
    "id":31781,
    "text":"@VladaPetrovi\u0107 signup process javi error na 2 koraku in ne gre naprej. Please popravi \u010dimprej.",
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