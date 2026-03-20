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
| uint32 | startingRank |
| uint32 | count |
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
| uint32 | boardID |
| uint32 | resetFrequency |

### Response

| Type | Name |
|------|------|
| uint32 | purgeDate |

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
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_resetFrequency |
| qlist\<uint32> | m_statIDs |
| qlist<[profileid](#profileid-structure)> | m_estimatedPIDs |

## profileid ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

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
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_resetFrequency |
| uint32 | m_leaderboardTotalPlayerCount |
| qlist<[PlayerStatSet](#playerstatset-structure)> | m_playerRanks |

## PlayerStatSet ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [profileid](#profileid-structure) | m_playerPID |
| datetime | m_submittedTime |
| qlist<[PropertyVariant](#propertyvariant-structure)> | m_stats |
| uint32 | m_rankStatus |
| uint32 | m_rank |
| variant | m_score |

## PropertyVariant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| variant | m_value |

## PlayerStatUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| qlist\<uint32> | m_contextIDs |
| qlist<[PropertyVariant](#propertyvariant-structure)> | m_stats |

## LeaderboardMilestone ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint8 | unkByte1 |
| uint8 | unkByte2 |
| uint32 | unkUint2 |
