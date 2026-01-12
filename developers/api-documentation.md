---
description: API reference for Tally's platform
---

# API Documentation

Tally provides APIs for programmatic access to token sale data, governance information, and platform functionality.

## Overview

### Available APIs

| API | Protocol | Use Case |
|-----|----------|----------|
| REST API | HTTP/JSON | General data access |
| GraphQL | GraphQL | Flexible queries |
| Webhooks | HTTP callbacks | Real-time notifications |

### Base URLs

<<TODO: Add production and testnet API base URLs>>

| Environment | Base URL |
|-------------|----------|
| Production | `https://api.tally.xyz/...` |
| Testnet | `https://api.testnet.tally.xyz/...` |

## Authentication

### API Keys

Authenticate requests with API keys:

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
  https://api.tally.xyz/v1/...
```

### Obtaining Keys

<<TODO: Add process for obtaining API keys - self-service vs. contact sales>>

### Key Security

Best practices for API key management:

- Store in environment variables
- Never commit to version control
- Rotate keys periodically
- Use separate keys for development/production

## Rate Limits

### Default Limits

<<TODO: Add specific rate limit numbers>>

| Endpoint Type | Limit |
|---------------|-------|
| Read operations | X requests/minute |
| Write operations | Y requests/minute |
| Webhooks | Z per event |

### Rate Limit Headers

Responses include rate limit information:

```
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 99
X-RateLimit-Reset: 1640000000
```

### Handling Rate Limits

When rate limited:

1. Check `X-RateLimit-Reset` header
2. Implement exponential backoff
3. Cache responses where appropriate
4. Consider request batching

## REST API

### Token Sales

#### List Sales

Get information about token sales:

```http
GET /v1/sales
```

**Parameters:**
<<TODO: Add query parameters>>

**Response:**
<<TODO: Add response schema>>

#### Get Sale Details

Get details for a specific sale:

```http
GET /v1/sales/{saleId}
```

**Response:**
<<TODO: Add response schema>>

#### Get Sale Participants

List participants in a sale:

```http
GET /v1/sales/{saleId}/participants
```

**Parameters:**
<<TODO: Add pagination parameters>>

### Governance

#### List DAOs

Get list of DAOs on Tally:

```http
GET /v1/daos
```

#### Get DAO Details

Get details for a specific DAO:

```http
GET /v1/daos/{daoId}
```

#### List Proposals

Get proposals for a DAO:

```http
GET /v1/daos/{daoId}/proposals
```

#### Get Proposal Details

Get details for a specific proposal:

```http
GET /v1/proposals/{proposalId}
```

### Staking

#### Get Staking Positions

Get staking positions for an address:

```http
GET /v1/staking/positions/{address}
```

#### Get Staking Stats

Get aggregate staking statistics:

```http
GET /v1/staking/stats/{contractAddress}
```

## GraphQL API

### Endpoint

<<TODO: Add GraphQL endpoint URL>>

```
POST https://api.tally.xyz/graphql
```

### Schema

<<TODO: Add link to GraphQL schema or schema explorer>>

### Example Queries

#### Get Sale Information

```graphql
query GetSale($id: ID!) {
  sale(id: $id) {
    id
    name
    status
    startTime
    endTime
    totalRaised
    participants {
      count
    }
  }
}
```

#### Get DAO Proposals

```graphql
query GetProposals($daoId: ID!, $first: Int) {
  proposals(daoId: $daoId, first: $first) {
    edges {
      node {
        id
        title
        status
        forVotes
        againstVotes
      }
    }
  }
}
```

#### Get Voter Participation

```graphql
query GetVoterStats($address: String!) {
  voter(address: $address) {
    totalVotes
    proposalsVoted
    delegatedPower
    delegations {
      from
      amount
    }
  }
}
```

## Webhooks

### Available Events

<<TODO: Add list of webhook events>>

| Event | Description |
|-------|-------------|
| `sale.started` | Token sale has started |
| `sale.ended` | Token sale has ended |
| `sale.participation` | New participation recorded |
| `proposal.created` | New proposal created |
| `proposal.executed` | Proposal executed |

### Webhook Setup

Register webhook endpoints:

<<TODO: Add webhook registration process>>

### Payload Format

Webhook payloads follow this structure:

```json
{
  "event": "sale.participation",
  "timestamp": "2024-01-15T12:00:00Z",
  "data": {
    "saleId": "...",
    "participant": "0x...",
    "amount": "1000000000000000000"
  },
  "signature": "..."
}
```

### Verifying Webhooks

Verify webhook authenticity:

<<TODO: Add signature verification process and code examples>>

### Retry Policy

Failed webhook deliveries are retried:

- First retry: 1 minute
- Second retry: 5 minutes
- Third retry: 30 minutes
- Final retry: 2 hours

## Error Handling

### Error Format

Errors follow a consistent format:

```json
{
  "error": {
    "code": "INVALID_PARAMETER",
    "message": "The 'address' parameter is invalid",
    "details": {
      "parameter": "address",
      "value": "invalid"
    }
  }
}
```

### Common Error Codes

| Code | HTTP Status | Description |
|------|-------------|-------------|
| `UNAUTHORIZED` | 401 | Invalid or missing API key |
| `FORBIDDEN` | 403 | Insufficient permissions |
| `NOT_FOUND` | 404 | Resource not found |
| `RATE_LIMITED` | 429 | Rate limit exceeded |
| `INVALID_PARAMETER` | 400 | Invalid request parameter |
| `INTERNAL_ERROR` | 500 | Server error |

## Code Examples

### JavaScript/TypeScript

```typescript
import axios from 'axios';

const client = axios.create({
  baseURL: 'https://api.tally.xyz/v1',
  headers: {
    'Authorization': `Bearer ${process.env.TALLY_API_KEY}`
  }
});

// Get sale details
async function getSale(saleId: string) {
  const response = await client.get(`/sales/${saleId}`);
  return response.data;
}

// List proposals
async function getProposals(daoId: string) {
  const response = await client.get(`/daos/${daoId}/proposals`);
  return response.data;
}
```

### Python

```python
import requests
import os

class TallyClient:
    def __init__(self):
        self.base_url = "https://api.tally.xyz/v1"
        self.headers = {
            "Authorization": f"Bearer {os.environ['TALLY_API_KEY']}"
        }

    def get_sale(self, sale_id: str):
        response = requests.get(
            f"{self.base_url}/sales/{sale_id}",
            headers=self.headers
        )
        response.raise_for_status()
        return response.json()

    def get_proposals(self, dao_id: str):
        response = requests.get(
            f"{self.base_url}/daos/{dao_id}/proposals",
            headers=self.headers
        )
        response.raise_for_status()
        return response.json()
```

## SDK Documentation

<<TODO: Add links to SDK documentation for each supported language>>

## Changelog

<<TODO: Add API changelog or link to release notes>>

## Support

For API support:

- Documentation issues: Open a GitHub issue
- Technical questions: Developer Discord
- Enterprise support: Contact your account manager

## See Also

- [Smart Contracts](smart-contracts.md) - Contract documentation
- [Developers Overview](README.md) - Getting started
