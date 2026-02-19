## Raw request

```json
[
   {
      "operationName":"GetGameName",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetGameName($spaceId: String!) {\n  game(spaceId: $spaceId) {\n    id\n    name\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetGameName($spaceId: String!) {
  game(spaceId: $spaceId) {
    id
    name
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
            "name":"Assassin's Creed® IV Black Flag",
            "__typename":"Game"
         }
      }
   }
]
```
