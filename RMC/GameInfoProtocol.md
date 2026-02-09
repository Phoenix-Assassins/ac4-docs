# GameInfoProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | SetSessionMember | [GameInfoProtocol::SetSessionMember_V1](#gameinfoprotocolsetsessionmember_v1) |
| 2 | RemoveSessionMember | [GameInfoProtocol::RemoveSessionMember_V1](#gameinfoprotocolremovesessionmember_v1) |
| 3 | GetSessionMembersCount | [GameInfoProtocol::GetSessionMembersCount_V1](#gameinfoprotocolgetsessionmemberscount_v1) |
| 4 | GetParticipantsWithParameter | [GameInfoProtocol::GetParticipantsWithParameter_V1](#gameinfoprotocolgetparticipantswithparameter_v1) |
| 5 | GetParticipantsWithOneParameterAndFilter | [GameInfoProtocol::GetParticipantsWithOneParameterAndFilter_V1](#gameinfoprotocolgetparticipantswithoneparameterandfilter_v1) |
| 6 | GetParticipantsByHermesModeInHermesSession | [GameInfoProtocol::GetParticipantsByHermesModeInHermesSession_V1](#gameinfoprotocolgetparticipantsbyhermesmodeinhermessession_v1) |
| 7 | GetFileInfoList | [GameInfoProtocol::GetFileInfoList_V1](#gameinfoprotocolgetfileinfolist_v1) |
| 8 | GetTitleItem | [GameInfoProtocol::GetTitleItem_V1](#gameinfoprotocolgettitleitem_v1) |
| 9 | InsertUserItem | [GameInfoProtocol::InsertUserItem_V1](#gameinfoprotocolinsertuseritem_v1) |
| 10 | RemoveUserItem | [GameInfoProtocol::RemoveUserItem_V1](#gameinfoprotocolremoveuseritem_v1) |
| 11 | GetUserItem | [GameInfoProtocol::GetUserItem_V1](#gameinfoprotocolgetuseritem_v1) |

# (1) SetSessionMember

## GameInfoProtocol::SetSessionMember_V1

### Request

Unused method, paylod unknown.

### Response

This method does not return anything.

# (2) RemoveSessionMember

## GameInfoProtocol::RemoveSessionMember_V1

### Request

Unused method, paylod unknown.

### Response

This method does not return anything.

# (3) GetSessionMembersCount

## GameInfoProtocol::GetSessionMembersCount_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| uint32 | memberCount |

# (4) GetParticipantsWithParameter

## GameInfoProtocol::GetParticipantsWithParameter_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| qlist<[Participant](#participant-structure)> | participants |

# (5) GetParticipantsWithOneParameterAndFilter

## GameInfoProtocol::GetParticipantsWithOneParameterAndFilter_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| qlist<[Participant](#participant-structure)> | participants |

# (6) GetParticipantsByHermesModeInHermesSession

## GameInfoProtocol::GetParticipantsByHermesModeInHermesSession_V1

### Request

| Type | Name |
|------|------|
| uint32 | hermesMode |

### Response

| Type | Name |
|------|------|
| qlist<[Participant](#participant-structure)> | participants |

# (7) GetFileInfoList

## GameInfoProtocol::GetFileInfoList_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr |

### Response

| Type | Name |
|------|------|
| qlist<[FileInfo](#fileinfo-structure)> | fileInfos |

# (8) GetTitleItem

## GameInfoProtocol::GetTitleItem_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

| Type | Name |
|------|------|
| [Buffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#buffer) | buffer |
| bool | unkBool |

# (9) InsertUserItem

## GameInfoProtocol::InsertUserItem_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| bool | unkBool |

# (10) RemoveUserItem

## GameInfoProtocol::RemoveUserItem_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| bool | unkBool |

# (11) GetUserItem

## GameInfoProtocol::GetUserItem_V1

### Request

Unused method, paylod unknown.

### Response

| Type | Name |
|------|------|
| [Buffer](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#buffer) | buffer |
| bool | unkBool |

# Types

## Participant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

## FileInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr |
| uint32 | unkUint |
