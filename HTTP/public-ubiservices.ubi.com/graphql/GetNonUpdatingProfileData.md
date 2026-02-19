## Raw request

```json
[
   {
      "operationName":"GetNonUpdatingProfileData",
      "variables":{
         "userIds":[
            "1feb5434-f1f1-43ff-9a68-590c969789ae",
            "c6e3c5f3-3a44-4099-85cb-4cab968b6813"
         ]
      },
      "extensions":{
         "persistedQuery":{
            "version":1,
            "sha256Hash":"a5eabc7090c7a59c0c1d7d63bb3dacb8b4d13c41d3e127d457d38a79b338cf52"
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
               "id":"1feb5434-f1f1-43ff-9a68-590c969789ae",
               "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/static/default_avatar.png?rs=146",
               "__typename":"User"
            },
            {
               "id":"c6e3c5f3-3a44-4099-85cb-4cab968b6813",
               "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/static/cf82b7c3_58d9_49bc_b1ac_a9e51f35c624.png?rs=146",
               "__typename":"User"
            }
         ]
      }
   }
]
```
