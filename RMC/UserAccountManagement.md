# UserAccountManagement

| ID | Method | Variant |
|----|--------|---------|
| 1 | HaveUsersPlayed | [UserAccountManagement::HaveUsersPlayed_V1](#useraccountmanagementhaveusersplayed_v1) |
| 2 | AreUsersPlaying | [UserAccountManagement::AreUsersPlaying_V1](#useraccountmanagementareusersplaying_v1) |

# (1) HaveUsersPlayed

## UserAccountManagement::HaveUsersPlayed_V1

### Request

| Type | Name |
|------|------|
| std_list<quuid> | profileIds |

### Response

| Type | Name |
|------|------|
| std_map<quuid,bool> | UserPresence |

# (2) AreUsersPlaying

## UserAccountManagement::AreUsersPlaying_V1

### Request

| Type | Name |
|------|------|
| std_list<quuid> | profileIds |

### Response

| Type | Name |
|------|------|
| std_map<quuid,bool> | UserPresence |
