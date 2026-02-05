# FriendSyncProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | SyncFriends | [FriendSyncProtocol::SyncFriends_V1](#friendsyncprotocolsyncfriends_v1) |

# (1) SyncFriends

## FriendSyncProtocol::SyncFriends_V1

### Request

| Type | Name |
|------|------|
| uint32 | friendType |
| qlist<profileid> | friends |

### Response

| Type | Name |
|------|------|
| qlist<profileid> | titleFriends |
