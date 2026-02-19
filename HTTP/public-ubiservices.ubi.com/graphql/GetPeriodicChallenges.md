## Raw request

```json
[
   {
      "operationName":"GetPeriodicChallenges",
      "variables":{
         "spaceId":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52"
      },
      "query":"query GetPeriodicChallenges($spaceId: String!) {\n  game(spaceId: $spaceId) {\n    id\n    viewer {\n      meta {\n        id\n        currencyPrizes: periodicChallengePrizes(\n          filterBy: {periodicChallengePrize: {type: CURRENCY}}\n        ) {\n          ...PrizeFragment\n          __typename\n        }\n        itemPrizes: periodicChallengePrizes(\n          filterBy: {periodicChallengePrize: {type: ITEM}}\n        ) {\n          ...PrizeFragment\n          __typename\n        }\n        rewardPrizes: periodicChallengePrizes(\n          filterBy: {periodicChallengePrize: {type: REWARD}}\n        ) {\n          ...PrizeFragment\n          __typename\n        }\n        activatedChallengesXp: periodicChallenges(\n          filterBy: {periodicChallenge: {isExpired: false}}\n        ) {\n          totalXpCount\n          xpEarnedCount\n          __typename\n        }\n        periodicChallenges {\n          totalCount\n          challenges: nodes {\n            ...PeriodicChallengeFragment\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment PrizeFragment on UserGamePeriodicChallengePrizesConnection {\n  totalCount\n  collectedValuesCount\n  totalValuesCount\n  edges {\n    meta {\n      id\n      count\n      collectedCount\n      __typename\n    }\n    node {\n      id\n      imageUrl\n      name\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment PeriodicChallengeFragment on PeriodicChallenge {\n  id\n  challengeId\n  startDate\n  endDate\n  isExpired\n  xpPrize\n  operation\n  description\n  imageUrl\n  name\n  previewUrl\n  target: valueV2\n  type\n  currencyPrizes: prizes(filterBy: {type: CURRENCY}) {\n    nodes {\n      id\n      imageUrl\n      name\n      __typename\n    }\n    __typename\n  }\n  itemPrizes: prizes(filterBy: {type: ITEM}) {\n    nodes {\n      id\n      imageUrl\n      name\n      __typename\n    }\n    __typename\n  }\n  rewardPrizes: prizes(filterBy: {type: REWARD}) {\n    nodes {\n      id\n      imageUrl\n      name\n      __typename\n    }\n    __typename\n  }\n  viewer {\n    meta {\n      id\n      isActivated\n      isCollectible\n      isCompleted\n      isInProgress\n      completedTimesTotal\n      contribution\n      progressPercentage\n      progress: progressV2\n      __typename\n    }\n    __typename\n  }\n  thresholds {\n    totalCount\n    nodes {\n      id\n      value: valueV2\n      cumulatedValue: cumulatedValueV2\n      xpPrize\n      viewer {\n        meta {\n          id\n          isCollected\n          isCollectible\n          __typename\n        }\n        __typename\n      }\n      currencyPrizes: prizes(filterBy: {type: CURRENCY}) {\n        edges {\n          meta {\n            id\n            value: count\n            __typename\n          }\n          node {\n            id\n            imageUrl\n            name\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      itemPrizes: prizes(filterBy: {type: ITEM}) {\n        edges {\n          meta {\n            id\n            value: count\n            __typename\n          }\n          node {\n            id\n            imageUrl\n            name\n            __typename\n          }\n          __typename\n        }\n        __typename\n      }\n      rewardPrizes: prizes(filterBy: {type: REWARD}) {\n        nodes {\n          id\n          imageUrl\n          name\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetPeriodicChallenges($spaceId: String!) {
  game(spaceId: $spaceId) {
    id
    viewer {
      meta {
        id
        currencyPrizes: periodicChallengePrizes(
          filterBy: {periodicChallengePrize: {type: CURRENCY}}
        ) {
          ...PrizeFragment
          __typename
        }
        itemPrizes: periodicChallengePrizes(
          filterBy: {periodicChallengePrize: {type: ITEM}}
        ) {
          ...PrizeFragment
          __typename
        }
        rewardPrizes: periodicChallengePrizes(
          filterBy: {periodicChallengePrize: {type: REWARD}}
        ) {
          ...PrizeFragment
          __typename
        }
        activatedChallengesXp: periodicChallenges(
          filterBy: {periodicChallenge: {isExpired: false}}
        ) {
          totalXpCount
          xpEarnedCount
          __typename
        }
        periodicChallenges {
          totalCount
          challenges: nodes {
            ...PeriodicChallengeFragment
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

fragment PrizeFragment on UserGamePeriodicChallengePrizesConnection {
  totalCount
  collectedValuesCount
  totalValuesCount
  edges {
    meta {
      id
      count
      collectedCount
      __typename
    }
    node {
      id
      imageUrl
      name
      __typename
    }
    __typename
  }
  __typename
}

fragment PeriodicChallengeFragment on PeriodicChallenge {
  id
  challengeId
  startDate
  endDate
  isExpired
  xpPrize
  operation
  description
  imageUrl
  name
  previewUrl
  target: valueV2
  type
  currencyPrizes: prizes(filterBy: {type: CURRENCY}) {
    nodes {
      id
      imageUrl
      name
      __typename
    }
    __typename
  }
  itemPrizes: prizes(filterBy: {type: ITEM}) {
    nodes {
      id
      imageUrl
      name
      __typename
    }
    __typename
  }
  rewardPrizes: prizes(filterBy: {type: REWARD}) {
    nodes {
      id
      imageUrl
      name
      __typename
    }
    __typename
  }
  viewer {
    meta {
      id
      isActivated
      isCollectible
      isCompleted
      isInProgress
      completedTimesTotal
      contribution
      progressPercentage
      progress: progressV2
      __typename
    }
    __typename
  }
  thresholds {
    totalCount
    nodes {
      id
      value: valueV2
      cumulatedValue: cumulatedValueV2
      xpPrize
      viewer {
        meta {
          id
          isCollected
          isCollectible
          __typename
        }
        __typename
      }
      currencyPrizes: prizes(filterBy: {type: CURRENCY}) {
        edges {
          meta {
            id
            value: count
            __typename
          }
          node {
            id
            imageUrl
            name
            __typename
          }
          __typename
        }
        __typename
      }
      itemPrizes: prizes(filterBy: {type: ITEM}) {
        edges {
          meta {
            id
            value: count
            __typename
          }
          node {
            id
            imageUrl
            name
            __typename
          }
          __typename
        }
        __typename
      }
      rewardPrizes: prizes(filterBy: {type: REWARD}) {
        nodes {
          id
          imageUrl
          name
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
```

## Response

```json
{
   "data":{
      "game":{
         "id":"c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
         "viewer":{
            "meta":{
               "id":"3880b63b-2915-4452-adc9-0fe152b785ac-c8b3f1c6-a246-4ffe-a837-a49d6bb0ce52",
               "currencyPrizes":{
                  "totalCount":0,
                  "collectedValuesCount":0,
                  "totalValuesCount":0,
                  "edges":[],
                  "__typename":"UserGamePeriodicChallengePrizesConnection"
               },
               "itemPrizes":{
                  "totalCount":0,
                  "collectedValuesCount":0,
                  "totalValuesCount":0,
                  "edges":[],
                  "__typename":"UserGamePeriodicChallengePrizesConnection"
               },
               "rewardPrizes":{
                  "totalCount":0,
                  "collectedValuesCount":0,
                  "totalValuesCount":0,
                  "edges":[],
                  "__typename":"UserGamePeriodicChallengePrizesConnection"
               },
               "activatedChallengesXp":{
                  "totalXpCount":0,
                  "xpEarnedCount":0,
                  "__typename":"UserGamePeriodicChallengesConnection"
               },
               "periodicChallenges":{
                  "totalCount":0,
                  "challenges":[],
                  "__typename":"UserGamePeriodicChallengesConnection"
               },
               "__typename":"UserGameMeta"
            },
            "__typename":"GameUserEdge"
         },
         "__typename":"Game"
      }
   }
}
```
