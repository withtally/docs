---
description: Controlled allocation at predetermined prices
---

# Fixed-Price Sales

Fixed-price sales offer a straightforward approach: set a predetermined price with optional allocation limits per wallet. Eligibility scoring and structured allocation reward long-term contributors, giving you control over who can participate and how much they can purchase.

## How Fixed-Price Sales Work

### The Basic Mechanism

1. **Price Setting:** Project determines token price in advance
2. **Eligibility Definition:** Configure who can participate and their allocations
3. **Sale Window:** Open purchases during defined period
4. **Direct Purchase:** Participants buy tokens at the fixed price
5. **Distribution:** Tokens allocated based on purchase order or pro-rata

### Allocation Methods

**First-Come-First-Served:**
- Participants purchase in order of transaction
- Earlier transactions get priority
- Sale ends when supply exhausted

**Pro-Rata Allocation:**
- All purchases collected during window
- Tokens distributed proportionally if oversubscribed
- Excess funds returned to participants

**Tiered Allocation:**
- Different limits for different participant tiers
- Based on eligibility score or allowlist status
- Rewards loyal community members

## Configuration Parameters

### Pricing

| Parameter | Description | Guidance |
|-----------|-------------|----------|
| Token Price | Fixed price per token | Based on valuation |
| Payment Currencies | Accepted tokens | USDC, USDT, ETH |
| Price Lock | Freeze price for duration | Typically locked |

### Allocation Controls

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Per-Wallet Maximum | Maximum tokens per address | Varies by goals |
| Per-Wallet Minimum | Minimum purchase size | Low barrier preferred |
| Total Supply | Tokens available for sale | Project discretion |

### Eligibility

| Parameter | Description | Options |
|-----------|-------------|---------|
| Allowlist | Specific addresses permitted | CSV upload |
| Eligibility Score | Point-based qualification | Custom criteria |
| KYC Requirement | Identity verification | On/Off |

## Advantages of Fixed-Price Sales

### Predictable Outcomes

Know your results before you start:

- Exact price per token
- Maximum possible raise
- Clear allocation structure
- No price uncertainty

### Simple Participation

Easiest mechanism for participants:

- Clear price, no complexity
- Know exactly what you're getting
- Familiar purchase flow
- No auction mechanics to learn

### Controlled Distribution

Fine-grained allocation management:

- Reward loyal community members
- Prevent whale concentration
- Implement tiered access
- Enforce strict limits

### Community Building

Design sales around your community:

- Recognize early contributors
- Gate access to committed participants
- Build goodwill through fair allocation
- Strengthen stakeholder alignment

## Considerations

### No Price Discovery

The project determines price, not the market:

- Risk of over or under-pricing
- No market signal on fair value
- Requires independent valuation

### Bot Risk

Fixed prices can attract automated buyers:

- Implement anti-bot measures
- Consider allowlists
- Use KYC as a filter
- Rate limit transactions

### Oversubscription Management

Popular sales may have excess demand:

- Plan allocation methodology in advance
- Communicate clearly to participants
- Ensure fair distribution process

## Eligibility Scoring

### How Scoring Works

Eligibility scores allow nuanced participant selection:

1. **Define Criteria:** Choose factors that matter (token holding, protocol usage, etc.)
2. **Assign Points:** Weight each criterion appropriately
3. **Calculate Scores:** Aggregate points for each address
4. **Set Thresholds:** Minimum score to participate, tiered allocations

### Example Criteria

| Criterion | Description | Example Points |
|-----------|-------------|----------------|
| Token Holding | Amount of project token held | 1 point per token |
| Holding Duration | Time tokens held | 10 points per month |
| Protocol Usage | Interactions with protocol | 5 points per transaction |
| Community Participation | Governance votes, forum posts | 20 points per action |
| NFT Ownership | Specific NFT collections | 50 points per NFT |

### Tier Structure Example

| Tier | Score Required | Allocation |
|------|----------------|------------|
| Diamond | 1000+ | $10,000 |
| Gold | 500-999 | $5,000 |
| Silver | 100-499 | $1,000 |
| Bronze | 1-99 | $250 |

## Technical Implementation

### Smart Contracts

Tally deploys straightforward sale contracts:

- Purchase and allocation logic
- Eligibility verification
- Refund handling (if pro-rata)
- Integration with compliance layer

### Frontend Experience

Clean, intuitive interface:

- Eligibility checking
- Purchase flow
- Allocation display
- Transaction confirmation

### Monitoring

Track sale progress:

- Purchases over time
- Participation by tier
- Remaining allocation
- Geographic distribution

## Best Practices

### Pricing Strategy

<<TODO: Add guidance on fixed-price valuation methodologies and considerations>>

### Allocation Design

Balance multiple goals:

- Broad distribution vs. meaningful allocations
- Rewarding loyalty vs. welcoming newcomers
- Simplicity vs. nuanced tiers

### Communication

Set clear expectations:

- Announce eligibility criteria in advance
- Explain allocation methodology
- Provide timeline and key dates
- Be transparent about limits

### Anti-Bot Measures

Protect your sale:

- Implement KYC requirements
- Use eligibility scoring
- Set reasonable rate limits
- Consider captcha or proof of humanity

## Demo

{% embed url="https://youtu.be/ApvGHcz4wbI" %}

## Learn More

- [Choosing Your Sale Type](../token-sales/choosing-your-sale-type.md)
- [Running Your Sale](../token-sales/running-your-sale.md)
- [KYC Verification](../compliance/kyc-verification.md)
