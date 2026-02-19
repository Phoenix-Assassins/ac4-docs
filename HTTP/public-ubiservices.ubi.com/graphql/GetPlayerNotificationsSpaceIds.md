## Raw request

```json
[
   {
      "operationName":"GetPlayerNotificationsSpaceIds",
      "variables":{
         "spaceId":"867a8a29-8803-4690-8adc-54d87d920fe9"
      },
      "query":"query GetPlayerNotificationsSpaceIds($spaceId: String!) {\n  spaceParameters(spaceId: $spaceId) {\n    id\n    playerNotificationsSpaceIds {\n      blocklistService\n      friendsService\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetPlayerNotificationsSpaceIds($spaceId: String!) {
  spaceParameters(spaceId: $spaceId) {
    id
    playerNotificationsSpaceIds {
      blocklistService
      friendsService
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
         "spaceParameters":{
            "id":"867a8a29-8803-4690-8adc-54d87d920fe9",
            "playerNotificationsSpaceIds":{
               "blocklistService":"45d58365-547f-4b45-ab5b-53ed14cc79ed",
               "friendsService":"abb909cd-ebaa-4ba5-a4a5-afa75cae8195",
               "__typename":"PlayerNotificationsSpaceIdsConfig"
            },
            "__typename":"SpaceParameters"
         }
      }
   }
]
```
