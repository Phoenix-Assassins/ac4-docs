# WalletProtocol

| ID | Method | Variant |
|----|--------|---------|
| 1 | RetrievePrimaryStoreURL | [WalletProtocol::RetrievePrimaryStoreURL_V1](#walletprotocolretrieveprimarystoreurl_v1) |
| 2 | PlayerWalletCurrencyBalanceChanged | [WalletProtocol::PlayerWalletCurrencyBalanceChanged_V1](#walletprotocolplayerwalletcurrencybalancechanged_v1) |
| 3 | SetPlayerUPlayToken | [WalletProtocol::SetPlayerUPlayToken_V1](#walletprotocolsetplayeruplaytoken_v1) |
| 4 | GetSteamIdByUplayId | [WalletProtocol::GetSteamIdByUplayId_V1](#walletprotocolgetsteamidbyuplayid_v1) |
| 5 | GetSKUByUplayId | [WalletProtocol::GetSKUByUplayId_V1](#walletprotocolgetskubyuplayid_v1) |
| 6 | GetPIDByUplayId | [WalletProtocol::GetPIDByUplayId_V1](#walletprotocolgetpidbyuplayid_v1) |

# (1) RetrievePrimaryStoreURL

## WalletProtocol::RetrievePrimaryStoreURL_V1

### Request

| Type | Name |
|------|------|
| string | unkStr1 |
| uint64 | unkLong |
| string | unkStr2 |
| string | unkStr3 |
| string | unkStr4 |

### Response

| Type | Name |
|------|------|
| string | storeURL |

# (2) PlayerWalletCurrencyBalanceChanged

## WalletProtocol::PlayerWalletCurrencyBalanceChanged_V1

### Request

Unused method, payload unknown.

### Response

This method does not return anything.

# (3) SetPlayerUPlayToken

## WalletProtocol::SetPlayerUPlayToken_V1

### Request

| Type | Name |
|------|------|
| string | token |

### Response

This method does not return anything.

# (4) GetSteamIdByUplayId

## WalletProtocol::GetSteamIdByUplayId_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| string | steamId |

# (5) GetSKUByUplayId

## WalletProtocol::GetSKUByUplayId_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| string | sku |

# (6) GetPIDByUplayId

## WalletProtocol::GetPIDByUplayId_V1

### Request

Unused method, payload unknown.

### Response

| Type | Name |
|------|------|
| uint32 | pid |
