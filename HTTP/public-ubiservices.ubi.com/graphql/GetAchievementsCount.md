## Raw request

```json
[
   {
      "operationName":"GetAchievementsCount",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
         "productId":437
      },
      "query":"query GetAchievementsCount($spaceId: String!, $productId: Int!) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        achievements(productId: $productId) {\n          totalCount\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetAchievementsCount($spaceId: String!, $productId: Int!) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        achievements(productId: $productId) {
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
         "game":{
            "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                  "achievements":{
                     "totalCount":60,
                     "__typename":"UserGameAchievementsConnection"
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
