# SharingProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | Share | [SharingProtocol::Share_V1](#sharingprotocolshare_v1) |
| 2 | FetchAllFriendSharedItems | [SharingProtocol::FetchAllFriendSharedItems_V1](#sharingprotocolfetchallfriendshareditems_v1) |
| 3 | FetchFriendSharedItems | [SharingProtocol::FetchFriendSharedItems_V1](#sharingprotocolfetchfriendshareditems_v1) |
| 4 | ClearSharedItems | [SharingProtocol::ClearSharedItems_V1](#sharingprotocolclearshareditems_v1) |

# (1) Share

## SharingProtocol::Share_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr |
| uint32 | unkUint3 |

### Response

This method does not return anything.

# (2) FetchAllFriendSharedItems

## SharingProtocol::FetchAllFriendSharedItems_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<[ShareItem](#shareitem-structure)> | shareItems |

# (3) FetchFriendSharedItems

## SharingProtocol::FetchFriendSharedItems_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[ShareItem](#shareitem-structure)> | shareItems |

# (4) ClearSharedItems

## SharingProtocol::ClearSharedItems_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# Types

## ShareItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr |
| uint32 | unkUint3 |
