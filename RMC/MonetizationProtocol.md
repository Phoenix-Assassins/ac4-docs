# MonetizationProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetPendingTransaction | [MonetizationProtocol::GetPendingTransaction_V1](#monetizationprotocol) |
| 2 | CreateTransaction | [MonetizationProtocol::CreateTransaction_V1](#monetizationprotocol) |
| 3 | CompleteTransaction | [MonetizationProtocol::CompleteTransaction_V1](#monetizationprotocol) |
| 4 | GetPendingTransaction2 | [MonetizationProtocol::GetPendingTransaction2_V1](#monetizationprotocol) |
| 5 | GetPendingTransaction3 | [MonetizationProtocol::GetPendingTransaction3_V1](#monetizationprotocol) |

# (1) GetPendingTransaction

## MonetizationProtocol::GetPendingTransaction_V1

### Request


### Response
| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<[Transaction](#Transaction-structure)> | transactions |

# (2) CreateTransaction

## MonetizationProtocol::CreateTransaction_V1

### Request


### Response
| Type | Name |
|------|------|
| uint32 | transactionID |

# (3) CompleteTransaction

## MonetizationProtocol::CompleteTransaction_V1

### Request


### Response
This method does not return anything.

# (4) GetPendingTransaction2

## MonetizationProtocol::GetPendingTransaction2_V1

### Request


### Response
| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<[Transaction2](#Transaction2-structure)> | transactions |

# (5) GetPendingTransaction3

## MonetizationProtocol::GetPendingTransaction3_V1

### Request
This method does not take any parameters.

### Response
| Type | Name |
|------|------|
| uint32 | unkUint |
| qlist\<[Transaction3](#Transaction3-structure)> | transactions |

# Types

## Transaction ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr1 |
| string | unkStr2 |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr3 |
| uint32 | unkUint3 |
| string | unkStr4 |

## Transaction2 ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr1 |
| string | unkStr2 |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr3 |
| uint32 | unkUint3 |
| string | unkStr4 |
| bool | unkBool |

## Transaction3 ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr1 |
| string | unkStr2 |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| uint32 | unkUint4 |
| string | unkStr3 |
| uint32 | unkUint5 |
| string | unkStr4 |
| bool | unkBool |
