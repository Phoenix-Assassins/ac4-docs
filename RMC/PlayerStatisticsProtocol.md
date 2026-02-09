# PlayerStatisticsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | ReadLeaderboardsByRank | [PlayerStatisticsProtocol::ReadLeaderboardsByRank_V1](#playerstatisticsprotocolreadleaderboardsbyrank_v1) |
| 2 | ResetStatistics | [PlayerStatisticsProtocol::ResetStatistics_V1](#playerstatisticsprotocolresetstatistics_v1) |
| 3 | GetStatboardNextPurgeDate | [PlayerStatisticsProtocol::GetStatboardNextPurgeDate_V1](#playerstatisticsprotocolgetstatboardnextpurgedate_v1) |
| 4 | GetMilestones | [PlayerStatisticsProtocol::GetMilestones_V1](#playerstatisticsprotocolgetmilestones_v1) |
| 5 | ForcePlayerRank | [PlayerStatisticsProtocol::ForcePlayerRank_V1](#playerstatisticsprotocolforceplayerrank_v1) |
| 6 | GetStatResetLog | [PlayerStatisticsProtocol::GetStatResetLog_V1](#playerstatisticsprotocolgetstatresetlog_v1) |

# (1) ReadLeaderboardsByRank

## PlayerStatisticsProtocol::ReadLeaderboardsByRank_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| bool | unkBool |
| [LeaderboardQuery](#leaderboardquery-structure) | query |

### Response

| Type | Name |
|------|------|
| [LeaderboardResult](#leaderboardresult-structure) | result1 |
| [LeaderboardResult](#leaderboardresult-structure) | result2 |

# (2) ResetStatistics

## PlayerStatisticsProtocol::ResetStatistics_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<uint32> | unkUints |
| qlist<[PlayerStatUpdate](#playerstatupdate-structure)> | statUpdates |

### Response

This method does not return anything.

# (3) GetStatboardNextPurgeDate

## PlayerStatisticsProtocol::GetStatboardNextPurgeDate_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

### Response

| Type | Name |
|------|------|
| uint32 | nextPurgeDate |

# (4) GetMilestones

## PlayerStatisticsProtocol::GetMilestones_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<[LeaderboardMilestone](#leaderboardmilestone-structure)> | milestones |

# (5) ForcePlayerRank

## PlayerStatisticsProtocol::ForcePlayerRank_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (6) GetStatResetLog

## PlayerStatisticsProtocol::GetStatResetLog_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist\<uint32> | unkUints |

# Types

## LeaderboardQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| qlist\<uint32> | unkUints |
| qlist<[UnkType](#unktype-structure)> | unkObjs |

## UnkType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| uint16 | unkShort1 |
| uint16 | unkShort2 |
| uint16 | unkShort3 |
| uint16 | unkShort4 |
| uint16 | unkShort5 |
| uint16 | unkShort6 |

## LeaderboardResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| qlist<[PlayerStatSet](#playerstatset-structure)> | statSets |

## PlayerStatSet ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| datetime | time |
| qlist<[PropertyVariant](#propertyvariant-structure)> | ranks |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| variant | variant |

## PropertyVariant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| variant | variant |

## PlayerStatUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<uint32> | unkUints |
| qlist<[PropertyVariant](#propertyvariant-structure)> | stats |

## LeaderboardMilestone ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint8 | unkByte1 |
| uint8 | unkByte2 |
| uint32 | unkUint2 |
