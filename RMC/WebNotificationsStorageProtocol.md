# WebNotificationsStorageProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | RegisterUser | [WebNotificationsStorageProtocol::RegisterUser_V1](#webnotificationsstorageprotocolregisteruser_v1) |
| 2 | PollNotifications | [WebNotificationsStorageProtocol::PollNotifications_V1](#webnotificationsstorageprotocolpollnotifications_v1) |
| 3 | UnregisterUser | [WebNotificationsStorageProtocol::UnregisterUser_V1](#webnotificationsstorageprotocolunregisteruser_v1) |

# (1) RegisterUser

## WebNotificationsStorageProtocol::RegisterUser_V1

### Request

This method does not take any parameters.

### Response

This method does not return anything.

# (2) PollNotifications

## WebNotificationsStorageProtocol::PollNotifications_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| string | listNotifications |
| int32 | nbNotifications |

# (3) UnregisterUser

## WebNotificationsStorageProtocol::UnregisterUser_V1

### Request

This method does not take any parameters.

### Response

This method does not return anything.
