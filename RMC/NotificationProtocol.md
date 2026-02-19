# NotificationProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | ProcessNotificationEvent | [NotificationProtocol::ProcessNotificationEvent_V1](#notificationprotocolprocessnotificationevent_v1) |

# (1) ProcessNotificationEvent

## NotificationProtocol::ProcessNotificationEvent_V1

### Request

| Type | Name |
|------|------|
| [NotificationEvent](#notificationevent-structure) | oNotificationEvent |

### Response

This method does not return anything.

# Types

## NotificationEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| profileid | m_pidSource |
| string | m_strRawParams |
