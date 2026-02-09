# LiveEventsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetEvents | [LiveEventsProtocol::GetEvents_V1](#liveeventsprotocolgetevents_v1) |
| 2 | SendEvent | [LiveEventsProtocol::SendEvent_V1](#liveeventsprotocolsendevent_v1) |
| 3 | SendEventMulticast | [LiveEventsProtocol::SendEventMulticast_V1](#liveeventsprotocolsendeventmulticast_v1) |
| 4 | SendEventWeb | [LiveEventsProtocol::SendEventWeb_V1](#liveeventsprotocolsendeventweb_v1) |

# (1) GetEvents

## LiveEventsProtocol::GetEvents_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

### Response

| Type | Name |
|------|------|
| qlist<[LiveEvent](#liveevent-structure)> | events |
| uint32 | unkUint |

# (2) SendEvent

## LiveEventsProtocol::SendEvent_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (3) SendEventMulticast

## LiveEventsProtocol::SendEventMulticast_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (4) SendEventWeb

## LiveEventsProtocol::SendEventWeb_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# Types

## LiveEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| bool | unkBool |
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint2 |
| uint64 | unkLong1 |
| uint64 | unkLong2 |
| uint8 | unkByte |
| qBuffer | buffer |

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
