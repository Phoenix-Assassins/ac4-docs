## Raw request

```json
[
   {
      "operationName":"GetRewardList",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetRewardList($spaceId: String!) {\n  viewer {\n    id\n    name\n    unitsBalance\n    game(spaceId: $spaceId) {\n      node {\n        id\n        name\n        __typename\n      }\n      meta {\n        id\n        rewards(\n          orderBy: [{field: COST, direction: DESC}, {field: RARITY, direction: ASC}, {field: IS_NEW, direction: DESC}]\n        ) {\n          nodes {\n            ...RewardsDetailsFragment\n            __typename\n          }\n          __typename\n        }\n        ...RewardsByGroupFragment\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment RewardsDetailsFragment on Reward {\n  id\n  cost\n  count\n  description\n  imageUrl\n  instructionHTML: instruction\n  isNew\n  name\n  rarity\n  rarityName\n  rarityColor\n  rewardId\n  spaceId\n  downloadUrl\n  conditionTreeType\n  conditionsType\n  conditionSets {\n    nodes {\n      id\n      discountedCost\n      discountPercentage\n      conditions {\n        nodes {\n          id\n          description\n          viewer {\n            meta {\n              id\n              isCompleted\n              __typename\n            }\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    totalCount\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      source\n      isLocked\n      redeemedCount\n      isRedeemed\n      currentCost\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment RewardsByGroupFragment on UserGameMeta {\n  id\n  commonRewards: rewards(filterBy: {reward: {rarity: COMMON}}) {\n    ...GameRewardsConnectionFragment\n    __typename\n  }\n  epicRewards: rewards(filterBy: {reward: {rarity: EPIC}}) {\n    ...GameRewardsConnectionFragment\n    __typename\n  }\n  exoticRewards: rewards(filterBy: {reward: {rarity: EXOTIC}}) {\n    ...GameRewardsConnectionFragment\n    __typename\n  }\n  legendaryRewards: rewards(filterBy: {reward: {rarity: LEGENDARY}}) {\n    ...GameRewardsConnectionFragment\n    __typename\n  }\n  rareRewards: rewards(filterBy: {reward: {rarity: RARE}}) {\n    ...GameRewardsConnectionFragment\n    __typename\n  }\n  __typename\n}\n\nfragment GameRewardsConnectionFragment on UserGameRewardsConnection {\n  __typename\n  totalCount\n  purchasesCount\n  totalPurchasesCount\n  nodes {\n    id\n    rewardId\n    rarity\n    rarityName\n    rarityColor\n    viewer {\n      meta {\n        id\n        ownedCount: redeemedCount\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}"
   }
]
```

## GQL query

```gql
query GetRewardList($spaceId: String!) {
  viewer {
    id
    name
    unitsBalance
    game(spaceId: $spaceId) {
      node {
        id
        name
        __typename
      }
      meta {
        id
        rewards(
          orderBy: [{field: COST, direction: DESC}, {field: RARITY, direction: ASC}, {field: IS_NEW, direction: DESC}]
        ) {
          nodes {
            ...RewardsDetailsFragment
            __typename
          }
          __typename
        }
        ...RewardsByGroupFragment
        __typename
      }
      __typename
    }
    __typename
  }
}

fragment RewardsDetailsFragment on Reward {
  id
  cost
  count
  description
  imageUrl
  instructionHTML: instruction
  isNew
  name
  rarity
  rarityName
  rarityColor
  rewardId
  spaceId
  downloadUrl
  conditionTreeType
  conditionsType
  conditionSets {
    nodes {
      id
      discountedCost
      discountPercentage
      conditions {
        nodes {
          id
          description
          viewer {
            meta {
              id
              isCompleted
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
    totalCount
    __typename
  }
  viewer {
    meta {
      id
      source
      isLocked
      redeemedCount
      isRedeemed
      currentCost
      __typename
    }
    __typename
  }
  __typename
}

fragment RewardsByGroupFragment on UserGameMeta {
  id
  commonRewards: rewards(filterBy: {reward: {rarity: COMMON}}) {
    ...GameRewardsConnectionFragment
    __typename
  }
  epicRewards: rewards(filterBy: {reward: {rarity: EPIC}}) {
    ...GameRewardsConnectionFragment
    __typename
  }
  exoticRewards: rewards(filterBy: {reward: {rarity: EXOTIC}}) {
    ...GameRewardsConnectionFragment
    __typename
  }
  legendaryRewards: rewards(filterBy: {reward: {rarity: LEGENDARY}}) {
    ...GameRewardsConnectionFragment
    __typename
  }
  rareRewards: rewards(filterBy: {reward: {rarity: RARE}}) {
    ...GameRewardsConnectionFragment
    __typename
  }
  __typename
}

fragment GameRewardsConnectionFragment on UserGameRewardsConnection {
  __typename
  totalCount
  purchasesCount
  totalPurchasesCount
  nodes {
    id
    rewardId
    rarity
    rarityName
    rarityColor
    viewer {
      meta {
        id
        ownedCount: redeemedCount
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
         "viewer":{
            "id":"1feb5434-f1f1-43ff-9a68-590c969789ae",
            "name":"mimak",
            "unitsBalance":0,
            "game":{
               "node":{
                  "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "name":"Assassin's Creed® IV Black Flag",
                  "__typename":"Game"
               },
               "meta":{
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "rewards":{
                     "nodes":[
                        {
                           "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "cost":20,
                           "count":1,
                           "description":"Equip Edward  with an authentic pirate costume.",
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD02_legendary.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"Edward The Legend Outfit",
                           "rarity":"LEGENDARY",
                           "rarityName":"Legendary",
                           "rarityColor":"#ff6d00",
                           "rewardId":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "downloadUrl":null,
                           "conditionTreeType":null,
                           "conditionsType":null,
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "source":"UbiConnect",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":20,
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
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD04_epic.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"The Vengeful Daughter Pack",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "rewardId":"b18215dd-a392-20ba-3f47-22dabdd99eac",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "downloadUrl":null,
                           "conditionTreeType":null,
                           "conditionsType":null,
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"b18215dd-a392-20ba-3f47-22dabdd99eac-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "source":"UbiConnect",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":40,
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
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD03_epic.jpg",
                           "instructionHTML":"You can access this Reward within the game.",
                           "isNew":false,
                           "name":"The Blades of Toledo Pack",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "rewardId":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "downloadUrl":null,
                           "conditionTreeType":null,
                           "conditionsType":null,
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "source":"UbiConnect",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":30,
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
                           "imageUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/connect/c4d42f50-1b89-4c14-9ac5-6da5a71c2ed3_common.jpg",
                           "instructionHTML":"Go to https://ubisoftconnect.com to download this Reward and start using it.",
                           "isNew":false,
                           "name":"Assassin's Creed® IV Desktop Wallpapers",
                           "rarity":"COMMON",
                           "rarityName":"Common",
                           "rarityColor":"#A0A0A0",
                           "rewardId":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4",
                           "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "downloadUrl":"https://ubiservices.cdn.ubi.com/c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52/reward/ACBFREWARD01PC_downloadable.zip",
                           "conditionTreeType":null,
                           "conditionsType":null,
                           "conditionSets":{
                              "nodes":[
                                 
                              ],
                              "totalCount":0,
                              "__typename":"ConditionSetsConnection"
                           },
                           "viewer":{
                              "meta":{
                                 "id":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "source":"UbiConnect",
                                 "isLocked":false,
                                 "redeemedCount":1,
                                 "isRedeemed":true,
                                 "currentCost":0,
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        }
                     ],
                     "__typename":"UserGameRewardsConnection"
                  },
                  "commonRewards":{
                     "__typename":"UserGameRewardsConnection",
                     "totalCount":1,
                     "purchasesCount":1,
                     "totalPurchasesCount":1,
                     "nodes":[
                        {
                           "id":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "rewardId":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4",
                           "rarity":"COMMON",
                           "rarityName":"Common",
                           "rarityColor":"#A0A0A0",
                           "viewer":{
                              "meta":{
                                 "id":"62cb3405-1a83-45b3-b6f5-61d9fcc0fdf4-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "ownedCount":1,
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        }
                     ]
                  },
                  "epicRewards":{
                     "__typename":"UserGameRewardsConnection",
                     "totalCount":2,
                     "purchasesCount":2,
                     "totalPurchasesCount":2,
                     "nodes":[
                        {
                           "id":"b18215dd-a392-20ba-3f47-22dabdd99eac-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "rewardId":"b18215dd-a392-20ba-3f47-22dabdd99eac",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "viewer":{
                              "meta":{
                                 "id":"b18215dd-a392-20ba-3f47-22dabdd99eac-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "ownedCount":1,
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        },
                        {
                           "id":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "rewardId":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd",
                           "rarity":"EPIC",
                           "rarityName":"Epic",
                           "rarityColor":"#ce00b1",
                           "viewer":{
                              "meta":{
                                 "id":"cee255fe-0262-6b9d-d3c1-a89c8fd58acd-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "ownedCount":1,
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        }
                     ]
                  },
                  "exoticRewards":{
                     "__typename":"UserGameRewardsConnection",
                     "totalCount":0,
                     "purchasesCount":0,
                     "totalPurchasesCount":0,
                     "nodes":[
                        
                     ]
                  },
                  "legendaryRewards":{
                     "__typename":"UserGameRewardsConnection",
                     "totalCount":1,
                     "purchasesCount":1,
                     "totalPurchasesCount":1,
                     "nodes":[
                        {
                           "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                           "rewardId":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d",
                           "rarity":"LEGENDARY",
                           "rarityName":"Legendary",
                           "rarityColor":"#ff6d00",
                           "viewer":{
                              "meta":{
                                 "id":"faa6104a-5ee0-c8e0-5e48-42818e69dd8d-1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                                 "ownedCount":1,
                                 "__typename":"UserRewardMeta"
                              },
                              "__typename":"RewardUserEdge"
                           },
                           "__typename":"Reward"
                        }
                     ]
                  },
                  "rareRewards":{
                     "__typename":"UserGameRewardsConnection",
                     "totalCount":0,
                     "purchasesCount":0,
                     "totalPurchasesCount":0,
                     "nodes":[
                        
                     ]
                  },
                  "__typename":"UserGameMeta"
               },
               "__typename":"UserGameEdge"
            },
            "__typename":"User"
         }
      }
   }
]
```
