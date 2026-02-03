# GameSessionProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | CreateSession | [GameSessionProtocol::CreateSession_V1](#gamesessionprotocolcreatesession_v1) |
| 2 | UpdateSession | [GameSessionProtocol::UpdateSession_V1](#gamesessionprotocolupdatesession_v1) |
| 3 | DeleteSession | [GameSessionProtocol::DeleteSession_V1](#gamesessionprotocoldeletesession_v1) |
| 4 | LeaveSession | [GameSessionProtocol::LeaveSession_V1](#gamesessionprotocolleavesession_v1) |
| 5 | GetSession | [GameSessionProtocol::GetSession_V1](#gamesessionprotocolgetsession_v1) |
| 6 | SearchSessions | [GameSessionProtocol::SearchSessions_V1](#gamesessionprotocolsearchsessions_v1) |
| 7 | AddParticipants | [GameSessionProtocol::AddParticipants_V1](#gamesessionprotocoladdparticipants_v1) |
| 8 | RemoveParticipants | [GameSessionProtocol::RemoveParticipants_V1](#gamesessionprotocolremoveparticipants_v1) |
| 9 | GetParticipantCount | [GameSessionProtocol::GetParticipantCount_V1](#gamesessionprotocolgetparticipantcount_v1) |
| 10 | GetParticipants | [GameSessionProtocol::GetParticipants_V1](#gamesessionprotocolgetparticipants_v1) |
| 11 | SendInvitation | [GameSessionProtocol::SendInvitation_V1](#gamesessionprotocolsendinvitation_v1) |
| 12 | GetInvitationReceivedCount | [GameSessionProtocol::GetInvitationReceivedCount_V1](#gamesessionprotocolgetinvitationreceivedcount_v1) |
| 13 | GetInvitationsReceived | [GameSessionProtocol::GetInvitationsReceived_V1](#gamesessionprotocolgetinvitationsreceived_v1) |
| 14 | GetInvitationSentCount | [GameSessionProtocol::GetInvitationSentCount_V1](#gamesessionprotocolgetinvitationsentcount_v1) |
| 15 | GetInvitationsSent | [GameSessionProtocol::GetInvitationsSent_V1](#gamesessionprotocolgetinvitationssent_v1) |
| 16 | AcceptInvitation | [GameSessionProtocol::AcceptInvitation_V1](#gamesessionprotocolacceptinvitation_v1) |
| 17 | DeclineInvitation | [GameSessionProtocol::DeclineInvitation_V1](#gamesessionprotocoldeclineinvitation_v1) |
| 18 | CancelInvitation | [GameSessionProtocol::CancelInvitation_V1](#gamesessionprotocolcancelinvitation_v1) |
| 19 | SendTextMessage | [GameSessionProtocol::SendTextMessage_V1](#gamesessionprotocolsendtextmessage_v1) |
| 20 | RegisterURLs | [GameSessionProtocol::RegisterURLs_V1](#gamesessionprotocolregisterurls_v1) |
| 21 | JoinSession | [GameSessionProtocol::JoinSession_V1](#gamesessionprotocoljoinsession_v1) |
| 22 | AbandonSession | [GameSessionProtocol::AbandonSession_V1](#gamesessionprotocolabandonsession_v1) |
| 23 | SearchSessionsWithParticipants | [GameSessionProtocol::SearchSessionsWithParticipants_V1](#gamesessionprotocolsearchsessionswithparticipants_v1) |
| 24 | GetSessions | [GameSessionProtocol::GetSessions_V1](#gamesessionprotocolgetsessions_v1) |
| 25 | GetParticipantsURLs | [GameSessionProtocol::GetParticipantsURLs_V1](#gamesessionprotocolgetparticipantsurls_v1) |
| 26 | MigrateHost | [GameSessionProtocol::MigrateHost_V1](#gamesessionprotocolmigratehost_v1) |
| 27 | SplitSession | [GameSessionProtocol::SplitSession_V1](#gamesessionprotocolsplitsession_v1) |
| 28 | SearchSocialSessions | [GameSessionProtocol::SearchSocialSessions_V1](#gamesessionprotocolsearchsocialsessions_v1) |
| 29 | ReportUnsuccessfulJoinSessions | [GameSessionProtocol::ReportUnsuccessfulJoinSessions_V1](#gamesessionprotocolreportunsuccessfuljoinsessions_v1) |

# (1) CreateSession

## GameSessionProtocol::CreateSession_V1

### Request

| Type | Name |
|------|------|
| GameSession | gameSession |

### Response

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

# (2) UpdateSession

## GameSessionProtocol::UpdateSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionUpdate | gameSessionUpdate |

### Response

This method does not return anything.

# (3) DeleteSession

## GameSessionProtocol::DeleteSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

This method does not return anything.

# (4) LeaveSession

## GameSessionProtocol::LeaveSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

This method does not return anything.

# (5) GetSession

## GameSessionProtocol::GetSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

| Type | Name |
|------|------|
| GameSessionSearchResult | searchResult |

# (6) SearchSessions

## GameSessionProtocol::SearchSessions_V1

### Request

| Type | Name |
|------|------|
| GameSessionQuery | gameSessionQuery |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchResult> | searchResults |

# (7) AddParticipants

## GameSessionProtocol::AddParticipants_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<profileid> | publicParticipants |
| qlist<profileid> | privateParticipants |

### Response

This method does not return anything.

# (8) RemoveParticipants

## GameSessionProtocol::RemoveParticipants_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<profileid> | participants |

### Response

This method does not return anything.

# (9) GetParticipantCount

## GameSessionProtocol::GetParticipantCount_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

| Type | Name |
|------|------|
| uint32 | count |

# (10) GetParticipants

## GameSessionProtocol::GetParticipants_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionParticipant> | participants |

# (11) SendInvitation

## GameSessionProtocol::SendInvitation_V1

### Request

| Type | Name |
|------|------|
| GameSessionInvitation | invitation |

### Response

This method does not return anything.

# (12) GetInvitationReceivedCount

## GameSessionProtocol::GetInvitationReceivedCount_V1

### Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |

### Response

| Type | Name |
|------|------|
| uint32 | count |

# (13) GetInvitationsReceived

## GameSessionProtocol::GetInvitationsReceived_V1

### Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionInvitationReceived> | invitations |

# (14) GetInvitationSentCount

## GameSessionProtocol::GetInvitationSentCount_V1

### Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |

### Response

| Type | Name |
|------|------|
| uint32 | count |

# (15) GetInvitationsSent

## GameSessionProtocol::GetInvitationsSent_V1

### Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionInvitationSent> | invitations |

# (16) AcceptInvitation

## GameSessionProtocol::AcceptInvitation_V1

### Request

| Type | Name |
|------|------|
| GameSessionInvitationReceived | gameSessionInvitation |

### Response

This method does not return anything.

# (17) DeclineInvitation

## GameSessionProtocol::DeclineInvitation_V1

### Request

| Type | Name |
|------|------|
| GameSessionInvitationReceived | gameSessionInvitation |

### Response

This method does not return anything.

# (18) CancelInvitation

## GameSessionProtocol::CancelInvitation_V1

### Request

| Type | Name |
|------|------|
| GameSessionInvitationSent | gameSessionInvitation |

### Response

This method does not return anything.

# (19) SendTextMessage

## GameSessionProtocol::SendTextMessage_V1

### Request

| Type | Name |
|------|------|
| GameSessionMessage | gameSessionMessage |

### Response

This method does not return anything.

# (20) RegisterURLs

## GameSessionProtocol::RegisterURLs_V1

### Request

| Type | Name |
|------|------|
| qlist<stationurl> | stationURLs |

### Response

This method does not return anything.

# (21) JoinSession

## GameSessionProtocol::JoinSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

This method does not return anything.

# (22) AbandonSession

## GameSessionProtocol::AbandonSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

This method does not return anything.

# (23) SearchSessionsWithParticipants

## GameSessionProtocol::SearchSessionsWithParticipants_V1

### Request

| Type | Name |
|------|------|
| uint32 | gameSessionTypeID |
| qlist<profileid> | participants |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchWithParticipantsResult> | searchResults |

# (24) GetSessions

## GameSessionProtocol::GetSessions_V1

### Request

| Type | Name |
|------|------|
| qlist<GameSessionKey> | gameSessionKeys |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchResult> | searchResults |

# (25) GetParticipantsURLs

## GameSessionProtocol::GetParticipantsURLs_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |
| qlist<profileid> | participants |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionParticipant> | gameSessionParticipants |

# (26) MigrateHost

## GameSessionProtocol::MigrateHost_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

This method does not return anything.

# (27) SplitSession

## GameSessionProtocol::SplitSession_V1

### Request

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKey |

### Response

| Type | Name |
|------|------|
| GameSessionKey | gameSessionKeyMigrated |

# (28) SearchSocialSessions

## GameSessionProtocol::SearchSocialSessions_V1

### Request

| Type | Name |
|------|------|
| GameSessionSocialQuery | gameSessionSocialQuery |

### Response

| Type | Name |
|------|------|
| qlist<GameSessionSearchWithParticipantsResult> | searchResults |

# (29) ReportUnsuccessfulJoinSessions

## GameSessionProtocol::ReportUnsuccessfulJoinSessions_V1

### Request

| Type | Name |
|------|------|
| qlist<GameSessionUnsuccessfulJoinSession> | unsuccessfulJoinSessions |

### Response

This method does not return anything.

# Types

## GameSessionKey ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_sessionID |

## GameSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| qlist<Property> | m_attributes |

## GameSessionSearchResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| profileid | m_hostPID |
| qlist<stationurl> | m_hostURLs |
| qlist<Property> | m_attributes |

## GameSessionUpdate ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| qlist<Property> | m_attributes |

## GameSessionParticipant ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| profileid | m_PID |
| qlist<stationurl> | m_stationURLs |

## GameSessionInvitation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| qlist<profileid> | m_recipientPIDs |
| string | m_message |

## GameSessionInvitationSent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| profileid | m_recipientPID |
| string | m_message |
| datetime | m_creationTime |

## GameSessionInvitationReceived ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| profileid | m_senderPID |
| string | m_message |
| datetime | m_creationTime |

## GameSessionQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_queryID |
| qlist<Property> | m_parameters |

## GameSessionSocialQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_typeID |
| uint32 | m_queryID |
| qlist<Property> | m_parameters |
| qlist<profileid> | m_participantIDs |

## GameSessionMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| string | m_message |

## GameSessionSearchWithParticipantsResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `GameSessionSearchResult`.

| Type | Name |
|------|------|
| qlist<profileid> | m_participantIDs |

## GameSessionUnsuccessfulJoinSession ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| GameSessionKey | m_sessionKey |
| uint32 | m_errorCategory |
| int32 | m_errorCode |
