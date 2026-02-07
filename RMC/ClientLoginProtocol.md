# ClientLoginProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | authenticate | [ClientLoginProtocol::authenticate_V1](#clientloginprotocolauthenticate_v1) |
| 2 | recommend | [ClientLoginProtocol::recommend_V1](#clientloginprotocolrecommend_v1) |
| 3 | getFriendStatus | [ClientLoginProtocol::getFriendStatus_V1](#clientloginprotocolgetfriendstatus_v1) |
| 4 | getServerTime | [ClientLoginProtocol::getServerTime_V1](#clientloginprotocolgetservertime_v1) |
| 5 | getCXBVersion | [ClientLoginProtocol::getCXBVersion_V1](#clientloginprotocolgetcxbversion_v1) |
| 6 | onCXBChanged | [ClientLoginProtocol::onCXBChanged_V1](#clientloginprotocoloncxbchanged_v1) |
| 7 | getCommunityEffort | [ClientLoginProtocol::getCommunityEffort_V1](#clientloginprotocolgetcommunityeffort_v1) |
| 8 | test_rpc | [ClientLoginProtocol::test_rpc_V1](#clientloginprotocoltest_rpc_v1) |
| 9 | isCurrentUserInGame | [ClientLoginProtocol::isCurrentUserInGame_V1](#clientloginprotocoliscurrentuseringame_v1) |
| 10 | updateClanTagWEB | [ClientLoginProtocol::updateClanTagWEB_V1](#clientloginprotocolupdateclantagweb_v1) |
| 11 | getPBStatus | [ClientLoginProtocol::getPBStatus_V1](#clientloginprotocolgetpbstatus_v1) |

# (1) authenticate

## ClientLoginProtocol::authenticate_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkStr2 |
| string | unkStr3 |
| uint32 | unkUint2 |
| bool | unkBool |

### Response

| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint1 |
| string | unkStr1 |
| string | unkStr2 |
| uint32 | unkUint2 |

# (2) recommend

## ClientLoginProtocol::recommend_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| string | unkStr1 |
| string | unkStr2 |

### Response

| Type | Name |
|------|------|
| bool | unkBool1 |
| bool | unkBool2 |

# (3) getFriendStatus

## ClientLoginProtocol::getFriendStatus_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| string | unkStr |
| qlist<string> | strings |

### Response

| Type | Name |
|------|------|
| bool | unkBool |
| qlist<[FriendInfo](#friendinfo-structure)> | infos |

# (4) getServerTime

## ClientLoginProtocol::getServerTime_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| datetime | serverTime |

# (5) getCXBVersion

## ClientLoginProtocol::getCXBVersion_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | cxbVersion |

# (6) onCXBChanged

## ClientLoginProtocol::onCXBChanged_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (7) getCommunityEffort

## ClientLoginProtocol::getCommunityEffort_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |

# (8) test_rpc

## ClientLoginProtocol::test_rpc_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (9) isCurrentUserInGame

## ClientLoginProtocol::isCurrentUserInGame_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| bool | isInGame |

# (10) updateClanTagWEB

## ClientLoginProtocol::updateClanTagWEB_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (11) getPBStatus

## ClientLoginProtocol::getPBStatus_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| bool | pbEnabled |

# Types

## FriendInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | name |
| uint32 | pid |
| bool | online |
