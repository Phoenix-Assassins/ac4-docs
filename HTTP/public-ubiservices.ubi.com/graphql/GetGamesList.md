## Raw request

```json
[
   {
      "operationName":"GetGamesList",
      "variables":{
         "includePartyJoinRequestField":true,
         "spaceIds":[
            "c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
         ]
      },
      "extensions":{
         "persistedQuery":{
            "version":1,
            "sha256Hash":"d96fd927c0fc3e97f8922eac693bbc88f1f42fa45d9a5ca28f53de11b5320325"
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
         "games":[
            {
               "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
               "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
               "name":"Assassin's Creed® IV Black Flag",
               "avatarUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/Club_Asset/Avatar.jpg",
               "backgroundUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/backgroundAssetId.jpg",
               "isPartyEnabled":false,
               "isPartyJoinRequestEnabled":false,
               "availablePlatforms":{
                  "nodes":[
                     {
                        "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                        "type":"PC",
                        "name":"PC",
                        "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                        "__typename":"Platform"
                     },
                     {
                        "id":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                        "type":"XONE",
                        "name":"Xbox One",
                        "applicationId":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                        "__typename":"Platform"
                     },
                     {
                        "id":"580db364-b218-4b27-90ff-408a1b9a43cf",
                        "type":"PS4",
                        "name":"PS4®",
                        "applicationId":"580db364-b218-4b27-90ff-408a1b9a43cf",
                        "__typename":"Platform"
                     },
                     {
                        "id":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                        "type":"PS3",
                        "name":"PS3™",
                        "applicationId":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                        "__typename":"Platform"
                     },
                     {
                        "id":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                        "type":"WII",
                        "name":"Wii U",
                        "applicationId":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                        "__typename":"Platform"
                     }
                  ],
                  "__typename":"PlatformConnection"
               },
               "__typename":"Game"
            }
         ]
      }
   }
]
```
