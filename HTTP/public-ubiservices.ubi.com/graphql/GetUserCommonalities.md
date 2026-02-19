## Raw request

```json
[
   {
      "operationName":"GetUserCommonalities",
      "variables":{
         "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac"
      },
      "query":"query GetUserCommonalities($userId: String!) {\n  user(userId: $userId) {\n    id\n    viewer {\n      meta {\n        id\n        gamesInCommon {\n          totalCount\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetUserCommonalities($userId: String!) {
  user(userId: $userId) {
    id
    viewer {
      meta {
        id
        gamesInCommon {
          totalCount
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
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-9370b63b-2d13-4352-adb9-0fe152a485ac",
                  "gamesInCommon":{
                     "totalCount":3,
                     "__typename":"GamesConnection"
                  },
                  "__typename":"UserUserMeta"
               },
               "__typename":"UserUserEdge"
            },
            "__typename":"User"
         }
      }
   }
]
```
