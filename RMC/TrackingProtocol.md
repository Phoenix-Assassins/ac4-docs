# TrackingProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | SendUserInfo | [TrackingProtocol::SendUserInfo_V1](#trackingprotocolsenduserinfo_v1) |
| 2 | GetConfiguration | [TrackingProtocol::GetConfiguration_V1](#trackingprotocolgetconfiguration_v1) |
| 3 | SendTags | [TrackingProtocol::SendTags_V1](#trackingprotocolsendtags_v1) |

# (1) SendUserInfo

## TrackingProtocol::SendUserInfo_V1

### Request

| Type | Name |
|------|------|
| TrackingInformation | user_info |
| uint32 | delta_time |

### Response

| Type | Name |
|------|------|
| TrackingInformation | user_info |
| uint32 | session_id |

# (2) GetConfiguration

## TrackingProtocol::GetConfiguration_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| std_list<string> | configured_tags |

# (3) SendTags

## TrackingProtocol::SendTags_V1

### Request

| Type | Name |
|------|------|
| std_list<TrackingTag> | tags |

### Response

This method does not return anything.

# Types

## TrackingInformation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | ipn |
| string | user_id |
| string | machine_id |
| string | visitor_id |

## TrackingTag ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | session_id |
| string | tag |
| string | attributes |
| uint32 | delta_time |
| string | new_user_id |
