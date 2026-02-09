# HermesAchievementsProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | ReadAchievementDetails | [HermesAchievementsProtocol::ReadAchievementDetails_V1](#hermesachievementsprotocolreadachievementdetails_v1) |
| 2 | ReadAchievementSet | [HermesAchievementsProtocol::ReadAchievementSet_V1](#hermesachievementsprotocolreadachievementset_v1) |
| 3 | UnlockAchievements | [HermesAchievementsProtocol::UnlockAchievements_V1](#hermesachievementsprotocolunlockachievements_v1) |

# (1) ReadAchievementDetails

## HermesAchievementsProtocol::ReadAchievementDetails_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |

### Response

| Type | Name |
|------|------|
| [HermesAchievement](#hermesachievement-structure) | achievement |

# (2) ReadAchievementSet

## HermesAchievementsProtocol::ReadAchievementSet_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<[HermesAchievement](#hermesachievement-structure)> | achievements |

# (3) UnlockAchievements

## HermesAchievementsProtocol::UnlockAchievements_V1

### Request

| Type | Name |
|------|------|
| qlist\<uint32> | achievementIds |

### Response

This method does not return anything.

# Types

## HermesAchievement ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkStr1 |
| string | unkStr2 |
| bool | unkBool1 |
| bool | unkBool2 |
| uint32 | unkUint2 |
| datetime | time |
