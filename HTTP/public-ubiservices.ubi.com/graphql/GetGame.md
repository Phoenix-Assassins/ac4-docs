## Raw request

```json
[
   {
      "operationName":"GetGame",
      "variables":{
         "shouldIncludeStatsFields":true,
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetGame($spaceId: String!, $shouldIncludeStatsFields: Boolean = true) {\n  game(spaceId: $spaceId) {\n    ...GameFragment\n    __typename\n  }\n}\n\nfragment GameFragment on Game {\n  id\n  spaceId\n  name\n  description\n  lowBoxArtUrl\n  backgroundUrl\n  logoColorUrl\n  logoFlatUrl\n  lowThumbnailUrl\n  avatarUrl\n  releaseDate\n  platform {\n    ...PlatformFragment\n    __typename\n  }\n  availablePlatformGroups {\n    ...PlatformFragment\n    __typename\n  }\n  availablePlatforms {\n    nodes {\n      ...PlatformFragment\n      __typename\n    }\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      lastPlayedDate\n      playTime @include(if: $shouldIncludeStatsFields)\n      completionPercentage @include(if: $shouldIncludeStatsFields)\n      ownedCrossplayPlatforms {\n        nodes {\n          ...PlatformFragment\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment PlatformFragment on Platform {\n  id\n  name\n  type\n  applicationId\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetGame($spaceId: String!, $shouldIncludeStatsFields: Boolean = true) {
  game(spaceId: $spaceId) {
    ...GameFragment
    __typename
  }
}

fragment GameFragment on Game {
  id
  spaceId
  name
  description
  lowBoxArtUrl
  backgroundUrl
  logoColorUrl
  logoFlatUrl
  lowThumbnailUrl
  avatarUrl
  releaseDate
  platform {
    ...PlatformFragment
    __typename
  }
  availablePlatformGroups {
    ...PlatformFragment
    __typename
  }
  availablePlatforms {
    nodes {
      ...PlatformFragment
      __typename
    }
    __typename
  }
  viewer {
    meta {
      id
      lastPlayedDate
      playTime @include(if: $shouldIncludeStatsFields)
      completionPercentage @include(if: $shouldIncludeStatsFields)
      ownedCrossplayPlatforms {
        nodes {
          ...PlatformFragment
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

fragment PlatformFragment on Platform {
  id
  name
  type
  applicationId
  __typename
}
```

## Response

```json
[
   {
      "data":{
         "game":{
            "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
            "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
            "name":"Assassin's Creed® IV Black Flag",
            "description":"Assassin's Creed® IV Black Flag begins in 1715, when pirates established a lawless republic in the Caribbean and ruled the land and seas. These outlaws paralyzed navies, halted international trade, and plundered vast fortunes. They threatened the power structures that ruled Europe, inspired the imaginations of millions, and left a legacy that still endures.",
            "lowBoxArtUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/boxArt_mobile.jpg",
            "backgroundUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/backgroundAssetId.jpg",
            "logoColorUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/LogoColor.png",
            "logoFlatUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/LogoColor.png",
            "lowThumbnailUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/spaceCardAsset/gameThumbnail_mobile.jpg",
            "avatarUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/Club_Asset/Avatar.jpg",
            "releaseDate":"2013-11-19T00:00:00Z",
            "platform":{
               "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
               "name":"PC",
               "type":"PC",
               "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
               "__typename":"Platform"
            },
            "availablePlatformGroups":[
               [
                  {
                     "id":"66b22534-0c4c-4bb0-b6f6-9674cfc307ce",
                     "name":"Web",
                     "type":"WEB",
                     "applicationId":"66b22534-0c4c-4bb0-b6f6-9674cfc307ce",
                     "__typename":"Platform"
                  },
                  {
                     "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "name":"PC",
                     "type":"PC",
                     "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "__typename":"Platform"
                  }
               ],
               [
                  {
                     "id":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                     "name":"Xbox One",
                     "type":"XONE",
                     "applicationId":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                     "__typename":"Platform"
                  }
               ],
               [
                  {
                     "id":"580db364-b218-4b27-90ff-408a1b9a43cf",
                     "name":"PS4®",
                     "type":"PS4",
                     "applicationId":"580db364-b218-4b27-90ff-408a1b9a43cf",
                     "__typename":"Platform"
                  }
               ],
               [
                  {
                     "id":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                     "name":"PS3™",
                     "type":"PS3",
                     "applicationId":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                     "__typename":"Platform"
                  }
               ],
               [
                  {
                     "id":"af91ec6b-9a93-4326-a74a-068373672a4e",
                     "name":"Xbox 360",
                     "type":"X360",
                     "applicationId":"af91ec6b-9a93-4326-a74a-068373672a4e",
                     "__typename":"Platform"
                  }
               ],
               [
                  {
                     "id":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                     "name":"Wii U",
                     "type":"WII",
                     "applicationId":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                     "__typename":"Platform"
                  }
               ]
            ],
            "availablePlatforms":{
               "nodes":[
                  {
                     "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "name":"PC",
                     "type":"PC",
                     "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                     "__typename":"Platform"
                  },
                  {
                     "id":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                     "name":"Xbox One",
                     "type":"XONE",
                     "applicationId":"e73d0cc7-e623-43df-b22b-5a07b177382a",
                     "__typename":"Platform"
                  },
                  {
                     "id":"580db364-b218-4b27-90ff-408a1b9a43cf",
                     "name":"PS4®",
                     "type":"PS4",
                     "applicationId":"580db364-b218-4b27-90ff-408a1b9a43cf",
                     "__typename":"Platform"
                  },
                  {
                     "id":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                     "name":"PS3™",
                     "type":"PS3",
                     "applicationId":"7034e6a9-6141-4e7b-9b34-26c3eba752d8",
                     "__typename":"Platform"
                  },
                  {
                     "id":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                     "name":"Wii U",
                     "type":"WII",
                     "applicationId":"c46e668b-227b-4b70-8187-faacaebc2ad2",
                     "__typename":"Platform"
                  }
               ],
               "__typename":"PlatformConnection"
            },
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                  "lastPlayedDate":"2026-02-03T21:15:51.621688Z",
                  "playTime":null,
                  "completionPercentage":null,
                  "ownedCrossplayPlatforms":{
                     "nodes":[
                        {
                           "id":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                           "name":"PC",
                           "type":"PC",
                           "applicationId":"b8aa2f37-9356-4bc7-87fe-953ce76fd506",
                           "__typename":"Platform"
                        }
                     ],
                     "__typename":"PlatformConnection"
                  },
                  "__typename":"UserGameMeta"
               },
               "__typename":"GameUserEdge"
            },
            "__typename":"Game"
         }
      }
   }
]
```
