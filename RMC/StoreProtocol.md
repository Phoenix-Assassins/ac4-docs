# StoreProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | GetProducts | [StoreProtocol::GetProducts_V1](#storeprotocolgetproducts_v1) |

# (1) GetProducts

## StoreProtocol::GetProducts_V1

### Request

This method does not take any parameters.

### Response

| Type | Name |
|------|------|
| qvector<Product> | products |

# Types

## Offer ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

| Type | Name |
|------|------|
| string | offerTextID |
| datetime | releaseDate |

## Product ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Data`.

| Type | Name |
|------|------|
| uint32 | productID |
| uint32 | productType |
| uint32 | bannerObjectID |
| string | name |
| string | description |
| qvector<Offer> | offers |
