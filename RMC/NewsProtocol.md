# NewsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetChannels | [NewsProtocol::GetChannels_V1](#newsprotocolgetchannels_v1) |
| 2 | GetChannelsByTypes | [NewsProtocol::GetChannelsByTypes_V1](#newsprotocolgetchannelsbytypes_v1) |
| 3 | GetSubscribableChannels | [NewsProtocol::GetSubscribableChannels_V1](#newsprotocolgetsubscribablechannels_v1) |
| 4 | GetSubscribedChannels | [NewsProtocol::GetSubscribedChannels_V1](#newsprotocolgetsubscribedchannels_v1) |
| 5 | SubscribeChannel | [NewsProtocol::SubscribeChannel_V1](#newsprotocolsubscribechannel_v1) |
| 6 | UnsubscribeChannel | [NewsProtocol::UnsubscribeChannel_V1](#newsprotocolunsubscribechannel_v1) |
| 7 | GetNextNewsByProfileID | [NewsProtocol::GetNextNewsByProfileID_V1](#newsprotocolgetnextnewsbyprofileid_v1) |
| 8 | GetNextNewsByChannelType | [NewsProtocol::GetNextNewsByChannelType_V1](#newsprotocolgetnextnewsbychanneltype_v1) |
| 9 | GetNewsByProfileIDs | [NewsProtocol::GetNewsByProfileIDs_V1](#newsprotocolgetnewsbyprofileids_v1) |
| 10 | GetNewsByChannelType | [NewsProtocol::GetNewsByChannelType_V1](#newsprotocolgetnewsbychanneltype_v1) |
| 11 | GetNewsBySubscriptions | [NewsProtocol::GetNewsBySubscriptions_V1](#newsprotocolgetnewsbysubscriptions_v1) |

# (1) GetChannels

## NewsProtocol::GetChannels_V1

### Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (2) GetChannelsByTypes

## NewsProtocol::GetChannelsByTypes_V1

### Request

| Type | Name |
|------|------|
| qlist<string> | newsChannelTypes |
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (3) GetSubscribableChannels

## NewsProtocol::GetSubscribableChannels_V1

### Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (4) GetSubscribedChannels

## NewsProtocol::GetSubscribedChannels_V1

### Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

### Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (5) SubscribeChannel

## NewsProtocol::SubscribeChannel_V1

### Request

| Type | Name |
|------|------|
| uint32 | newsChannelID |

### Response

This method does not return anything.

# (6) UnsubscribeChannel

## NewsProtocol::UnsubscribeChannel_V1

### Request

| Type | Name |
|------|------|
| uint32 | newsChannelID |

### Response

This method does not return anything.

# (7) GetNextNewsByProfileID

## NewsProtocol::GetNextNewsByProfileID_V1

### Request

| Type | Name |
|------|------|
| profileid | profileID |
| uint32 | count |
| uint32 | latestSeenMessageID |

### Response

| Type | Name |
|------|------|
| NewsMessageResult | newsMessageResult |

# (8) GetNextNewsByChannelType

## NewsProtocol::GetNextNewsByChannelType_V1

### Request

| Type | Name |
|------|------|
| string | newsChannelType |
| uint32 | count |
| uint32 | latestSeenMessageID |

### Response

| Type | Name |
|------|------|
| NewsMessageResult | newsMessageResult |

# (9) GetNewsByProfileIDs

## NewsProtocol::GetNewsByProfileIDs_V1

### Request

| Type | Name |
|------|------|
| qlist<profileid> | profileIDs |
| ResultRange | range |

### Response

| Type | Name |
|------|------|
| NewsMessageResult | newsMessageResult |

# (10) GetNewsByChannelType

## NewsProtocol::GetNewsByChannelType_V1

### Request

| Type | Name |
|------|------|
| string | newsChannelType |
| ResultRange | range |

### Response

| Type | Name |
|------|------|
| NewsMessageResult | newsMessageResult |

# (11) GetNewsBySubscriptions

## NewsProtocol::GetNewsBySubscriptions_V1

### Request

| Type | Name |
|------|------|
| ResultRange | range |

### Response

| Type | Name |
|------|------|
| NewsMessageResult | newsMessageResult |

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| profileid | m_ownerPID |
| string | m_name |
| string | m_description |
| datetime | m_creationTime |
| datetime | m_expirationTime |
| string | m_type |
| string | m_locale |
| bool | m_subscribable |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_channel |
| profileid | m_recipient |
| profileid | m_publisher |
| string | m_publisherName |
| datetime | m_publicationTime |
| datetime | m_displayTime |
| datetime | m_expirationTime |
| string | m_title |
| string | m_link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `NewsHeader`.

| Type | Name |
|------|------|
| string | m_body |

## NewsRecipient ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_channel |
| profileid | m_recipient |

## NewsFeedLink ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_newsChannelID |
| string | m_URL |
| string | m_description |
| datetime | m_feedUpdatedParseTime |
| datetime | m_lastUpdatedTime |
| datetime | m_nextRefreshTime |
| uint32 | m_refreshElapsedTimeMilliseconds |
| uint32 | m_refreshPeriodSeconds |
| bool | m_refreshEnabled |
| uint32 | m_refreshMethod |
| datetime | m_newestMessageTime |
| uint32 | m_messageAdded |

## NewsMessageResult ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qlist<NewsMessage> | m_messages |
| uint32 | m_messageCount |
