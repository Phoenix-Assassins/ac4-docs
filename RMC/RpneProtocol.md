# RpneProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | SendEvent | [RpneProtocol::SendEvent_V1](#rpneprotocolsendevent_v1) |
| 2 | GetSubscriptions | [RpneProtocol::GetSubscriptions_V1](#rpneprotocolgetsubscriptions_v1) |
| 3 | SetSubscriptions | [RpneProtocol::SetSubscriptions_V1](#rpneprotocolsetsubscriptions_v1) |
| 4 | RequestInteractiveEvents | [RpneProtocol::RequestInteractiveEvents_V1](#rpneprotocolrequestinteractiveevents_v1) |
| 5 | UpdateInteractiveEvents | [RpneProtocol::UpdateInteractiveEvents_V1](#rpneprotocolupdateinteractiveevents_v1) |

# (1) SendEvent

## RpneProtocol::SendEvent_V1

### Request

| Type | Name |
|------|------|
| string | id |
| std_map<string,variant> | values |

### Response

This method does not return anything.

# (2) GetSubscriptions

## RpneProtocol::GetSubscriptions_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| std_map<string,std_map<string,SubscriptionState>> | subscriptions |

# (3) SetSubscriptions

## RpneProtocol::SetSubscriptions_V1

### Request

| Type | Name |
|------|------|
| std_map<string,std_map<string,SubscriptionState>> | subscriptions |

### Response

This method does not return anything.

# (4) RequestInteractiveEvents

## RpneProtocol::RequestInteractiveEvents_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| std_list<EventContent> | events |

# (5) UpdateInteractiveEvents

## RpneProtocol::UpdateInteractiveEvents_V1

### Request

| Type | Name |
|------|------|
| std_list<EventContent> | events |

### Response

This method does not return anything.

# Types

## EventContent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_eventId |
| string | m_socialNetworkId |
| string | m_message |
| int32 | m_id |
| datetime | m_creationDate |
| datetime | m_expiryDate |
| int32 | m_playerAction |

## SubscriptionState ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_value |
| bool | m_isConfigurableByUser |
