## Raw request

```json
[
   {
      "operationName":"GetViewerConsentsQuery",
      "variables":{
         "consentIds":[
            "8212886d-abfa-49fb-b95f-169122881030"
         ]
      },
      "query":"query GetViewerConsentsQuery($consentIds: [String!]!) {\n  viewer {\n    playerConsents(consentIds: $consentIds) {\n      id\n      consentValue\n      __typename\n    }\n    __typename\n  }\n}\n"
   }
]
```

## GQL query

```gql
query GetViewerConsentsQuery($consentIds: [String!]!) {
  viewer {
    playerConsents(consentIds: $consentIds) {
      id
      consentValue
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
         "viewer":{
            "playerConsents":[
               {
                  "id":"8212886d-abfa-49fb-b95f-169122881030",
                  "consentValue":"public",
                  "__typename":"PlayerConsent"
               }
            ],
            "__typename":"User"
         }
      }
   }
]
```
