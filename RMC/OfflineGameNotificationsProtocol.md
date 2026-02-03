# OfflineGameNotificationsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | PollNotifications | [OfflineGameNotificationsProtocol::PollNotifications_V1](#offlinegamenotificationsprotocolpollnotifications_v1) |
| 2 | PollSpecificOfflineNotifications | [OfflineGameNotificationsProtocol::PollSpecificOfflineNotifications_V1](#offlinegamenotificationsprotocolpollspecificofflinenotifications_v1) |
| 3 | PollAnyOfflineNotifications | [OfflineGameNotificationsProtocol::PollAnyOfflineNotifications_V1](#offlinegamenotificationsprotocolpollanyofflinenotifications_v1) |

# (1) PollNotifications

## OfflineGameNotificationsProtocol::PollNotifications_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<NotificationEvent> | listNotifications |
| uint32 | nbRemainingNotifs |

# (2) PollSpecificOfflineNotifications

## OfflineGameNotificationsProtocol::PollSpecificOfflineNotifications_V1

### Request

| Type | Name |
|------|------|
| qlist<uint32> | majortype |

### Response

| Type | Name |
|------|------|
| qlist<TimedNotification> | listTimedNotification |
| uint32 | ret |

# (3) PollAnyOfflineNotifications

## OfflineGameNotificationsProtocol::PollAnyOfflineNotifications_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<TimedNotification> | listTimedNotification |
| uint32 | nbRemainingNotifs |

# Types

## NotificationEvent ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| profileid | m_pidSource |
| string | m_strRawParams |

## TimedNotification ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

| Type | Name |
|------|------|
| datetime | timestamp |
| NotificationEvent | notification |
