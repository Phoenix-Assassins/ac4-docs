# PlayerStatsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | WriteStats | [PlayerStatsProtocol::WriteStats_V1](#playerstatsprotocolwritestats_v1) |
| 2 | ReadStatsByPlayers | [PlayerStatsProtocol::ReadStatsByPlayers_V1](#playerstatsprotocolreadstatsbyplayers_v1) |
| 3 | ReadStatboardHistory | [PlayerStatsProtocol::ReadStatboardHistory_V1](#playerstatsprotocolreadstatboardhistory_v1) |
| 4 | ReadLeaderboardHistory | [PlayerStatsProtocol::ReadLeaderboardHistory_V1](#playerstatsprotocolreadleaderboardhistory_v1) |
| 5 | ReadStatboardHistoryAggregated | [PlayerStatsProtocol::ReadStatboardHistoryAggregated_V1](#playerstatsprotocolreadstatboardhistoryaggregated_v1) |
| 6 | GetStatboardNextPurgeDate | [PlayerStatsProtocol::GetStatboardNextPurgeDate_V1](#playerstatsprotocolgetstatboardnextpurgedate_v1) |
| 7 | ReadLeaderboardsNearPlayer | [PlayerStatsProtocol::ReadLeaderboardsNearPlayer_V1](#playerstatsprotocolreadleaderboardsnearplayer_v1) |
| 8 | ReadLeaderboardsByRank | [PlayerStatsProtocol::ReadLeaderboardsByRank_V1](#playerstatsprotocolreadleaderboardsbyrank_v1) |
| 9 | ReadLeaderboardsByPlayers | [PlayerStatsProtocol::ReadLeaderboardsByPlayers_V1](#playerstatsprotocolreadleaderboardsbyplayers_v1) |
| 10 | ReadPopulationStats | [PlayerStatsProtocol::ReadPopulationStats_V1](#playerstatsprotocolreadpopulationstats_v1) |
| 11 | ReadPopulationStatsHistory | [PlayerStatsProtocol::ReadPopulationStatsHistory_V1](#playerstatsprotocolreadpopulationstatshistory_v1) |

# (1) WriteStats

## PlayerStatsProtocol::WriteStats_V1

### Request

| Type | Name |
|------|------|
| qlist<PlayerStatUpdate> | playerStatUpdates |

### Response

This method does not return anything.

# (2) ReadStatsByPlayers

## PlayerStatsProtocol::ReadStatsByPlayers_V1

### Request

| Type | Name |
|------|------|
| qlist<profileid> | playerPIDs |
| qlist<StatboardQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<StatboardResult> | results |

# (3) ReadStatboardHistory

## PlayerStatsProtocol::ReadStatboardHistory_V1

### Request

| Type | Name |
|------|------|
| qlist<StatboardHistoryQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<StatboardResult> | results |

# (4) ReadLeaderboardHistory

## PlayerStatsProtocol::ReadLeaderboardHistory_V1

### Request

| Type | Name |
|------|------|
| qlist<LeaderboardHistoryQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<LeaderboardResult> | results |

# (5) ReadStatboardHistoryAggregated

## PlayerStatsProtocol::ReadStatboardHistoryAggregated_V1

### Request

| Type | Name |
|------|------|
| qlist<StatboardHistoryAggregatedQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<StatboardResult> | results |

# (6) GetStatboardNextPurgeDate

## PlayerStatsProtocol::GetStatboardNextPurgeDate_V1

### Request

| Type | Name |
|------|------|
| uint32 | boardID |
| uint32 | resetFrequency |

### Response

| Type | Name |
|------|------|
| datetime | purgeDate |

# (7) ReadLeaderboardsNearPlayer

## PlayerStatsProtocol::ReadLeaderboardsNearPlayer_V1

### Request

| Type | Name |
|------|------|
| profileid | playerPID |
| uint32 | count |
| qlist<LeaderboardQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<LeaderboardResult> | results |

# (8) ReadLeaderboardsByRank

## PlayerStatsProtocol::ReadLeaderboardsByRank_V1

### Request

| Type | Name |
|------|------|
| uint32 | startingRank |
| uint32 | count |
| qlist<LeaderboardQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<LeaderboardResult> | results |

# (9) ReadLeaderboardsByPlayers

## PlayerStatsProtocol::ReadLeaderboardsByPlayers_V1

### Request

| Type | Name |
|------|------|
| qlist<LeaderboardQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<LeaderboardResult> | results |

# (10) ReadPopulationStats

## PlayerStatsProtocol::ReadPopulationStats_V1

### Request

| Type | Name |
|------|------|
| qlist<PopulationStatQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<PopulationStatResult> | results |

# (11) ReadPopulationStatsHistory

## PlayerStatsProtocol::ReadPopulationStatsHistory_V1

### Request

| Type | Name |
|------|------|
| qlist<PopulationStatHistoryQuery> | queries |

### Response

| Type | Name |
|------|------|
| qlist<PopulationStatHistoryResult> | results |

# Types

## PlayerStatUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| qlist<uint32> | m_contextIDs |
| qlist<PropertyVariant> | m_stats |

## PlayerStatSortCriteria ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_sortStatID |
| uint32 | m_sortOrder |

## StatboardQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| qlist<uint32> | m_contextIDs |
| uint32 | m_resetFrequency |
| qlist<uint32> | m_statIDs |
| qlist<PlayerStatSortCriteria> | m_sortCriterias |

## LeaderboardQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_resetFrequency |
| qlist<uint32> | m_statIDs |
| qlist<profileid> | m_estimatedPIDs |

## PlayerStatSet ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| profileid | m_playerPID |
| datetime | m_submittedTime |
| qlist<PropertyVariant> | m_stats |

## StatboardResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_resetFrequency |
| qlist<PlayerStatSet> | m_playerStatSets |
| qlist<PropertyVariant> | m_defaultStatValues |

## PlayerRank ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| PlayerStatSet | m_playerStatSet |
| uint32 | m_rankStatus |
| uint32 | m_rank |
| variant | m_score |

## LeaderboardResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_resetFrequency |
| uint32 | m_leaderboardTotalPlayerCount |
| qlist<PlayerRank> | m_playerRanks |

## DateRange ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| datetime | m_startingDatetime |
| datetime | m_endingDatetime |

## StatboardHistoryQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<profileid> | m_playerPIDs |
| uint32 | m_boardID |
| qlist<uint32> | m_contextIDs |
| qlist<uint32> | m_statIDs |
| ResultRange | m_resultRange |
| qlist<PropertyVariant> | m_playerStats |
| qlist<DateRange> | m_dateRanges |
| qlist<PlayerStatSortCriteria> | m_sortCriterias |

## StatboardHistoryAggregatedQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<profileid> | m_playerPIDs |
| uint32 | m_boardID |
| qlist<uint32> | m_contextIDs |
| qlist<uint32> | m_statIDs |
| ResultRange | m_resultRange |
| qlist<PropertyVariant> | m_playerStats |
| qlist<DateRange> | m_dateRanges |
| qlist<PlayerStatSortCriteria> | m_sortCriterias |
| uint32 | m_filterOption |

## LeaderboardHistoryQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<profileid> | m_playerPIDs |
| uint32 | m_boardID |
| uint32 | m_contextID |
| ResultRange | m_resultRange |
| qlist<DateRange> | m_dateRanges |
| uint32 | m_filterOption |

## PopulationStatQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| qlist<uint32> | m_statIDs |

## PopulationStatResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_statID |
| double | m_sum |
| double | m_average |
| double | m_standardDeviation |

## PopulationStatHistoryQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| qlist<uint32> | m_statIDs |
| qlist<datetime> | m_dates |

## PopulationStatHistoryResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_boardID |
| uint32 | m_contextID |
| uint32 | m_statID |
| double | m_sum |
| double | m_average |
| double | m_standardDeviation |
| datetime | m_date |
