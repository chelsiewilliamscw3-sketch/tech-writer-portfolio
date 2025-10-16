# API Guide: Transactions v1

## Overview
This guide describes endpoints for reading transaction data used in finance reporting workflows.

## Base URL
`https://api.example.com/v1`

## Authentication
Bearer Token (see internal Confluence page `Auth-Tokens`)

## Endpoints
### GET /transactions
Retrieve a list of transactions filtered by date range and account.

**Query Params**
- `start` (YYYY-MM-DD)
- `end` (YYYY-MM-DD)
- `account` (string)

**Response**
```json
{
  "count": 120,
  "items": [ { "id": "tx_001", "date": "2025-09-01", "amount": 130.55, "account": "OPEX-401" } ]
}
```

### GET /transactions/{id}
Retrieve a single transaction by id.

**Response**
```json
{ "id": "tx_001", "date": "2025-09-01", "amount": 130.55, "account": "OPEX-401", "note": "Office supplies" }
```

## Errors
- 401 Unauthorized – invalid token
- 404 Not Found – transaction does not exist

## Changelog
- v1.0 – initial draft
