# GlobalEventsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | FetchCurrent | [GlobalEventsProtocol::FetchCurrent_V1](#globaleventsprotocolfetchcurrent_v1) |

# (1) FetchCurrent

## GlobalEventsProtocol::FetchCurrent_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<[GlobalEvent](#globalevent-structure)> | events |

# Types

## GlobalEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |
| qlist<[Property](#property-structure)> | props |

## Property ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | key |
| variant | value |
