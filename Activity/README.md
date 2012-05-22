## Activity stream

<pre class="terminal">
GET https://api.zepppelin.com/api/3/activity.json
</pre>

Return messages in particular network. Corresponds to the "Activity" tab on the website.

### Parameters

* flow\_id: _Optional_ - Flow id 
* time: _Optional_ - UTC+0 timestamp. Returns messages till time.

### Response

``` json
[
  {
    "created_at":"2012-04-23 10:39:29",
    "id":31787,
    "text":"@UserDemo this is just sample demo status message.",
    "in_reply_to_status_id":null,
    "favorited":false,
    "type":4,
    "via":"web",
    "liked":false,
    "like_count":0,
    "comment_count":0,
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
```

## User activity stream

```
GET https://api.zepppelin.com/api/3/activity/user.json
```

Return activity messages for user.

### Parameters

* user\_id: _Optional_ - User id
* time: _Optional_ - UTC+0 timestamp. Returns messages till time.

### Response

``` json
[
  {
    "created_at":"2012-04-20 09:06:54",
    "id":31777,
    "text":"My todo",
    "in_reply_to_status_id":null,
    "favorited":false,
    "type":5,
    "via":"web",
    "liked":false,
    "like_count":0,
    "comment_count":0,
    "tags":[
      
    ],
    "can_delete":true,
    "documents":[
      
    ],
    "message_data":{
      "title":"My todo",
      "items":[
        {
          "message_item_id":"1684",
          "title":"todo item 1",
          "user_id":"4",
          "enddate":"2012-04-20 09:07:38",
          "link_url":"4-user-demo",
          "name":"Demo User",
          "file_id":"1894",
          "done":true
        },
        {
          "message_item_id":"1685",
          "title":"to do item 2",
          "done":false
        }
      ]
    },
    "new":false,
    "share_with":{
      "type":"user",
      "id":4
    }
  }
]
```

## Group activity stream

```
GET https://api.zepppelin.com/api/3/activity/group.json
```

Return activity messages for group.

### Parameters

* group\_id: _Optional_ - Group id
* time: _Optional_ - UTC+0 timestamp. Returns messages till time.

### Response

``` json
[
  {
    "created_at":"2011-04-02 04:16:16",
    "id":29542,
    "text":"new test message",
    "in_reply_to_status_id":null,
    "favorited":false,
    "type":1,
    "via":"web",
    "liked":false,
    "like_count":0,
    "comment_count":0,
    "tags":[
      
    ],
    "can_delete":true,
    "documents":[
      
    ],
    "message_data":null,
    "new":false,
    "share_with":{
      "type":"group",
      "id":14
    }
  }
]
```
