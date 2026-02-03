# FriendsLeagueProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | getCurrentGoals | [FriendsLeagueProtocol::getCurrentGoals_V1](#friendsleagueprotocolgetcurrentgoals_v1) |
| 2 | savePlayerProgress | [FriendsLeagueProtocol::savePlayerProgress_V1](#friendsleagueprotocolsaveplayerprogress_v1) |

# (1) getCurrentGoals

## FriendsLeagueProtocol::getCurrentGoals_V1

### Request
This method does not take any parameters.

### Response
| Type | Name |
|------|------|
| qlist\<[FriendsLeagueGoal](#FriendsLeagueGoal)\> | goals |
| uint64 | unkUint |
| datetime | time |

# (2) savePlayerProgress

## FriendsLeagueProtocol::savePlayerProgress_V1

### Request
| Type | Name |
|------|------|
| uint64 | unkUint |

### Response
This method does not return anything.

# Types

## FriendsLeagueGoal ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint8 | unkByte |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
