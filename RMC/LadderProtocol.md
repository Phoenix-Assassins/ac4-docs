# LadderProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | RegisterNewGame | [LadderProtocol::RegisterNewGame_V1](#ladderprotocolregisternewgame_v1) |
| 2 | ParticipateToGame | [LadderProtocol::ParticipateToGame_V1](#ladderprotocolparticipatetogame_v1) |
| 3 | EndGame | [LadderProtocol::EndGame_V1](#ladderprotocolendgame_v1) |
| 4 | RunSimulation | [LadderProtocol::RunSimulation_V1](#ladderprotocolrunsimulation_v1) |
| 5 | GetRewardBitfield | [LadderProtocol::GetRewardBitfield_V1](#ladderprotocolgetrewardbitfield_v1) |

# (1) RegisterNewGame

## LadderProtocol::RegisterNewGame_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| [LadderGameObj](#laddergameobj-structure) | unkObj |
| qBuffer | buffer |

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# (2) ParticipateToGame

## LadderProtocol::ParticipateToGame_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| [UnkType](#unktype-structure) | unkObj |
| qBuffer | buffer |

### Response

This method does not return anything.

# (3) EndGame

## LadderProtocol::EndGame_V1

### Request

| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist<[UnkType2](#unktype2-structure)> | objs |

### Response

| Type | Name |
|------|------|
| qlist<[UnkType2](#unktype2-structure)> | objs |

# (4) RunSimulation

## LadderProtocol::RunSimulation_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| qlist<[UnkType2](#unktype2-structure)> | objs |

# (5) GetRewardBitfield

## LadderProtocol::GetRewardBitfield_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| uint32 | unkUint |

# Types

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

## UnkType2 ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| [UnkType](#unktype-structure) | unkObj |
| uint32 | unkUint |
| qBuffer | buffer |
