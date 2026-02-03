# SimpleAuthenticationProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | Authenticate | [SimpleAuthenticationProtocol::Authenticate_V1](#simpleauthenticationprotocolauthenticate_v1) |
| 1 | Authenticate | [SimpleAuthenticationProtocol::Authenticate_V2](#simpleauthenticationprotocolauthenticate_v2) |
| 2 | LoginWithToken | [SimpleAuthenticationProtocol::LoginWithToken_V1](#simpleauthenticationprotocolloginwithtoken_v1) |
| 2 | LoginWithToken | [SimpleAuthenticationProtocol::LoginWithToken_V2](#simpleauthenticationprotocolloginwithtoken_v2) |
| 3 | Login | [SimpleAuthenticationProtocol::Login_V1](#simpleauthenticationprotocollogin_v1) |
| 3 | Login | [SimpleAuthenticationProtocol::Login_V2](#simpleauthenticationprotocollogin_v2) |
| 4 | Register | [SimpleAuthenticationProtocol::Register_V1](#simpleauthenticationprotocolregister_v1) |

# (1) Authenticate

## SimpleAuthenticationProtocol::Authenticate_V1

### Request

| Type | Name |
|------|------|
| string | strUserName |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |

## SimpleAuthenticationProtocol::Authenticate_V2

### Request

| Type | Name |
|------|------|
| string | strUserName |
| ClientVersionInfo | versionInfo |
| RVConnectionData | pConnectionData |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |

# (2) LoginWithToken

## SimpleAuthenticationProtocol::LoginWithToken_V1

### Request

| Type | Name |
|------|------|
| string | strToken |
| string | strOnlineKey |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |

## SimpleAuthenticationProtocol::LoginWithToken_V2

### Request

| Type | Name |
|------|------|
| string | strToken |
| string | strOnlineKey |
| ClientVersionInfo | versionInfo |
| RVConnectionData | pConnectionData |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |

# (3) Login

## SimpleAuthenticationProtocol::Login_V1

### Request

| Type | Name |
|------|------|
| string | strUsername |
| string | strPassword |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |

## SimpleAuthenticationProtocol::Login_V2

### Request

| Type | Name |
|------|------|
| string | strUsername |
| string | strPassword |
| ClientVersionInfo | versionInfo |
| RVConnectionData | pConnectionData |

### Response

| Type | Name |
|------|------|
| profileid | pidProfile |
| RVConnectionData | pConnectionData |
| string | strReturnMsg |

# (4) Register

## SimpleAuthenticationProtocol::Register_V1

### Request

| Type | Name |
|------|------|
| std_list<stationurl> | vecMyURLs |

### Response

| Type | Name |
|------|------|
| uint32 | pidConnectionID |
| stationurl | urlPublic |

# Types

## RVConnectionData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| stationurl | m_urlRegularProtocols |
| std_list<byte> | m_lstSpecialProtocols |
| stationurl | m_urlSpecialProtocols |
| uint32 | nid |

## ClientVersionInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint16 | m_v1 |
| uint16 | m_v2 |
| uint16 | m_v3 |
| uint32 | m_v4 |
| variant | m_customVersion |
