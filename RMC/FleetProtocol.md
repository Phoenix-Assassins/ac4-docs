# FleetProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | StartSession | [FleetProtocol::StartSession_V1](#fleetprotocolstartsession_v1) |
| 2 | UpdateSession | [FleetProtocol::UpdateSession_V1](#fleetprotocolupdatesession_v1) |
| 3 | CloseSession | [FleetProtocol::CloseSession_V1](#fleetprotocolclosesession_v1) |
| 4 | GetPlayer | [FleetProtocol::GetPlayer_V1](#fleetprotocolgetplayer_v1) |
| 5 | UpdatePlayer | [FleetProtocol::UpdatePlayer_V1](#fleetprotocolupdateplayer_v1) |
| 6 | DeletePlayer | [FleetProtocol::DeletePlayer_V1](#fleetprotocoldeleteplayer_v1) |
| 7 | GetBoats | [FleetProtocol::GetBoats_V1](#fleetprotocolgetboats_v1) |
| 8 | UpdateBoats | [FleetProtocol::UpdateBoats_V1](#fleetprotocolupdateboats_v1) |
| 9 | AddBoat | [FleetProtocol::AddBoat_V1](#fleetprotocoladdboat_v1) |
| 10 | DeleteBoat | [FleetProtocol::DeleteBoat_V1](#fleetprotocoldeleteboat_v1) |
| 11 | GetResources | [FleetProtocol::GetResources_V1](#fleetprotocolgetresources_v1) |
| 12 | UpdateResources | [FleetProtocol::UpdateResources_V1](#fleetprotocolupdateresources_v1) |
| 13 | GetMissions | [FleetProtocol::GetMissions_V1](#fleetprotocolgetmissions_v1) |
| 14 | GetMission | [FleetProtocol::GetMission_V1](#fleetprotocolgetmission_v1) |
| 15 | AddMissions | [FleetProtocol::AddMissions_V1](#fleetprotocoladdmissions_v1) |
| 16 | AddMission | [FleetProtocol::AddMission_V1](#fleetprotocoladdmission_v1) |
| 17 | UpdateMission | [FleetProtocol::UpdateMission_V1](#fleetprotocolupdatemission_v1) |
| 18 | UpdateMissions | [FleetProtocol::UpdateMissions_V1](#fleetprotocolupdatemissions_v1) |
| 19 | DeleteMission | [FleetProtocol::DeleteMission_V1](#fleetprotocoldeletemission_v1) |
| 20 | DeleteMissions | [FleetProtocol::DeleteMissions_V1](#fleetprotocoldeletemissions_v1) |
| 21 | GetRoutes | [FleetProtocol::GetRoutes_V1](#fleetprotocolgetroutes_v1) |
| 22 | UpdateRoutes | [FleetProtocol::UpdateRoutes_V1](#fleetprotocolupdateroutes_v1) |
| 23 | GetRewards | [FleetProtocol::GetRewards_V1](#fleetprotocolgetrewards_v1) |
| 24 | AddRewards | [FleetProtocol::AddRewards_V1](#fleetprotocoladdrewards_v1) |
| 25 | WithdrawReward | [FleetProtocol::WithdrawReward_V1](#fleetprotocolwithdrawreward_v1) |
| 26 | GetFriendMissions | [FleetProtocol::GetFriendMissions_V1](#fleetprotocolgetfriendmissions_v1) |
| 27 | HelpFriendMission | [FleetProtocol::HelpFriendMission_V1](#fleetprotocolhelpfriendmission_v1) |
| 28 | BatchUpdate | [FleetProtocol::BatchUpdate_V1](#fleetprotocolbatchupdate_v1) |
| 29 | UpdateUserUPlayId | [FleetProtocol::UpdateUserUPlayId_V1](#fleetprotocolupdateuseruplayid_v1) |

# (1) StartSession

## FleetProtocol::StartSession_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| string | sesName |

# (2) UpdateSession

## FleetProtocol::UpdateSession_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

This method does not return anything.

# (3) CloseSession

## FleetProtocol::CloseSession_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

This method does not return anything.

# (4) GetPlayer

## FleetProtocol::GetPlayer_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

| Type | Name |
|------|------|
| [Player](#player-structure) | player |

# (5) UpdatePlayer

## FleetProtocol::UpdatePlayer_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint16 | unkShort |
| qlist<[FleetBoat](#fleetboat-structure)> | boats |
| qlist<[FleetResource](#fleetresource-structure)> | resources |
| qlist<[FleetRoute](#fleetroute-structure)> | routes |

### Response

| Type | Name |
|------|------|
| qlist<uint32> | unkUints |

# (6) DeletePlayer

## FleetProtocol::DeletePlayer_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

This method does not return anything.

# (7) GetBoats

## FleetProtocol::GetBoats_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[FleetBoat](#fleetboat-structure)> | boats |

# (8) UpdateBoats

## FleetProtocol::UpdateBoats_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetBoat](#fleetboat-structure)> | boats |

### Response

This method does not return anything.

# (9) AddBoat

## FleetProtocol::AddBoat_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| [FleetBoat](#fleetboat-structure) | boat |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (10) DeleteBoat

## FleetProtocol::DeleteBoat_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| uint32 | unkUint |

### Response

This method does not return anything.

# (11) GetResources

## FleetProtocol::GetResources_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[FleetResource](#fleetresource-structure)> | resources |

# (12) UpdateResources

## FleetProtocol::UpdateResources_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetResource](#fleetresource-structure)> | resources |

### Response

This method does not return anything.

# (13) GetMissions

## FleetProtocol::GetMissions_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

| Type | Name |
|------|------|
| qlist<[FleetMission](#fleetmission-structure)> | missions |

# (14) GetMission

## FleetProtocol::GetMission_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| [FleetMission](#fleetmission-structure) | mission |

# (15) AddMissions

## FleetProtocol::AddMissions_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetMission](#fleetmission-structure)> | missions |

### Response

| Type | Name |
|------|------|
| qlist<uint32> | unkUints |

# (16) AddMission

## FleetProtocol::AddMission_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (17) UpdateMission

## FleetProtocol::UpdateMission_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (18) UpdateMissions

## FleetProtocol::UpdateMissions_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetMission](#fleetmission-structure)> | missions |

### Response

This method does not return anything.

# (19) DeleteMission

## FleetProtocol::DeleteMission_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (20) DeleteMissions

## FleetProtocol::DeleteMissions_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (21) GetRoutes

## FleetProtocol::GetRoutes_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[FleetRoute](#fleetroute-structure)> | routes |

# (22) UpdateRoutes

## FleetProtocol::UpdateRoutes_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetRoute](#fleetroute-structure)> | routes |

### Response

This method does not return anything.

# (23) GetRewards

## FleetProtocol::GetRewards_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

| Type | Name |
|------|------|
| qlist<[FleetReward](#fleetreward-structure)> | rewards |

# (24) AddRewards

## FleetProtocol::AddRewards_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetReward](#fleetreward-structure)> | rewards |

### Response

This method does not return anything.

# (25) WithdrawReward

## FleetProtocol::WithdrawReward_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| uint32 | unkUint1 |
| uint32 | unkUint2 |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (26) GetFriendMissions

## FleetProtocol::GetFriendMissions_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

| Type | Name |
|------|------|
| qlist<[FleetMission](#fleetmission-structure)> | missions |
| qlist<[FleetBoat](#fleetboat-structure)> | boats |

# (27) HelpFriendMission

## FleetProtocol::HelpFriendMission_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| uint32 | unkUint1 |
| uint16 | unkShort |
| uint32 | unkUint2 |

### Response

This method does not return anything.

# (28) BatchUpdate

## FleetProtocol::BatchUpdate_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |
| qlist<[FleetBoat](#fleetboat-structure)> | boats |
| qlist<uint32> | unkUints |
| qlist<[FleetResource](#fleetresource-structure)> | resources |
| qlist<[FleetReward](#fleetreward-structure)> | rewards |
| qlist<[FleetMission](#fleetmission-structure)> | missions1 |
| qlist<[FleetMission](#fleetmission-structure)> | missions2 |
| qlist<[FleetRoute](#fleetroute-structure)> | routes |

### Response

| Type | Name |
|------|------|
| qlist<uint32> | unkUints |

# (29) UpdateUserUPlayId

## FleetProtocol::UpdateUserUPlayId_V1

### Request

| Type | Name |
|------|------|
| string | unkStr |

### Response

This method does not return anything.

# Types

## Player ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | name |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint16 | unkShort |
| qlist<[FleetBoat](#fleetboat-structure)> | boats |
| qlist<[FleetResource](#fleetresource-structure)> | resources |
| qlist<[FleetMission](#fleetmission-structure)> | missions |
| qlist<[FleetRoute](#fleetroute-structure)> | routes |
| qlist<[FleetReward](#fleetreward-structure)> | rewards |

## FleetBoat ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| uint16 | unkShort |
| uint32 | unkUint5 |

## FleetResource ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint16 | unkShort |
| uint32 | unkUint |

## FleetMission ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr1 |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| qlist<uint32> | unkUints |
| uint32 | unkUint4 |
| uint32 | unkUint5 |
| uint32 | unkUint6 |
| uint16 | unkShort1 |
| string | unkStr2 |
| uint16 | unkShort2 |

## FleetRoute ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint16 | unkShort |

## FleetReward ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
