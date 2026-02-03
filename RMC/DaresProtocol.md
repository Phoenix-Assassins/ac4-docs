# DaresProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | requestDares | [DaresProtocol::requestDares_V1](#daresprotocolrequestdares_v1) |
| 2 | deleteDare | [DaresProtocol::deleteDare_V1](#daresprotocoldeletedare_v1) |
| 3 | postDare | [DaresProtocol::postDare_V1](#daresprotocolpostdare_v1) |
| 4 | changeStatus | [DaresProtocol::changeStatus_V1](#daresprotocolchangestatus_v1) |
| 5 | requestUnreadCount | [DaresProtocol::requestUnreadCount_V1](#daresprotocolrequestunreadcount_v1) |

# (1) requestDares

## DaresProtocol::requestDares_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| datetime | lastReadDate |
| qlist<DareInfo> | allDares |

# (2) deleteDare

## DaresProtocol::deleteDare_V1

### Request

| Type | Name |
|------|------|
| uint32 | dareId |

### Response

This method does not return anything.

# (3) postDare

## DaresProtocol::postDare_V1

### Request

| Type | Name |
|------|------|
| profileid | targetPID |
| uint32 | dareId |
| uint32 | score |

### Response

This method does not return anything.

# (4) changeStatus

## DaresProtocol::changeStatus_V1

### Request

| Type | Name |
|------|------|
| qlist<uint32> | dareIDs |
| uint32 | status |

### Response

This method does not return anything.

# (5) requestUnreadCount

## DaresProtocol::requestUnreadCount_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | count |

# Types

## DareInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| profileid | m_senderPID |
| profileid | m_targetPID |
| datetime | m_publishDate |
| uint32 | m_score |
| uint32 | m_dareID |
| uint32 | m_status |
