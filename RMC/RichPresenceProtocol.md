# RichPresenceProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | SetPresence | [RichPresenceProtocol::SetPresence_V1](#richpresenceprotocolsetpresence_v1) |
| 2 | GetPresence | [RichPresenceProtocol::GetPresence_V1](#richpresenceprotocolgetpresence_v1) |

# (1) SetPresence

## RichPresenceProtocol::SetPresence_V1

### Request

| Type | Name |
|------|------|
| uint32 | pid |
| qBuffer | props |

### Response

This method does not return anything.

# (2) GetPresence

## RichPresenceProtocol::GetPresence_V1

### Request

| Type | Name |
|------|------|
| qlist<[UnkType](#unktype-structure)> | unkObjs |

### Response

| Type | Name |
|------|------|
| qlist<[PresenceElement](#presenceelement-structure)> | presenceElements |

# Types

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

## PresenceElement ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| bool | overrideStatus |
| uint32 | unkUint |
| qBuffer | props |
