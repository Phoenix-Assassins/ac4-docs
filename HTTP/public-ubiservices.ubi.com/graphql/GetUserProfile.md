## Raw request

```json
[
   {
      "operationName":"GetUserProfile",
      "variables":{
         "userId":"f880b63b-2845-3452-adb9-0fe152b78538"
      },
      "query":"query GetUserProfile($userId: String!) {\n  user(userId: $userId) {\n    ...ProfileFragment\n    __typename\n  }\n}\n\nfragment ProfileFragment on User {\n  id\n  userId\n  avatarUrl\n  name\n  level\n  isViewer\n  onlineStatus\n  games(filterBy: {isOwned: true}) {\n    totalCount\n    __typename\n  }\n  networks {\n    edges {\n      node {\n        id\n        publicCodeName\n        __typename\n      }\n      meta {\n        id\n        name\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  lastPlayedGame {\n    node {\n      id\n      bannerUrl: backgroundUrl\n      __typename\n    }\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      isFavorite\n      isFriend\n      isBlocked\n      requestStatus\n      nickname\n      gamesInCommon {\n        totalCount\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetUserProfile($userId: String!) {
  user(userId: $userId) {
    ...ProfileFragment
    __typename
  }
}

fragment ProfileFragment on User {
  id
  userId
  avatarUrl
  name
  level
  isViewer
  onlineStatus
  games(filterBy: {isOwned: true}) {
    totalCount
    __typename
  }
  networks {
    edges {
      node {
        id
        publicCodeName
        __typename
      }
      meta {
        id
        name
        __typename
      }
      __typename
    }
    __typename
  }
  lastPlayedGame {
    node {
      id
      bannerUrl: backgroundUrl
      __typename
    }
    __typename
  }
  viewer {
    meta {
      id
      isFavorite
      isFriend
      isBlocked
      requestStatus
      nickname
      gamesInCommon {
        totalCount
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
         "user":{
            "id":"3880b63b-2815-4452-adc9-0fe152b785a5",
            "userId":"3880b63b-2815-4452-adc9-0fe152b785a5",
            "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/upload/8e4a44aa_6bcb_4c77_8a28_df9323fde1ca.png?rs=146",
            "name":"CoderForLife",
            "level":76,
            "isViewer":false,
            "onlineStatus":"ONLINE",
            "games":{
               "totalCount":39,
               "__typename":"UserGamesConnection"
            },
            "networks":{
               "edges":[
                  {
                     "node":{
                        "id":"UPLAY",
                        "publicCodeName":"UPLAY",
                        "__typename":"Network"
                     },
                     "meta":{
                        "id":"f880b63b-2845-3452-adb9-0fe152b78538",
                        "name":"CoderForLife",
                        "__typename":"UserNetworkMeta"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "node":{
                        "id":"XBL",
                        "publicCodeName":"XBL",
                        "__typename":"Network"
                     },
                     "meta":{
                        "id":"2cc24b35-a8b4-4298-b46a-8b143482d071",
                        "name":"CoderforLife666",
                        "__typename":"UserNetworkMeta"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "node":{
                        "id":"PSN",
                        "publicCodeName":"PSN",
                        "__typename":"Network"
                     },
                     "meta":{
                        "id":"bc48720c-414c-4552-a820-5e7e69cd7f91",
                        "name":"CoderForLife666",
                        "__typename":"UserNetworkMeta"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "node":{
                        "id":"SWITCH",
                        "publicCodeName":"NINTENDO",
                        "__typename":"Network"
                     },
                     "meta":{
                        "id":"6f1a4bca-c214-4e81-83c3-e2c55cbd4792",
                        "name":"LifeCoder",
                        "__typename":"UserNetworkMeta"
                     },
                     "__typename":"UserNetworkEdge"
                  },
                  {
                     "node":{
                        "id":"TWITCH",
                        "publicCodeName":"TWITCH",
                        "__typename":"Network"
                     },
                     "meta":{
                        "id":"f42134d8-b757-3aeb-8a37-822a3f61b0c1",
                        "name":"coder_for_life",
                        "__typename":"UserNetworkMeta"
                     },
                     "__typename":"UserNetworkEdge"
                  }
               ],
               "__typename":"UserNetworksConnection"
            },
            "lastPlayedGame":{
               "node":{
                  "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "bannerUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/backgroundAssetId.jpg",
                  "__typename":"Game"
               },
               "__typename":"UserGameEdge"
            },
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-f880b63b-2845-3452-adb9-0fe152b78538",
                  "isFavorite":false,
                  "isFriend":true,
                  "isBlocked":false,
                  "requestStatus":"FRIENDS",
                  "nickname":"",
                  "gamesInCommon":{
                     "totalCount":3,
                     "__typename":"GamesConnection"
                  },
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
