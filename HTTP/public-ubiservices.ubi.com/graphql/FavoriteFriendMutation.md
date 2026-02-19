## Raw request

```json
[
   {
      "operationName":"FavoriteFriendMutation",
      "variables":{
         "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
         "isFavorite":true
      },
      "query":"mutation FavoriteFriendMutation($userId: String!, $isFavorite: Boolean!) {\n  favoriteFriend(userId: $userId, isFavorite: $isFavorite) {\n    ...FriendMutationBodyFragment\n    __typename\n  }\n}\n\nfragment FriendMutationBodyFragment on FriendRequestPayload {\n  userId\n  user {\n    ...UserProfileFragment\n    __typename\n  }\n  __typename\n}\n\nfragment UserProfileFragment on User {\n  id\n  userId\n  viewer {\n    meta {\n      id\n      requestStatus\n      isFriend\n      isFavorite\n      isBlocked\n      nickname\n      __typename\n    }\n    __typename\n  }\n  __typename\n}"
   }
]
```

## GQL mutation

```gql
mutation FavoriteFriendMutation($userId: String!, $isFavorite: Boolean!) {
  favoriteFriend(userId: $userId, isFavorite: $isFavorite) {
    ...FriendMutationBodyFragment
    __typename
  }
}

fragment FriendMutationBodyFragment on FriendRequestPayload {
  userId
  user {
    ...UserProfileFragment
    __typename
  }
  __typename
}

fragment UserProfileFragment on User {
  id
  userId
  viewer {
    meta {
      id
      requestStatus
      isFriend
      isFavorite
      isBlocked
      nickname
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
         "favoriteFriend":{
            "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
            "user":{
               "id":"9370b63b-2d13-4352-adb9-0fe152a485ac",
               "userId":"9370b63b-2d13-4352-adb9-0fe152a485ac",
               "viewer":{
                  "meta":{
                     "id":"1feb5434-f1f1-43ff-9a68-590c969789ae-9370b63b-2d13-4352-adb9-0fe152a485ac",
                     "requestStatus":"FRIENDS",
                     "isFriend":true,
                     "isFavorite":true,
                     "isBlocked":false,
                     "nickname":"",
                     "__typename":"UserUserMeta"
                  },
                  "__typename":"UserUserEdge"
               },
               "__typename":"User"
            },
            "__typename":"FriendRequestPayload"
         }
      }
   }
]
```
