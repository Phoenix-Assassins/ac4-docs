## Raw request

```json
[
   {
      "operationName":"GetFriends",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetFriends($spaceId: String) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        friends {\n          totalCount\n          edges {\n            node {\n              id\n              userId\n              name\n              avatarUrl\n              onlineStatus\n              currentOnlineGame {\n                node {\n                  id\n                  __typename\n                }\n                __typename\n              }\n              viewer {\n                meta {\n                  id\n                  nickname\n                  isFavorite\n                  __typename\n                }\n                __typename\n              }\n              __typename\n            }\n            meta {\n              id\n              hasPlaySession\n              lastPlayedDate\n              __typename\n            }\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetFriends($spaceId: String) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        friends {
          totalCount
          edges {
            node {
              id
              userId
              name
              avatarUrl
              onlineStatus
              currentOnlineGame {
                node {
                  id
                  __typename
                }
                __typename
              }
              viewer {
                meta {
                  id
                  nickname
                  isFavorite
                  __typename
                }
                __typename
              }
              __typename
            }
            meta {
              id
              hasPlaySession
              lastPlayedDate
              __typename
            }
            __typename
          }
          __typename
        }
        __typename
      }
      __typename
    }
    __typename
  }
}
```

## Response

```json
[
   {
      "data":{
         "game":{
            "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "friends":{
                     "totalCount":2,
                     "edges":[
                        {
                           "node":{
                              "id":"3880b63b-2815-4452-adc9-0ff152b785a5",
                              "userId":"3880b63b-2815-4452-adc9-0fe152b785a5",
                              "name":"CoderForLife",
                              "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/upload/8e4a44aa_6bcb_4c77_8a28_df9323fde1ca.png?rs=146",
                              "onlineStatus":"ONLINE",
                              "currentOnlineGame":null,
                              "viewer":{
                                 "meta":{
                                    "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-3880b63b-2815-4452-adc9-0fe152b785a5",
                                    "nickname":"",
                                    "isFavorite":false,
                                    "__typename":"UserUserMeta"
                                 },
                                 "__typename":"UserUserEdge"
                              },
                              "__typename":"User"
                           },
                           "meta":{
                              "id":"3880b63b-2815-4452-adc9-0fe152b785a5-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                              "hasPlaySession":true,
                              "lastPlayedDate":null,
                              "__typename":"UserGameMeta"
                           },
                           "__typename":"GameUserEdge"
                        },
                        {
                           "node":{
                              "id":"ae3ebf05-7bb6-4880-ab3e-3eefc67e3342",
                              "userId":"ae3ebf05-7bb6-4880-ab3e-3effc67e3342",
                              "name":"Premahog",
                              "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/upload/c0530a36_73cc_4071_a8e6_31c4c1f02046.png?rs=146",
                              "onlineStatus":"OFFLINE",
                              "currentOnlineGame":null,
                              "viewer":{
                                 "meta":{
                                    "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-ae3ebf05-7bb6-4880-ab3e-3effc67e3342",
                                    "nickname":"",
                                    "isFavorite":false,
                                    "__typename":"UserUserMeta"
                                 },
                                 "__typename":"UserUserEdge"
                              },
                              "__typename":"User"
                           },
                           "meta":{
                              "id":"ae3ebf05-7bb6-4880-ab3e-3effc67e3342-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                              "hasPlaySession":true,
                              "lastPlayedDate":null,
                              "__typename":"UserGameMeta"
                           },
                           "__typename":"GameUserEdge"
                        }
                     ],
                     "__typename":"GameFriendsConnection"
                  },
                  "__typename":"UserGameMeta"
               },
               "__typename":"GameUserEdge"
            },
            "__typename":"Game"
         }
      }
   }
]
```
