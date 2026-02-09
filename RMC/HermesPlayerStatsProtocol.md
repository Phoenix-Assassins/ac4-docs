# HermesPlayerStatsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | WriteStats | [HermesPlayerStatsProtocol::WriteStats_V1](#hermesplayerstatsprotocolwritestats_v1) |
| 2 | WritePlayerStats | [HermesPlayerStatsProtocol::WritePlayerStats_V1](#hermesplayerstatsprotocolwriteplayerstats_v1) |
| 3 | ReadPlayerStats | [HermesPlayerStatsProtocol::ReadPlayerStats_V1](#hermesplayerstatsprotocolreadplayerstats_v1) |
| 4 | ReadClanStats | [HermesPlayerStatsProtocol::ReadClanStats_V1](#hermesplayerstatsprotocolreadclanstats_v1) |
| 5 | ReadStatsLeaderboardByRange | [HermesPlayerStatsProtocol::ReadStatsLeaderboardByRange_V1](#hermesplayerstatsprotocolreadstatsleaderboardbyrange_v1) |
| 6 | ReadStatsLeaderboardByRangeClan | [HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeClan_V1](#hermesplayerstatsprotocolreadstatsleaderboardbyrangeclan_v1) |
| 7 | ReadStatsLeaderboardByRangeForPlayer | [HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeForPlayer_V1](#hermesplayerstatsprotocolreadstatsleaderboardbyrangeforplayer_v1) |
| 8 | ReadStatsLeaderboardByRangeForPlayerClan | [HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeForPlayerClan_V1](#hermesplayerstatsprotocolreadstatsleaderboardbyrangeforplayerclan_v1) |
| 9 | ReadStatsLeaderboardForPlayers | [HermesPlayerStatsProtocol::ReadStatsLeaderboardForPlayers_V1](#hermesplayerstatsprotocolreadstatsleaderboardforplayers_v1) |
| 10 | ReadStatsLeaderboardFromSlidingTable | [HermesPlayerStatsProtocol::ReadStatsLeaderboardFromSlidingTable_V1](#hermesplayerstatsprotocolreadstatsleaderboardfromslidingtable_v1) |
| 11 | StoreNpId | [HermesPlayerStatsProtocol::StoreNpId_V1](#hermesplayerstatsprotocolstorenpid_v1) |
| 12 | RetrieveNpIds | [HermesPlayerStatsProtocol::RetrieveNpIds_V1](#hermesplayerstatsprotocolretrievenpids_v1) |

# (1) WriteStats

## HermesPlayerStatsProtocol::WriteStats_V1

### Request

Unused method, paylod unknown.

### Response

This method does not return anything.

# (2) WritePlayerStats

## HermesPlayerStatsProtocol::WritePlayerStats_V1

### Request

| Type | Name |
|------|------|
| qlist<[StatisticWriteWithBoard](#statisticwritewithboard-structure)> | stats |

### Response

This method does not return anything.

# (3) ReadPlayerStats

## HermesPlayerStatsProtocol::ReadPlayerStats_V1

### Request

| Type | Name |
|------|------|
| qlist<[StatisticData](#statisticdata-structure)> | statData |
| qlist<[UnkType](#unktype-structure)> | unkObjs |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListRead](#scorelistread-structure)> | scores |

# (4) ReadClanStats

## HermesPlayerStatsProtocol::ReadClanStats_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListReadClan](#scorelistreadclan-structure)> | scores |

# (5) ReadStatsLeaderboardByRange

## HermesPlayerStatsProtocol::ReadStatsLeaderboardByRange_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListRead](#scorelistread-structure)> | scores |
| uint32 | unkUint |

# (6) ReadStatsLeaderboardByRangeClan

## HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeClan_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListReadClan](#scorelistreadclan-structure)> | scores |
| uint32 | unkUint |

# (7) ReadStatsLeaderboardByRangeForPlayer

## HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeForPlayer_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint3 |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListRead](#scorelistread-structure)> | scores |
| uint32 | unkUint |

# (8) ReadStatsLeaderboardByRangeForPlayerClan

## HermesPlayerStatsProtocol::ReadStatsLeaderboardByRangeForPlayerClan_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListReadClan](#scorelistreadclan-structure)> | scores |
| uint32 | unkUint |

# (9) ReadStatsLeaderboardForPlayers

## HermesPlayerStatsProtocol::ReadStatsLeaderboardForPlayers_V1

### Request

| Type | Name |
|------|------|
| qlist<[LeaderboardData](#leaderboarddata-structure)> | leaderboardData |
| qlist<[UnkType](#unktype-structure)> | unkObjs |

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListRead](#scorelistread-structure)> | scores |
| uint32 | unkUint |

# (10) ReadStatsLeaderboardFromSlidingTable

## HermesPlayerStatsProtocol::ReadStatsLeaderboardFromSlidingTable_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[ScoreListRead](#scorelistread-structure)> | scores |

# (11) StoreNpId

## HermesPlayerStatsProtocol::StoreNpId_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (12) RetrieveNpIds

## HermesPlayerStatsProtocol::RetrieveNpIds_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| qBuffer | npIds |

# Types

## StatisticWriteWithBoard ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist<[StatisticWriteValue](#statisticwritevalue-structure)> | values |

## StatisticWriteValue ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint8 | unkByte1 |
| [StatisticValueVariant](#statisticvaluevariant-structure) | variant |
| uint8 | unkByte2 |

## StatisticValueVariant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | uintVal |
| uint64 | longVal |
| double | doubleVal |
| string | strVal |
| uint8 | byteVal |

## ScoreListRead ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| qlist<[StatisticReadValueByBoard](#StatisticReadValueByBoard-structure)> | statsByBoard |

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

## StatisticReadValueByBoard ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| qlist<[StatisticReadValue](#statisticreadvalue-structure)> | values |
| datetime | time |

## StatisticReadValue ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint8 | unkByte1 |
| [StatisticValueVariant](#statisticvaluevariant-structure) | variant1 |
| uint8 | unkByte2 |
| [StatisticValueVariant](#statisticvaluevariant-structure) | variant2 |
| [StatisticValueVariant](#statisticvaluevariant-structure) | variant3 |

## StatisticData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<uint32> | unkUints |

## ScoreListReadClan ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist<[StatisticReadValueByBoard](#statisticreadvaluebyboard-structure)> | statsByBoard |

## LeaderboardData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
