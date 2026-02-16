## Raw request

```json
[
   {
      "operationName":"GetNotificationsList",
      "variables":{
         "limit":20
      },
      "query":"query GetNotificationsList($limit: Int, $before: ID, $platforms: [String!]) {\n  viewer {\n    id\n    name\n    notifications(limit: $limit, before: $before, platforms: $platforms) {\n      ...NotificationData\n      __typename\n    }\n    __typename\n  }\n}\n\nfragment NotificationData on NotificationItem {\n  id\n  notificationId\n  message\n  creationDate: createdDate\n  isViewed\n  event {\n    notificationId\n    eventType: type\n    userId\n    ... on CommunityChallengeAvailable {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      challenge {\n        ...NotificationsPeriodicChallenge\n        __typename\n      }\n      __typename\n    }\n    ... on ChallengeAvailable {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      challenge {\n        ...NotificationsPeriodicChallenge\n        __typename\n      }\n      __typename\n    }\n    ... on ChallengeCompleted {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      challenge {\n        ...NotificationsPeriodicChallenge\n        __typename\n      }\n      __typename\n    }\n    ... on CoreChallengeCompleted {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      challenge {\n        ...NotificationsCoreChallenge\n        __typename\n      }\n      __typename\n    }\n    ... on FriendRequestAccepted {\n      friend {\n        ...NotificationsFriend\n        __typename\n      }\n      __typename\n    }\n    ... on FriendRequestReceived {\n      friend {\n        ...NotificationsFriend\n        __typename\n      }\n      __typename\n    }\n    ... on ReferralProgramInvited {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      __typename\n    }\n    ... on ReferralProgramInviteeRewarded {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      __typename\n    }\n    ... on ReferralProgramReferrerRewarded {\n      game {\n        ...NotificationsGame\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment NotificationsGame on Game {\n  id\n  name\n  backgroundUrl\n  isCrossplaySupported\n  platform {\n    id\n    type\n    name\n    applicationId\n    __typename\n  }\n  spaceId\n  viewer {\n    meta {\n      id\n      lastPlayedOn {\n        id\n        type\n        name\n        __typename\n      }\n      ownedCrossplayPlatforms {\n        nodes {\n          id\n          name\n          __typename\n        }\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}\n\nfragment NotificationsPeriodicChallenge on PeriodicChallenge {\n  id\n  imageUrl\n  type\n  challengeId\n  __typename\n}\n\nfragment NotificationsCoreChallenge on ClassicChallenge {\n  id\n  icon\n  type: __typename\n  challengeId\n}\n\nfragment NotificationsFriend on User {\n  id\n  userId\n  avatarUrl\n  name\n  networks {\n    edges {\n      meta {\n        name\n        __typename\n      }\n      node {\n        publicCodeName\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL query

```gql
query GetNotificationsList($limit: Int, $before: ID, $platforms: [String!]) {
  viewer {
    id
    name
    notifications(limit: $limit, before: $before, platforms: $platforms) {
      ...NotificationData
      __typename
    }
    __typename
  }
}

fragment NotificationData on NotificationItem {
  id
  notificationId
  message
  creationDate: createdDate
  isViewed
  event {
    notificationId
    eventType: type
    userId
    ... on CommunityChallengeAvailable {
      game {
        ...NotificationsGame
        __typename
      }
      challenge {
        ...NotificationsPeriodicChallenge
        __typename
      }
      __typename
    }
    ... on ChallengeAvailable {
      game {
        ...NotificationsGame
        __typename
      }
      challenge {
        ...NotificationsPeriodicChallenge
        __typename
      }
      __typename
    }
    ... on ChallengeCompleted {
      game {
        ...NotificationsGame
        __typename
      }
      challenge {
        ...NotificationsPeriodicChallenge
        __typename
      }
      __typename
    }
    ... on CoreChallengeCompleted {
      game {
        ...NotificationsGame
        __typename
      }
      challenge {
        ...NotificationsCoreChallenge
        __typename
      }
      __typename
    }
    ... on FriendRequestAccepted {
      friend {
        ...NotificationsFriend
        __typename
      }
      __typename
    }
    ... on FriendRequestReceived {
      friend {
        ...NotificationsFriend
        __typename
      }
      __typename
    }
    ... on ReferralProgramInvited {
      game {
        ...NotificationsGame
        __typename
      }
      __typename
    }
    ... on ReferralProgramInviteeRewarded {
      game {
        ...NotificationsGame
        __typename
      }
      __typename
    }
    ... on ReferralProgramReferrerRewarded {
      game {
        ...NotificationsGame
        __typename
      }
      __typename
    }
    __typename
  }
  __typename
}

fragment NotificationsGame on Game {
  id
  name
  backgroundUrl
  isCrossplaySupported
  platform {
    id
    type
    name
    applicationId
    __typename
  }
  spaceId
  viewer {
    meta {
      id
      lastPlayedOn {
        id
        type
        name
        __typename
      }
      ownedCrossplayPlatforms {
        nodes {
          id
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

fragment NotificationsPeriodicChallenge on PeriodicChallenge {
  id
  imageUrl
  type
  challengeId
  __typename
}

fragment NotificationsCoreChallenge on ClassicChallenge {
  id
  icon
  type: __typename
  challengeId
}

fragment NotificationsFriend on User {
  id
  userId
  avatarUrl
  name
  networks {
    edges {
      meta {
        name
        __typename
      }
      node {
        publicCodeName
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
         "viewer":{
            "id":"1feb5434-f1f1-43ff-9a68-590c969789ae",
            "name":"Mim4k",
            "notifications":[
               {
                  "id":"6982653d1408184310b55cb2",
                  "notificationId":"6982653d1408184310b55cb2",
                  "message":"Sent you a friend request.",
                  "creationDate":"2026-02-03T21:14:37.005Z",
                  "isViewed":false,
                  "event":{
                     "notificationId":"6982653d1408184310b55cb2",
                     "eventType":"FriendRequestReceived",
                     "userId":"1feb5434-f1f1-43ff-9a68-590c969789ae",
                     "friend":{
                        "id":"c6e3c5f3-3a44-4099-85cb-4caa968b6813",
                        "userId":"c6e3c5f3-3a44-4099-85cb-4caa968b6813",
                        "avatarUrl":"https://ubiservices.cdn.ubi.com/77560d22-668e-40ad-a445-69ae77826b40/static/cf82b7c3_58d9_49bc_b1ac_a9e51f35c624.png?rs=146",
                        "name":"henrickjack",
                        "networks":{
                           "edges":[
                              {
                                 "meta":{
                                    "name":"henrickjack",
                                    "__typename":"UserNetworkMeta"
                                 },
                                 "node":{
                                    "publicCodeName":"UPLAY",
                                    "__typename":"Network"
                                 },
                                 "__typename":"UserNetworkEdge"
                              },
                              {
                                 "meta":{
                                    "name":"76561198799363538",
                                    "__typename":"UserNetworkMeta"
                                 },
                                 "node":{
                                    "publicCodeName":"STEAM",
                                    "__typename":"Network"
                                 },
                                 "__typename":"UserNetworkEdge"
                              }
                           ],
                           "__typename":"UserNetworksConnection"
                        },
                        "__typename":"User"
                     },
                     "__typename":"FriendRequestReceived"
                  },
                  "__typename":"NotificationItem"
               }
            ],
            "__typename":"User"
         }
      }
   }
]
```
