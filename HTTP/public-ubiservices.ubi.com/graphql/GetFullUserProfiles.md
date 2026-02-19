## Raw request

```json
[
   {
      "operationName":"GetFullUserProfiles",
      "variables":{
         "shouldGetRichPresence":true,
         "userIds":[
            "c6e3c5f3-3a44-4099-85cb-4cab968b6813"
         ]
      },
      "extensions":{
         "persistedQuery":{
            "version":1,
            "sha256Hash":"c51161945e24d03b836c06b7e38b7e76b66e4dff265425da8a79e874b23cbb2b"
         }
      }
   }
]
```

## GQL query

Persisted query.

## Response

```json
[
   {
      "data":{
         "users":[
            {
               "id":"c6e3c5f3-3a44-4099-85cb-4cab968b6813",
               "profileId":"c6e3c5f3-3a44-4099-85cb-4cab968b6813",
               "name":"henrickjack",
               "__typename":"User",
               "currentOnlineGame":null,
               "networks":{
                  "edges":[
                     {
                        "meta":{
                           "id":"c6e3c5f3-3a44-4099-85cb-4cab968b6813",
                           "name":"henrickjack",
                           "__typename":"UserNetworkMeta"
                        },
                        "node":{
                           "id":"UPLAY",
                           "publicCodeName":"UPLAY",
                           "__typename":"Network"
                        },
                        "__typename":"UserNetworkEdge"
                     },
                     {
                        "meta":{
                           "id":"8fd61997-1ba9-4159-9925-bddce272de98",
                           "name":"76561198799363538",
                           "__typename":"UserNetworkMeta"
                        },
                        "node":{
                           "id":"STEAM",
                           "publicCodeName":"STEAM",
                           "__typename":"Network"
                        },
                        "__typename":"UserNetworkEdge"
                     }
                  ],
                  "__typename":"UserNetworksConnection"
               },
               "richPresences":[],
               "onlineStatus":"OFFLINE",
               "viewer":{
                  "meta":{
                     "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c6e3c5f3-3a44-4099-85cb-4cab968b6813",
                     "nickname":"",
                     "isFriend":true,
                     "isBlocked":false,
                     "isFavorite":false,
                     "requestStatus":"FRIENDS",
                     "__typename":"UserUserMeta"
                  },
                  "__typename":"UserUserEdge"
               }
            }
         ]
      }
   }
]
```
