# ClansProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | CreateClan | [ClansProtocol::CreateClan_V1](#clansprotocolcreateclan_v1) |
| 2 | WEB_CreateClan | [ClansProtocol::WEB_CreateClan_V1](#clansprotocolweb_createclan_v1) |
| 3 | UpdateClanStatus | [ClansProtocol::UpdateClanStatus_V1](#clansprotocolupdateclanstatus_v1) |
| 4 | GetClansInfos | [ClansProtocol::GetClansInfos_V1](#clansprotocolgetclaninfos_v1) |
| 5 | GetClansNames | [ClansProtocol::GetClansNames_V1](#clansprotocolgetclansnames_v1) |
| 6 | GetPlayersClanInfos | [ClansProtocol::GetPlayersClanInfos_V1](#clansprotocolgetplayersclaninfos_v1) |
| 7 | GetMembersLists | [ClansProtocol::GetMembersLists_V1](#clansprotocolgetmemberslists_v1) |
| 8 | InviteToClan | [ClansProtocol::InviteToClan_V1](#clansprotocolinvitetoclan_v1) |
| 9 | AcceptClanInvite | [ClansProtocol::AcceptClanInvite_V1](#clansprotocolacceptclaninvite_v1) |
| 10 | RefuseClanInvite | [ClansProtocol::RefuseClanInvite_V1](#clansprotocolrefuseclaninvite_v1) |
| 11 | LeaveClan | [ClansProtocol::LeaveClan_V1](#clansprotocolleaveclan_v1) |
| 12 | ChangeRole | [ClansProtocol::ChangeRole_V1](#clansprotocolchangerole_v1) |
| 13 | Kick | [ClansProtocol::Kick_V1](#clansprotocolkick_v1) |

# (1) CreateClan

## ClansProtocol::CreateClan_V1

### Request

| Type | Name |
|------|------|
| string | unkStr1 |
| string | unkStr2 |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

# (2) WEB_CreateClan

## ClansProtocol::WEB_CreateClan_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

# (3) UpdateClanStatus

## ClansProtocol::UpdateClanStatus_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (4) GetClansInfos

## ClansProtocol::GetClansInfos_V1

### Request

| Type | Name |
|------|------|
| qlist<uint32> | clanIds |

### Response

| Type | Name |
|------|------|
| qlist\<[ClanInfo](#claninfo-structure)> | infos |

# (5) GetClansNames

## ClansProtocol::GetClansNames_V1

### Request

| Type | Name |
|------|------|
| qlist<string> | names |

### Response

| Type | Name |
|------|------|
| qlist<string> | clanNames |

# (6) GetPlayersClanInfos

## ClansProtocol::GetPlayersClanInfos_V1

### Request

| Type | Name |
|------|------|
| qlist<[UnkType](#unktype-structure)> | list |

### Response

| Type | Name |
|------|------|
| qlist\<uin32> | unkUints1 |
| qlist\<uin32> | unkUints2 |

# (7) GetMembersLists

## ClansProtocol::GetMembersLists_V1

### Request

| Type | Name |
|------|------|
| qlist\<uin32> | clanIds |

### Response

| Type | Name |
|------|------|
| qlist<qlist<[ClanMember](#clanmember-structure)>> | membersLists |

# (8) InviteToClan

## ClansProtocol::InviteToClan_V1

### Request

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (9) AcceptClanInvite

## ClansProtocol::AcceptClanInvite_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (10) RefuseClanInvite

## ClansProtocol::RefuseClanInvite_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (11) LeaveClan

## ClansProtocol::LeaveClan_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (12) ChangeRole

## ClansProtocol::ChangeRole_V1

### Request

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint1 |
| uint32 | unkUint2 |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (13) Kick

## ClansProtocol::Kick_V1

### Request

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# Types

## ClanInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkStr1 |
| string | unkStr2 |
| [UnkType](#UnkType-structure)> | list |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |

## UnkType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| uint16 | unkShort1 |
| uint16 | unkShort2 |
| uint16 | unkShort3 |
| uint16 | unkShort4 |
| uint16 | unkShort5 |
| uint16 | unkShort6 |

## ClanMember ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint32 | unkUint5 |
| uint32 | unkUint6 |
| uint32 | unkUint7 |
| uint32 | unkUint8 |
| uint32 | unkUint9 |
| uint32 | unkUint10 |
