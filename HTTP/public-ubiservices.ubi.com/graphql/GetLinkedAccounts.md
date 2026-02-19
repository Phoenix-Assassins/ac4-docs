## Raw request

```json
[
   {
      "operationName":"GetLinkedAccounts",
      "variables":{
         "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac"
      },
      "query":"query GetLinkedAccounts($userId: String!) {\n  user(userId: $userId) {\n    id\n    networks {\n      edges {\n        meta {\n          id\n          profileId\n          name\n          __typename\n        }\n        node {\n          id\n          publicCodeName\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetLinkedAccounts($userId: String!) {
  user(userId: $userId) {
    id
    networks {
      edges {
        meta {
          id
          profileId
          name
          __typename
        }
        node {
          id
          publicCodeName
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
         "user":{
            "id":"9370b63b-2d13-4352-adb9-0fe152a485ac",
            "networks":{
               "edges":[
                  {
                     "meta":{
                        "id":"9370b63b-2d13-4352-adb9-0fe152a485ac",
                        "profileId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
                        "name":"CoderForLife",
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
                        "id":"6ca94b15-adb4-4298-b45a-8b109401c0f6",
                        "profileId":"6ca94b15-adb4-4298-b45a-8b109401c0f6",
                        "name":"CoderforLife666",
                        "__typename":"UserNetworkMeta"
                     },
                     "node":{
                        "id":"XBL",
                        "publicCodeName":"XBL",
                        "__typename":"Network"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "meta":{
                        "id":"3c4572fc-9186-4582-ad20-2e7a695d7f97",
                        "profileId":"3c4572fc-9186-4582-ad20-2e7a695d7f97",
                        "name":"CoderForLife666",
                        "__typename":"UserNetworkMeta"
                     },
                     "node":{
                        "id":"PSN",
                        "publicCodeName":"PSN",
                        "__typename":"Network"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "meta":{
                        "id":"13ca4bca-c724-4e81-83c3-e2158cb9d792",
                        "profileId":"13ca4bca-c724-4e81-83c3-e2158cb9d792",
                        "name":"LifeCoder",
                        "__typename":"UserNetworkMeta"
                     },
                     "node":{
                        "id":"SWITCH",
                        "publicCodeName":"NINTENDO",
                        "__typename":"Network"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "meta":{
                        "id":"e47134d4-b05b-98eb-3a7f-822a0f21b0c2",
                        "profileId":"e47134d4-b05b-98eb-3a7f-822a0f21b0c2",
                        "name":"coder_for_life",
                        "__typename":"UserNetworkMeta"
                     },
                     "node":{
                        "id":"TWITCH",
                        "publicCodeName":"TWITCH",
                        "__typename":"Network"
                     },
                     "__typename":"UserNetworkEdge"
                  }
               ],
               "__typename":"UserNetworksConnection"
            },
            "__typename":"User"
         }
      }
   }
]
```
