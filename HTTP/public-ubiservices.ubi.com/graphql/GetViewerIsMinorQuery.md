## Raw request

```json
[
   {
      "operationName":"GetViewerIsMinorQuery",
      "variables":{},
      "query":"query GetViewerIsMinorQuery {\n  viewer {\n    minor\n    __typename\n  }\n}\n"
   }
]
```

## GQL query

```gql
query GetViewerIsMinorQuery {
  viewer {
    minor
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
            "minor":false,
            "__typename":"User"
         }
      }
   }
]
```
