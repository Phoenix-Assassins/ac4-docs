# AccountManagerProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetContent | [AccountManagerProtocol::GetContent_V1](#accountmanagerprotocolgetcontent_v1) |
| 2 | SaveContent | [AccountManagerProtocol::SaveContent_V1](#accountmanagerprotocolsavecontent_v1) |
| 3 | RequestPid | [AccountManagerProtocol::RequestPid_V1](#accountmanagerprotocolrequestpid_v1) |
| 4 | ReleasePid | [AccountManagerProtocol::ReleasePid_V1](#accountmanagerprotocolreleasepid_v1) |

# (1) GetContent

## AccountManagerProtocol::GetContent_V1

### Request

| Type | Name |
|------|------|
| int16 | id |

### Response

| Type | Name |
|------|------|
| AccountManagerData | data |

# (2) SaveContent

## AccountManagerProtocol::SaveContent_V1

### Request

| Type | Name |
|------|------|
| AccountManagerData | data |

### Response

| Type | Name |
|------|------|
| int16 | id |

# (3) RequestPid

## AccountManagerProtocol::RequestPid_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | pid |

# (4) ReleasePid

## AccountManagerProtocol::ReleasePid_V1

### Request

| Type | Name |
|------|------|
| uint32 | pid |

### Response

This method does not return anything.

# Types

## AccountManagerData ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | name |
| string | description |
| uint32 | status |
| datetime | creation_date |
| datetime | modification_date |
