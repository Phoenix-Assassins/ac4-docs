## Raw request

```json
[
   {
      "operationName":"GetAchievements",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
         "productId":437
      },
      "query":"query GetAchievements($spaceId: String!, $productId: Int) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        achievements(productId: $productId) {\n          totalCount\n          completedCount\n          nodes {\n            ...AchievementFragment\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment AchievementFragment on Achievement {\n  id\n  achievementId\n  title\n  description\n  icon\n  viewer {\n    meta {\n      id\n      completionDate\n      isCompleted\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetAchievements($spaceId: String!, $productId: Int) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        achievements(productId: $productId) {
          totalCount
          completedCount
          nodes {
            ...AchievementFragment
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

fragment AchievementFragment on Achievement {
  id
  achievementId
  title
  description
  icon
  viewer {
    meta {
      id
      completionDate
      isCompleted
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
                  "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
                  "achievements":{
                     "totalCount":60,
                     "completedCount":29,
                     "nodes":[
                        {
                           "id":"437-1",
                           "achievementId":1,
                           "title":"Heroes Aren't Born",
                           "description":"Complete memory sequence 1.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_1.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-1",
                                 "completionDate":"2025-08-14T02:10:13",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-2",
                           "achievementId":2,
                           "title":"Good While It Lasted",
                           "description":"Complete memory sequence 2.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_2.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-2",
                                 "completionDate":"2025-08-29T02:44:29",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-3",
                           "achievementId":3,
                           "title":"A Pirate's Life For Me",
                           "description":"Complete memory sequence 3.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_3.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-3",
                                 "completionDate":"2025-10-12T01:13:49",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-4",
                           "achievementId":4,
                           "title":"No Apologies",
                           "description":"Complete memory sequence 4.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_4.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-4",
                                 "completionDate":"2025-10-16T02:18:25",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-5",
                           "achievementId":5,
                           "title":"Death Of A Salesman",
                           "description":"Complete memory sequence 5.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_5.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-5",
                                 "completionDate":"2025-10-18T15:41:26",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-6",
                           "achievementId":6,
                           "title":"Mixing Up The Medicines",
                           "description":"Complete memory sequence 6.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_6.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-6",
                                 "completionDate":"2025-10-18T23:04:35",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-7",
                           "achievementId":7,
                           "title":"The Hammer Falls",
                           "description":"Complete memory sequence 7.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_7.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-7",
                                 "completionDate":"2025-10-19T00:44:01",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-8",
                           "achievementId":8,
                           "title":"Adrift",
                           "description":"Complete memory sequence 8.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_8.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-8",
                                 "completionDate":"2025-10-19T01:51:39",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-9",
                           "achievementId":9,
                           "title":"A New Hope",
                           "description":"Complete memory sequence 9.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_9.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-9",
                                 "completionDate":"2025-10-19T03:08:46",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-10",
                           "achievementId":10,
                           "title":"My Elusive Fortune",
                           "description":"Complete memory sequence 10.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_10.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-10",
                                 "completionDate":"2025-10-19T05:29:09",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-11",
                           "achievementId":11,
                           "title":"Been Down So Long...",
                           "description":"Complete memory sequence 11.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_11.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-11",
                                 "completionDate":"2025-10-19T06:21:34",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-12",
                           "achievementId":12,
                           "title":"Just Like Starting Over",
                           "description":"Complete memory sequence 12.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_12.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-12",
                                 "completionDate":"2025-10-19T07:53:42",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-13",
                           "achievementId":13,
                           "title":"Saw That One Coming...",
                           "description":"Complete memory sequence 13.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_13.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-13",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-14",
                           "achievementId":14,
                           "title":"Routine Hacking",
                           "description":"Complete present day mission 2.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_14.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-14",
                                 "completionDate":"2025-10-12T01:26:32",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-15",
                           "achievementId":15,
                           "title":"Getting Weird Around Here",
                           "description":"Complete present day mission 3.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_15.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-15",
                                 "completionDate":"2025-10-18T23:24:55",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-16",
                           "achievementId":16,
                           "title":"Bunker Buddies",
                           "description":"Complete present day mission 4.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_16.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-16",
                                 "completionDate":"2025-10-19T05:43:13",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-17",
                           "achievementId":17,
                           "title":"It's All Good",
                           "description":"Complete present day mission 5.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_17.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-17",
                                 "completionDate":"2025-10-19T07:59:33",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-18",
                           "achievementId":18,
                           "title":"By The Book",
                           "description":"Complete 100% of all main mission constraints.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_18.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-18",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-19",
                           "achievementId":19,
                           "title":"Hungover",
                           "description":"Wake up in a haystack.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_19.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-19",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-20",
                           "achievementId":20,
                           "title":"Silence, Fool!",
                           "description":"Kill a guard ringing a bell.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_20.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-20",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-21",
                           "achievementId":21,
                           "title":"Owned",
                           "description":"Complete every activity in a single location.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_21.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-21",
                                 "completionDate":"2025-08-27T00:51:39",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-22",
                           "achievementId":22,
                           "title":"Vault Raider",
                           "description":"Unlock the secret door in Tulum.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_22.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-22",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-23",
                           "achievementId":23,
                           "title":"Killer Killer",
                           "description":"Harpoon a killer whale.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_23.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-23",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-24",
                           "achievementId":24,
                           "title":"Help A Brother Out",
                           "description":"Complete a Templar Hunt sequence.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_24.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-24",
                                 "completionDate":"2025-10-16T01:27:52",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-25",
                           "achievementId":25,
                           "title":"Sea Legs",
                           "description":"Complete all naval contracts.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_25.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-25",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-26",
                           "achievementId":26,
                           "title":"King Of The Castle",
                           "description":"Capture all forts.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_26.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-26",
                                 "completionDate":"2025-10-18T21:10:12",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-27",
                           "achievementId":27,
                           "title":"Employee Of The Month",
                           "description":"Complete 25 Abstergo challenges.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_27.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-27",
                                 "completionDate":"2025-10-06T02:32:47",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-28",
                           "achievementId":28,
                           "title":"Business And Pleasure",
                           "description":"Earn 50,000 reales.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_28.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-28",
                                 "completionDate":"2025-10-06T02:34:49",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-29",
                           "achievementId":29,
                           "title":"Mer-man",
                           "description":"Swim a total of 1 nmi.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_29.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-29",
                                 "completionDate":"2025-10-06T02:12:36",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-30",
                           "achievementId":30,
                           "title":"Redingote Up!",
                           "description":"Craft the Hunter outfit.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_30.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-30",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-31",
                           "achievementId":31,
                           "title":"Thug Life",
                           "description":"Plunder 30 ships.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_31.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-31",
                                 "completionDate":"2025-10-17T20:16:37",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-32",
                           "achievementId":32,
                           "title":"Devil Of The Caribbean",
                           "description":"Defeat all 4 legendary ships.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_32.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-32",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-33",
                           "achievementId":33,
                           "title":"Destroyer",
                           "description":"Fully upgrade the Jackdaw.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_33.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-33",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-34",
                           "achievementId":34,
                           "title":"Seven Deadly Seas",
                           "description":"Explore all underwater shipwrecks.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_34.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-34",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-35",
                           "achievementId":35,
                           "title":"Barfly",
                           "description":"Unlock all taverns.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_35.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-35",
                                 "completionDate":"2025-10-18T19:06:28",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-36",
                           "achievementId":36,
                           "title":"Cannon fodder",
                           "description":"Recruit 500 crew members.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_36.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-36",
                                 "completionDate":"2025-10-19T02:39:28",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-37",
                           "achievementId":37,
                           "title":"FTFY",
                           "description":"Fully upgrade your hideout.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_37.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-37",
                                 "completionDate":"2025-10-19T00:46:25",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-38",
                           "achievementId":38,
                           "title":"Cartographer",
                           "description":"Visit every location of the game.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_38.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-38",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-39",
                           "achievementId":39,
                           "title":"Ghost In The Machine",
                           "description":"Hack 15 computers in Abstergo Entertainment.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_39.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-39",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-40",
                           "achievementId":40,
                           "title":"Roped In",
                           "description":"Perform 5 air assassinations from a swinging rope.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_40.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-40",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-41",
                           "achievementId":41,
                           "title":"Sharing Is Caring",
                           "description":"Share each type of discovery with friends once.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_41.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-41",
                                 "completionDate":"2025-10-15T04:09:16",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-42",
                           "achievementId":42,
                           "title":"All Aboard!",
                           "description":"Board a ship without losing any crew members.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_42.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-42",
                                 "completionDate":"2025-10-06T00:46:02",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-43",
                           "achievementId":43,
                           "title":"Siren Song",
                           "description":"Rescue pirate hostages by distracting enemies with \"dancers.\"",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_43.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-43",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-44",
                           "achievementId":44,
                           "title":"Wild West Indies",
                           "description":"Kill 4 enemies in a row using multi-pistols.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_44.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-44",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-45",
                           "achievementId":45,
                           "title":"Excavator",
                           "description":"Find a buried treasure.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_45.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-45",
                                 "completionDate":"2025-08-14T02:06:12",
                                 "isCompleted":true,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-46",
                           "achievementId":46,
                           "title":"Committed To The Cause",
                           "description":"Reach level 55 in Multiplayer.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_46.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-46",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-47",
                           "achievementId":47,
                           "title":"Personal Bag Of Tricks",
                           "description":"Finish a game session with an ability set that you customized in Multiplayer.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_47.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-47",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-48",
                           "achievementId":48,
                           "title":"Master Of The Caribbean",
                           "description":"Complete the Discovery Mode of Wolfpack in Multiplayer.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_48.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-48",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-49",
                           "achievementId":49,
                           "title":"Lab Technician",
                           "description":"Play and complete a game session of Game Lab in the Multiplayer Public playlist.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_49.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-49",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-50",
                           "achievementId":50,
                           "title":"All Rounder",
                           "description":"Play on every game mode, and use every ability and ranged weapon once in Multiplayer.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_50.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-50",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-51",
                           "achievementId":51,
                           "title":"Sacred Land",
                           "description":"Playing as The Jaguar, be the highest scoring player of a Domination game session.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_51.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-51",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-52",
                           "achievementId":52,
                           "title":"Queen Anne’s Revenge ",
                           "description":"Playing as Blackbeard, perform an acrobatic kill and a gun kill in less than 10 seconds.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_52.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-52",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-53",
                           "achievementId":53,
                           "title":"Preemptive Strike ",
                           "description":"Playing as The Orchid, block 10 abilities from opponents with Sabotage.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_53.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-53",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-54",
                           "achievementId":54,
                           "title":"Elevator to the Gallows ",
                           "description":"Kill a player using a lift that has been trapped with Booby Trap.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_54.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-54",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-55",
                           "achievementId":55,
                           "title":"Liberation Day",
                           "description":"Free your first slave.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_55.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-55",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-56",
                           "achievementId":56,
                           "title":"Seeds of independence",
                           "description":"Liberate 500 slaves.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_56.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-56",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-57",
                           "achievementId":57,
                           "title":"Firepower",
                           "description":"Kill 5 guards at once with a blunderbuss.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_57.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-57",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-58",
                           "achievementId":58,
                           "title":"His Own Medicine",
                           "description":"Disarm the Gouverneur and kill him with the branding iron.",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_58.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-58",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-59",
                           "achievementId":59,
                           "title":"His Word Was “Perhaps”",
                           "description":"Freedom Cry - Complete all missions",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_59.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-59",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        },
                        {
                           "id":"437-60",
                           "achievementId":60,
                           "title":"His Full Attention",
                           "description":"Freedom Cry - Achieve 100% synchronization",
                           "icon":"https://ubiservices.cdn.ubi.com/10322023-976e-49e7-8e02-df5325c868bf/achievement/9e04a2a27dfa06c6713c04523bd36c9a_60.png",
                           "viewer":{
                              "meta":{
                                 "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-437-60",
                                 "completionDate":null,
                                 "isCompleted":false,
                                 "__typename":"UserAchievementMeta"
                              },
                              "__typename":"AchievementUserEdge"
                           },
                           "__typename":"Achievement"
                        }
                     ],
                     "__typename":"UserGameAchievementsConnection"
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
