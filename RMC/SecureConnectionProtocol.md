# SecureConnectionProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | Register | [SecureConnectionProtocol::Register_V1](#secureconnectionprotocolregister_v1) |
| 2 | RequestConnectionData | [SecureConnectionProtocol::RequestConnectionData_V1](#secureconnectionprotocolrequestconnectiondata_v1) |
| 3 | RequestURLs | [SecureConnectionProtocol::RequestURLs_V1](#secureconnectionprotocolrequesturls_v1) |

# (1) Register

## SecureConnectionProtocol::Register_V1

### Request

| Type | Name |
|------|------|
| std_list<stationurl> | vecMyURLs |

### Response

| Type | Name |
|------|------|
| uint32 | pidConnectionID |
| stationurl | urlPublic |

# (2) RequestConnectionData

## SecureConnectionProtocol::RequestConnectionData_V1

### Request

| Type | Name |
|------|------|
| uint32 | cidTarget |
| uint32 | pidTarget |

### Response

| Type | Name |
|------|------|
| std_list<ConnectionData> | pvecConnectionsData |

# (3) RequestURLs

## SecureConnectionProtocol::RequestURLs_V1

### Request

| Type | Name |
|------|------|
| uint32 | cidTarget |
| uint32 | pidTarget |

### Response

| Type | Name |
|------|------|
| std_list<stationurl> | plstURLs |

# Types

## ConnectionData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| stationurl | m_StationUrl |
| uint32 | m_ConnectionID |
