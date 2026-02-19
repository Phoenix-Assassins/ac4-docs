## Raw request

```json
[
   {
      "operationName":"GetClassicChallenges",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a79d6fb0ce57"
      },
      "query":"query GetClassicChallenges($spaceId: String!) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        classicChallenges {\n          totalCount\n          totalXpCount\n          completedCount\n          xpEarnedCount\n          nodes {\n            ...ClassicChallengeFragment\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment ClassicChallengeFragment on ClassicChallenge {\n  id\n  challengeId\n  description\n  name\n  xpPrize\n  targetCompletion\n  icon\n  viewer {\n    meta {\n      id\n      completionDate\n      isCompleted\n      currentCompletion\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetClassicChallenges($spaceId: String!) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        classicChallenges {
          totalCount
          totalXpCount
          completedCount
          xpEarnedCount
          nodes {
            ...ClassicChallengeFragment
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

fragment ClassicChallengeFragment on ClassicChallenge {
  id
  challengeId
  description
  name
  xpPrize
  targetCompletion
  icon
  viewer {
    meta {
      id
      completionDate
      isCompleted
      currentCompletion
      __typename
    }
    __typename
  }
  __typename
}
```

## Response

```json
[
   {
      "data":{
         "game":{
            "id":"c8b3f1c6-a246-4ffe-a837-a79d6fb0ce57",
            "viewer":{
               "meta":{
                  "id":"3880b63b-2915-4452-adc9-0fe152b785ac-c8b3f1c6-a246-4ffe-a837-a79d6fb0ce57",
                  "classicChallenges":{
                     "totalCount":0,
                     "totalXpCount":0,
                     "completedCount":0,
                     "xpEarnedCount":0,
                     "nodes":[],
                     "__typename":"UserGameClassicChallengesConnection"
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
