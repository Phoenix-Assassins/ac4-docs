## Raw request

```json
[
   {
      "operationName":"GetChallengesRewards",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetChallengesRewards($spaceId: String!) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        periodicChallenges {\n          totalCount\n          __typename\n        }\n        classicChallenges {\n          totalCount\n          __typename\n        }\n        rewards(\n          orderBy: [{field: RARITY, direction: ASC}, {field: IS_NEW, direction: DESC}, {field: IS_LOCKED, direction: ASC}, {field: IS_REDEEMED, direction: ASC}]\n        ) {\n          nodes {\n            ...RewardsDetails\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment RewardsDetails on Reward {\n  id\n  cost\n  count\n  description\n  conditionHTML: condition\n  imageUrl\n  instructionHTML: instruction\n  isNew\n  name\n  rewardId\n  rarity\n  rarityName\n  rarityColor\n  spaceId\n  conditionSets {\n    nodes {\n      id\n      __typename\n    }\n    totalCount\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      isLocked\n      redeemedCount\n      isRedeemed\n      currentCost\n      source\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetChallengesRewards($spaceId: String!) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        periodicChallenges {
          totalCount
          __typename
        }
        classicChallenges {
          totalCount
          __typename
        }
        rewards(
          orderBy: [{field: RARITY, direction: ASC}, {field: IS_NEW, direction: DESC}, {field: IS_LOCKED, direction: ASC}, {field: IS_REDEEMED, direction: ASC}]
        ) {
          nodes {
            ...RewardsDetails
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
}

fragment RewardsDetails on Reward {
  id
  cost
  count
  description
  conditionHTML: condition
  imageUrl
  instructionHTML: instruction
  isNew
  name
  rewardId
  rarity
  rarityName
  rarityColor
  spaceId
  conditionSets {
    nodes {
      id
      __typename
    }
    totalCount
    __typename
  }
  viewer {
    meta {
      id
      isLocked
      redeemedCount
      isRedeemed
      currentCost
      source
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
         "game":{
            "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
            "viewer":{
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                  "periodicChallenges":{
                     "totalCount":0,
                     "__typename":"UserGamePeriodicChallengesConnection"
                  },
                  "classicChallenges":{
                     "totalCount":0,
                     "__typename":"UserGameClassicChallengesConnection"
                  },
                  "rewards":{
                     "nodes":[
                        {
                           "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "cost":20,
                           "count":1,
                           "description":"Equip Edward  with an authentic pirate costume.",
                           "conditionHTML":null,
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD02_legendary.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"Edward The Legend Outfit",
                           "rewardId":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d",
                           "rarity":"LEGENDARY",
                           "rarityName":"Legendary",
                           "rarityColor":"#ff6d00",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":20,
                                 "source":"UbiConnect",
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        },
                        {
                           "id":"b18215dd-a392-20ba-3f47-22dabdd99eac-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "cost":40,
                           "count":1,
                           "description":"Get Lady Black’s Vengeful Daughter outfit for Multiplayer, and customize the Jackdaw with epic items",
                           "conditionHTML":null,
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD04_epic.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"The Vengeful Daughter Pack",
                           "rewardId":"b18215dd-a392-20ba-3f47-22dabdd99eac",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"b18215dd-a392-20ba-3f47-22dabdd99eac-1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":40,
                                 "source":"UbiConnect",
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        },
                        {
                           "id":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "cost":30,
                           "count":1,
                           "description":"Slay your enemies with the Blades of Toledo, and unlock exclusive Multiplayer Profile items.",
                           "conditionHTML":null,
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD03_epic.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"The Blades of Toledo Pack",
                           "rewardId":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd-1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":30,
                                 "source":"UbiConnect",
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        },
                        {
                           "id":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "cost":0,
                           "count":1,
                           "description":"Download Uplay-exclusive Assassin's Creed® IV Black Flag desktop wallpapers for your PC.",
                           "conditionHTML":null,
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/connect/c4d42f50-1b89-4c14-9ac5-6da5a71c2ed3_common.jpg",
                           "instructionHTML":"Go to https://ubisoftconnect.com to download this Reward and start using it.",
                           "isNew":false,
                           "name":"Assassin's Creed® IV Desktop Wallpapers",
                           "rewardId":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4",
                           "rarity":"COMMON",
                           "rarityName":"Common",
                           "rarityColor":"#A0A0A0",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4-1feb5434-f1f1-43ff-9a68-590c969789ae-c7b3f1c6-a246-4ffe-a837-a49d6bc0ce52",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":0,
                                 "source":"UbiConnect",
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        }
                     ],
                     "__typename":"UserGameRewardsConnection"
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
