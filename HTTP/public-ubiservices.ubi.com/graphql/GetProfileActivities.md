## Raw request

```json
[
   {
      "operationName":"GetProfileActivities",
      "variables":{
         "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
         "platforms":[
            
         ],
         "offset":1
      },
      "query":"query GetProfileActivities($userId: String!, $platforms: [PlatformType!], $offset: Int) {\n  user(userId: $userId) {\n    lastPlayedGame {\n      ...UserStatisticsFragment\n      __typename\n    }\n    currentOnlineGame {\n      ...UserStatisticsFragment\n      __typename\n    }\n    ...UserFragment\n    __typename\n  }\n}\n\nfragment UserStatisticsFragment on UserGameEdge {\n  node {\n    id\n    statistics(orderBy: [ORDINAL]) {\n      nodes {\n        id\n        name\n        sort\n        user(userId: $userId) {\n          meta {\n            id\n            formattedScore\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment UserFragment on User {\n  id\n  userId\n  isViewer\n  currentOnlineGame {\n    ...RecentGameFragment\n    __typename\n  }\n  lastPlayedGame {\n    ...RecentGameFragment\n    __typename\n  }\n  lastPlayedGames: games(\n    limit: 2\n    offset: $offset\n    orderBy: [{field: LAST_PLAYED_DATE, direction: DESC}]\n    filterBy: {game: {platforms: $platforms}}\n  ) {\n    edges {\n      meta {\n        id\n        profileId\n        lastPlayedOn {\n          id\n          name\n          type\n          __typename\n        }\n        __typename\n      }\n      node {\n        id\n        spaceId\n        isCrossplaySupported\n        name\n        backgroundUrl\n        logoFlatUrl\n        logoColorUrl\n        platform {\n          id\n          applicationId\n          name\n          type\n          __typename\n        }\n        viewer {\n          meta {\n            id\n            hasPlaySession\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      isFriend\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment RecentGameFragment on UserGameEdge {\n  node {\n    id\n    spaceId\n    name\n    coverUrl: lowBoxArtUrl\n    bannerUrl: backgroundUrl\n    isStatisticsSupported\n    isCrossplaySupported\n    platform {\n      name\n      id\n      type\n      applicationId\n      __typename\n    }\n    viewer {\n      meta {\n        id\n        hasPlaySession\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  meta {\n    id\n    profileId\n    classicChallenges {\n      totalCount\n      completedCount\n      __typename\n    }\n    lastPlayedOn {\n      id\n      name\n      type\n      __typename\n    }\n    completedPeriodicChallenges: periodicChallenges(\n      filterBy: {isCompleted: true, hasContributed: true}\n    ) {\n      totalCount\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetProfileActivities($userId: String!, $platforms: [PlatformType!], $offset: Int) {
  user(userId: $userId) {
    lastPlayedGame {
      ...UserStatisticsFragment
      __typename
    }
    currentOnlineGame {
      ...UserStatisticsFragment
      __typename
    }
    ...UserFragment
    __typename
  }
}

fragment UserStatisticsFragment on UserGameEdge {
  node {
    id
    statistics(orderBy: [ORDINAL]) {
      nodes {
        id
        name
        sort
        user(userId: $userId) {
          meta {
            id
            formattedScore
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
  __typename
}

fragment UserFragment on User {
  id
  userId
  isViewer
  currentOnlineGame {
    ...RecentGameFragment
    __typename
  }
  lastPlayedGame {
    ...RecentGameFragment
    __typename
  }
  lastPlayedGames: games(
    limit: 2
    offset: $offset
    orderBy: [{field: LAST_PLAYED_DATE, direction: DESC}]
    filterBy: {game: {platforms: $platforms}}
  ) {
    edges {
      meta {
        id
        profileId
        lastPlayedOn {
          id
          name
          type
          __typename
        }
        __typename
      }
      node {
        id
        spaceId
        isCrossplaySupported
        name
        backgroundUrl
        logoFlatUrl
        logoColorUrl
        platform {
          id
          applicationId
          name
          type
          __typename
        }
        viewer {
          meta {
            id
            hasPlaySession
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
  viewer {
    meta {
      id
      isFriend
      __typename
    }
    __typename
  }
  __typename
}

fragment RecentGameFragment on UserGameEdge {
  node {
    id
    spaceId
    name
    coverUrl: lowBoxArtUrl
    bannerUrl: backgroundUrl
    isStatisticsSupported
    isCrossplaySupported
    platform {
      name
      id
      type
      applicationId
      __typename
    }
    viewer {
      meta {
        id
        hasPlaySession
        __typename
      }
      __typename
    }
    __typename
  }
  meta {
    id
    profileId
    classicChallenges {
      totalCount
      completedCount
      __typename
    }
    lastPlayedOn {
      id
      name
      type
      __typename
    }
    completedPeriodicChallenges: periodicChallenges(
      filterBy: {isCompleted: true, hasContributed: true}
    ) {
      totalCount
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
            "lastPlayedGame":{
               "node":{
                  "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "statistics":{
                     "nodes":[
                        
                     ],
                     "__typename":"GameStatisticsConnection"
                  },
                  "__typename":"Game",
                  "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "name":"Assassin's Creed® IV Black Flag",
                  "coverUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/boxArt_mobile.jpg",
                  "bannerUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/backgroundAssetId.jpg",
                  "isStatisticsSupported":false,
                  "isCrossplaySupported":true,
                  "platform":{
                     "name":"PC",
                     "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "type":"PC",
                     "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "__typename":"Platform"
                  },
                  "viewer":{
                     "meta":{
                        "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                        "hasPlaySession":true,
                        "__typename":"UserGameMeta"
                     },
                     "__typename":"GameUserEdge"
                  }
               },
               "__typename":"UserGameEdge",
               "meta":{
                  "id":"9370b63b-2d13-4352-adb9-0fe152a485ac-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "profileId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
                  "classicChallenges":{
                     "totalCount":0,
                     "completedCount":0,
                     "__typename":"UserGameClassicChallengesConnection"
                  },
                  "lastPlayedOn":{
                     "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "name":"PC",
                     "type":"PC",
                     "__typename":"Platform"
                  },
                  "completedPeriodicChallenges":{
                     "totalCount":0,
                     "__typename":"UserGamePeriodicChallengesConnection"
                  },
                  "__typename":"UserGameMeta"
               }
            },
            "currentOnlineGame":null,
            "id":"9370b63b-2d13-4352-adb9-0fe152a485ac",
            "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
            "isViewer":false,
            "lastPlayedGames":{
               "edges":[
                  {
                     "meta":{
                        "id":"9370b63b-2d13-4352-adb9-0fe152a485ac-aab6ceb2-2ea5-4d27-9719-cc2cb87395b7",
                        "profileId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
                        "lastPlayedOn":{
                           "id":"2d10b938-06a4-4f79-89b5-a57706032a5f",
                           "name":"PC",
                           "type":"PC",
                           "__typename":"Platform"
                        },
                        "__typename":"UserGameMeta"
                     },
                     "node":{
                        "id":"aab6ceb2-2ea5-4d27-9719-cc2cb87395b7",
                        "spaceId":"aab6ceb2-2ea5-4d27-9719-cc2cb87395b7",
                        "isCrossplaySupported":false,
                        "name":"Far Cry® 4",
                        "backgroundUrl":"https://ubiservices.cdn.ubi.com/aab6ceb2-2ea5-4d27-9719-cc2cb87395b7/applicationCardAsset/FCC35e0.jpg",
                        "logoFlatUrl":"https://ubiservices.cdn.ubi.com/aab6ceb2-2ea5-4d27-9719-cc2cb87395b7/spaceCardAsset/LogoColor.png",
                        "logoColorUrl":"https://ubiservices.cdn.ubi.com/aab6ceb2-2ea5-4d27-9719-cc2cb87395b7/spaceCardAsset/Connect_Game_Logo_Color_Asset.png",
                        "platform":{
                           "id":"2d10b938-06a4-4f79-89b5-a57706032a5f",
                           "applicationId":"2d10b938-06a4-4f79-89b5-a57706032a5f",
                           "name":"PC",
                           "type":"PC",
                           "__typename":"Platform"
                        },
                        "viewer":{
                           "meta":{
                              "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-aab6ceb2-2ea5-4d27-9719-cc2cb87395b7",
                              "hasPlaySession":false,
                              "__typename":"UserGameMeta"
                           },
                           "__typename":"GameUserEdge"
                        },
                        "__typename":"Game"
                     },
                     "__typename":"UserGameEdge"
                  },
                  {
                     "meta":{
                        "id":"9370b63b-2d13-4352-adb9-0fe152a485ac-6678eff0-1293-4f87-8c8c-06a4ca646068",
                        "profileId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
                        "lastPlayedOn":{
                           "id":"697a073a-83f3-46af-9da7-0d0b0a8a2366",
                           "name":"PC",
                           "type":"PC",
                           "__typename":"Platform"
                        },
                        "__typename":"UserGameMeta"
                     },
                     "node":{
                        "id":"6678eff0-1293-4f87-8c8c-06a4ca646068",
                        "spaceId":"6678eff0-1293-4f87-8c8c-06a4ca646068",
                        "isCrossplaySupported":false,
                        "name":"Assassin's Creed® Unity",
                        "backgroundUrl":"https://ubiservices.cdn.ubi.com/6678eff0-1293-4f87-8c8c-06a4ca646068/spaceCardAsset/backgroundAssetId2.jpg",
                        "logoFlatUrl":"https://ubiservices.cdn.ubi.com/6678eff0-1293-4f87-8c8c-06a4ca646068/spaceCardAsset/LogoColor.png",
                        "logoColorUrl":"https://ubiservices.cdn.ubi.com/6678eff0-1293-4f87-8c8c-06a4ca646068/spaceCardAsset/LogoColor.png",
                        "platform":{
                           "id":"697a073a-83f3-46af-9da7-0d0b0a8a2366",
                           "applicationId":"697a073a-83f3-46af-9da7-0d0b0a8a2366",
                           "name":"PC",
                           "type":"PC",
                           "__typename":"Platform"
                        },
                        "viewer":{
                           "meta":{
                              "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-6678eff0-1293-4f87-8c8c-06a4ca646068",
                              "hasPlaySession":true,
                              "__typename":"UserGameMeta"
                           },
                           "__typename":"GameUserEdge"
                        },
                        "__typename":"Game"
                     },
                     "__typename":"UserGameEdge"
                  }
               ],
               "__typename":"UserGamesConnection"
            },
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-9370b63b-2d13-4352-adb9-0fe152a485ac",
                  "isFriend":true,
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
