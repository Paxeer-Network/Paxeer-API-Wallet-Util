Base URL: https://wallet-api.paxeer.app

### Consolidated Wallet Profile
``` GET /api/address/:address/profile ```

Response:
```json
{
    "address": "0x29e1f94f6b209b57ecdc1fe87448a6d085a78a5a",
    "native_balance": 100,
    "token_balances": [
        {
            "balance": 100,
            "token_id": null,
            "details": {
                "name": "Token Name",
                "symbol": "TKN",
                "decimals": 18,
                "type": "ERC-20",
                "contract": "0x1234567890123456789012345678901234567890",
                "fiat_value": 100,
                "icon_url": "https://example.com/icon.png"
            }
        }
    ],
    "transactions": [
        {
            "hash": "0x1234567890123456789012345678901234567890123456789012345678901234",
            "from_address_hash": "0x1234567890123456789012345678901234567890",
            "to_address_hash": "0x1234567890123456789012345678901234567890",
            "value": 100,
            "gas_used": 21000,
            "block_number": 6861
        }
    ],
    "token_transfers": [
        {
            "transaction_hash": "0x1234567890123456789012345678901234567890123456789012345678901234",
            "from_address_hash": "0x1234567890123456789012345678901234567890",
            "to_address_hash": "0x1234567890123456789012345678901234567890",
            "amount": 100,
            "token_ids": null,
            "block_number": 6861,
            "token": {
                "name": "Token Name",
                "symbol": "TKN",
                "type": "ERC-20",
                "contract": "0x1234567890123456789012345678901234567890"
            }
        }
    ]
}
```

### Blockchain Stats
``` GET /api/stats ```

Response:
```json
{
    "latestBlock": 6861,
    "totalTransactions": 100
}
```
### Balance of an address
``` GET /api/address/:address/balance ```

Response:
```json
{
    "address": "0x29e1f94f6b209b57ecdc1fe87448a6d085a78a5a",
    "balance": 100
}
```
### Transactions of an address
``` GET /api/address/:address/transactions ```

Response:
```json
{
    "address": "0x29e1f94f6b209b57ecdc1fe87448a6d085a78a5a",
    "transactions": [
        {
            "hash": "0x1234567890123456789012345678901234567890123456789012345678901234",
            "from_address_hash": "0x1234567890123456789012345678901234567890",
            "to_address_hash": "0x1234567890123456789012345678901234567890",
            "value": 100,
            "gas_used": 21000,
            "block_number": 6861
        }
    ]
}
```
### Token Transfers of an address
``` GET /api/address/:address/tokentransfers ```

Response:
```json
{
    "address": "0x29e1f94f6b209b57ecdc1fe87448a6d085a78a5a",
    "transfers": [
        {
            "transaction_hash": "0x1234567890123456789012345678901234567890123456789012345678901234",
            "from_address_hash": "0x1234567890123456789012345678901234567890",
            "to_address_hash": "0x1234567890123456789012345678901234567890",
            "amount": 100,
            "token_ids": null,
            "block_number": 6861,
            "token": {
                "name": "Token Name",
                "symbol": "TKN",
                "type": "ERC-20",
                "contract": "0x1234567890123456789012345678901234567890"
            }
        }
    ]
}
```
### Token Balances of an address
``` GET /api/address/:address/tokens ```

Response:
```json
{
    "address": "0x29e1f94f6b209b57ecdc1fe87448a6d085a78a5a",
    "tokens": [
        {
            "balance": 100,
            "token_id": null,
            "details": {
                "name": "Token Name",
                "symbol": "TKN",
                "decimals": 18,
                "type": "ERC-20",
                "contract": "0x1234567890123456789012345678901234567890",
                "fiat_value": 100,
                "icon_url": "https://example.com/icon.png"
            }
        }
    ]
}
```
