# PrivilegesProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetPrivileges | [PrivilegesProtocol::GetPrivileges_V1](#privilegesprotocolgetprivileges_v1) |
| 2 | ActivateKey | [PrivilegesProtocol::ActivateKey_V1](#privilegesprotocolactivatekey_v1) |
| 3 | ActivateKeyWithExpectedPrivileges | [PrivilegesProtocol::ActivateKeyWithExpectedPrivileges_V1](#privilegesprotocolactivatekeywithexpectedprivileges_v1) |
| 4 | GetPrivilegeRemainDuration | [PrivilegesProtocol::GetPrivilegeRemainDuration_V1](#privilegesprotocolgetprivilegeremainduration_v1) |
| 5 | GetExpiredPrivileges | [PrivilegesProtocol::GetExpiredPrivileges_V1](#privilegesprotocolgetexpiredprivileges_v1) |
| 6 | GetPrivilegesEx | [PrivilegesProtocol::GetPrivilegesEx_V1](#privilegesprotocolgetprivilegesex_v1) |

# (1) GetPrivileges

## PrivilegesProtocol::GetPrivileges_V1

### Request

| Type | Name |
|------|------|
| string | localeCode |

### Response

| Type | Name |
|------|------|
| std_map<uint32,Privilege> | privileges |

# (2) ActivateKey

## PrivilegesProtocol::ActivateKey_V1

### Request

| Type | Name |
|------|------|
| string | uniqueKey |
| string | languageCode |

### Response

| Type | Name |
|------|------|
| PrivilegeGroup | privilege |

# (3) ActivateKeyWithExpectedPrivileges

## PrivilegesProtocol::ActivateKeyWithExpectedPrivileges_V1

### Request

| Type | Name |
|------|------|
| string | uniqueKey |
| string | languageCode |
| qlist<uint32> | expectedPrivilegeIDs |

### Response

| Type | Name |
|------|------|
| PrivilegeGroup | privilege |

# (4) GetPrivilegeRemainDuration

## PrivilegesProtocol::GetPrivilegeRemainDuration_V1

### Request

| Type | Name |
|------|------|
| uint32 | privilegeID |

### Response

| Type | Name |
|------|------|
| int32 | seconds |

# (5) GetExpiredPrivileges

## PrivilegesProtocol::GetExpiredPrivileges_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<PrivilegeEx> | expiredPrivileges |

# (6) GetPrivilegesEx

## PrivilegesProtocol::GetPrivilegesEx_V1

### Request

| Type | Name |
|------|------|
| string | localeCode |

### Response

| Type | Name |
|------|------|
| qlist<PrivilegeEx> | privilegesEx |

# Types

## Privilege ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| string | m_description |

## PrivilegeEx ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| string | m_description |
| int32 | m_duration |

## PrivilegeGroup ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_description |
| qlist<Privilege> | m_privileges |
