# ChallengeProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | Search | [ChallengeProtocol::Search_V1](#challengeprotocolsearch_v1) |
| 2 | Join | [ChallengeProtocol::Join_V1](#challengeprotocoljoin_v1) |
| 3 | WriteProgression | [ChallengeProtocol::WriteProgression_V1](#challengeprotocolwriteprogression_v1) |
| 4 | ReadProgressions | [ChallengeProtocol::ReadProgressions_V1](#challengeprotocolreadprogressions_v1) |

# (1) Search

## ChallengeProtocol::Search_V1

### Request

| Type | Name |
|------|------|
| ChallengeSearchQuery | query |

### Response

| Type | Name |
|------|------|
| ChallengeSearchResult | result |

# (2) Join

## ChallengeProtocol::Join_V1

### Request

| Type | Name |
|------|------|
| ChallengeJoinData | joinData |

### Response

This method does not return anything.

# (3) WriteProgression

## ChallengeProtocol::WriteProgression_V1

### Request

| Type | Name |
|------|------|
| ChallengeProgressionUpdate | challengeProgressionUpdate |

### Response

| Type | Name |
|------|------|
| ChallengeProgression | challengeProgression |

# (4) ReadProgressions

## ChallengeProtocol::ReadProgressions_V1

### Request

| Type | Name |
|------|------|
| ChallengeProgressionQuery | query |

### Response

| Type | Name |
|------|------|
| qlist<ChallengeProgression> | results |

# Types

## ChallengeDefinition ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_challengeId |
| string | m_category |
| uint32 | m_availability |
| datetime | m_startTeaseTime |
| datetime | m_startAvailabilityTime |
| datetime | m_endAvailabilityTime |
| std_map<string,variant> | m_joinParams |
| std_map<string,variant> | m_progressionParams |
| std_map<string,variant> | m_extraParams |
| std_map<string,string> | m_localizedStrings |
| bool | m_hasJoined |

## ChallengeSearchQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<uint32> | m_availabilities |
| qlist<string> | m_categories |
| uint32 | m_joinStatus |
| ResultRange | m_range |

## ChallengeSearchResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<ChallengeDefinition> | m_challengeDefinitions |
| uint32 | m_totalResultCount |

## Progression ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| std_map<string,variant> | m_parameters |
| datetime | m_lastUpdate |
| uint32 | m_state |

## PlayerProgression ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| datetime | m_joinTime |
| string | m_team |
| Progression | m_progression |

## ChallengeProgression ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_challengeId |
| Progression | m_globalProgression |
| std_map<profileid,PlayerProgression> | m_playerProgressions |
| std_map<string,Progression> | m_teamProgressions |
| std_map<string,variant> | m_returnValues |

## ProgressionQueryElement ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_challengeId |
| qlist<string> | m_teams |

## ChallengeProgressionQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<ProgressionQueryElement> | m_queryElements |
| qlist<profileid> | m_pids |

## ChallengeJoinData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_challengeId |
| std_map<string,variant> | m_joinParams |

## ChallengeProgressionUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_challengeId |
| std_map<string,variant> | m_progressionParams |
