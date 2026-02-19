## Raw request

```json
[
   {
      "operationName":"GetUserProfilesWithOnlyCurrentGames",
      "variables":{
         "shouldGetRichPresence":true,
         "userIds":[
            "3880b63b-2915-4452-adc9-0fe152b785ac"
         ]
      },
      "extensions":{
         "persistedQuery":{
            "version":1,
            "sha256Hash":"3f0cc5738cb463787926101fbf91fdc64f36c60d44c7363d11c1c1e46db43374"
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
         "users":[
            {
               "id":"3880b63b-2915-4452-adc9-0fe152b785ac",
               "profileId":"3880b63b-2915-4452-adc9-0fe152b785ac",
               "currentOnlineGame":null,
               "richPresences":[],
               "__typename":"User"
            }
         ]
      }
   }
]
```
