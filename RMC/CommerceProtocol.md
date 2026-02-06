# CommerceProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetProducts | [CommerceProtocol::GetProducts_V1](#commerceprotocolgetproducts_v1) |

# (1) GetProducts

## CommerceProtocol::GetProducts_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qlist<[Product](#product-structure)> | products |

# Types

## Product ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| string | unkStr1 |
| string | unkStr2 |
| qlist\<[UnkType](#UnkType-structure)> | list |
| string | unkStr3 |

## UnkType ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | unkStr |
| datetime | time |
