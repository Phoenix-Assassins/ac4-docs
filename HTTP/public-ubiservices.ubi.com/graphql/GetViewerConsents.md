## Raw request

```json
[
   {
      "operationName":"GetViewerConsents",
      "variables":{
         "consentIds":[
            "8212886d-abfa-49fb-b95f-169122881030"
         ]
      },
      "extensions":{
         "persistedQuery":{
            "version":1,
            "sha256Hash":"33c7def28470ef33eea9e4c53004e43fca6bc2d3bcef341fc359a81099909423"
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
         "viewer":{
            "id":"1feb5434-f1f1-43ff-9a68-590c969789ae",
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
