## Raw request

```json
[
   {
      "operationName":"GetParticipantsQuery",
      "variables":{
         "profileIds":[
            "3850b63b-28c5-4452-adc9-0fe153b785a5",
            "ae3ebf05-7bb6-4880-ab3e-3eefc67e33b9"
         ],
         "consentIds":[
            "8212886d-abfa-49fb-b95f-169122881030"
         ]
      },
      "query":"query GetParticipantsQuery($profileIds: [String!], $consentIds: [String!]!) {\n  users(profileIds: $profileIds) {\n    ...ParticipantUserFragment\n    __typename\n  }\n}\n\nfragment ParticipantUserFragment on User {\n  profileId: userId\n  avatarUrl\n  name\n  onlineStatus\n  viewer {\n    meta {\n      isBlocked\n      isFriend\n      nickname\n      acceptances(consentIds: $consentIds) {\n        consentId\n        hasConsented\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n"
   }
]
```

## GQL query

```gql
query GetParticipantsQuery($profileIds: [String!], $consentIds: [String!]!) {
  users(profileIds: $profileIds) {
    ...ParticipantUserFragment
    __typename
  }
}

fragment ParticipantUserFragment on User {
  profileId: userId
  avatarUrl
  name
  onlineStatus
  viewer {
    meta {
      isBlocked
      isFriend
      nickname
      acceptances(consentIds: $consentIds) {
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
```

## Response

```json
[
   {
      "data":{
         "users":[
            {
               "profileId":"3850b63b-28c5-4452-adc9-0fe153b785a5",
               "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/upload/8e4a44aa_6bcb_4c77_8a28_df9323fde1ca.png?rs=146",
               "name":"CoderForLife",
               "onlineStatus":"ONLINE",
               "viewer":{
                  "meta":{
                     "isBlocked":false,
                     "isFriend":true,
                     "nickname":"",
                     "acceptances":[
                        {
                           "consentId":"8212886d-abfa-49fb-b95f-169122881030",
                           "hasConsented":true,
                           "__typename":"UserAcceptance"
                        }
                     ],
                     "__typename":"UserUserMeta"
                  },
                  "__typename":"UserUserEdge"
               },
               "__typename":"User"
            },
            {
               "profileId":"ae3ebf05-7bb6-4880-ab3e-3eefc67e33b9",
               "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/upload/c0530a36_73cc_4071_a8e6_31c4c1f02046.png?rs=146",
               "name":"Premahog",
               "onlineStatus":"OFFLINE",
               "viewer":{
                  "meta":{
                     "isBlocked":false,
                     "isFriend":true,
                     "nickname":"",
                     "acceptances":[
                        {
                           "consentId":"8212886d-abfa-49fb-b95f-169122881030",
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
         ]
      }
   }
]
```
