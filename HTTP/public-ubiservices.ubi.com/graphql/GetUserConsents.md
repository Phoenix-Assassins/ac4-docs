## Raw request

```json
[
   {
      "operationName":"GetUserConsents",
      "variables":{
         "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
         "consentIds":[
            "76c93e10-5a8b-49a8-925c-a9bd5422851a"
         ]
      },
      "query":"query GetUserConsents($userId: String!, $consentIds: [String!]!) {\n  user(userId: $userId) {\n    id\n    name\n    viewer {\n      meta {\n        id\n        acceptances(consentIds: $consentIds) {\n          id\n          consentId\n          hasConsented\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetUserConsents($userId: String!, $consentIds: [String!]!) {
  user(userId: $userId) {
    id
    name
    viewer {
      meta {
        id
        acceptances(consentIds: $consentIds) {
          id
          consentId
          hasConsented
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
            "name":"CoderForLife",
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-9370b63b-2d13-4352-adb9-0fe152a485ac",
                  "acceptances":[
                     {
                        "id":"9370b63b-2d13-4352-adb9-0fe152a485ac-76c93e10-5a8b-49a8-925c-a9bd5322851a",
                        "consentId":"76c93e10-5a8b-49a8-925c-a9bd5322851a",
                        "hasConsented":true,
                        "__typename":"UserAcceptance"
                     }
                  ],
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
