---
description: Compare sale mechanisms to find the right fit for your project
---

# Choosing Your Sale Type

Tally supports multiple sale mechanisms, each with distinct advantages. This guide helps you understand the options and select the best fit for your distribution strategy and compliance requirements.

## Sale Type Overview

| Feature | LBP | CCA | Fixed Price |
|---------|-----|-----|-------------|
| Price Discovery | Declining curve | Market-driven auction | Predetermined |
| Best For | Broad distribution | Transparent price finding | Controlled allocation |
| Complexity | Medium | Medium | Low |
| Participant Experience | Simple bidding | Batch auctions | Direct purchase |

## Liquidity Bootstrapping Pools (LBPs)

LBPs enable price discovery through a declining price curve. The price starts high and decreases over time, discouraging early speculation and allowing broader participation at fair prices.

### How LBPs Work

1. **Starting price:** Set above expected market value
2. **Price decline:** Automatically decreases based on configured curve
3. **Participant timing:** Buyers choose when to enter based on their price targets
4. **Natural equilibrium:** Price stabilizes when buy pressure matches the decline rate

### Advantages

- **Anti-whale:** Declining price discourages large early purchases
- **Fair distribution:** Participants self-select based on price tolerance
- **Simple UX:** Straightforward buy experience for participants
- **Proven mechanism:** Widely used and understood in crypto

### Considerations

- Requires careful initial price and curve configuration
- Final price depends on market dynamics
- May leave tokens unsold if starting price is too high

### Best For

- Projects prioritizing broad distribution
- Teams comfortable with market-driven outcomes
- Sales targeting crypto-native participants

Learn more: [Liquidity Bootstrapping Pools](../sale-types/liquidity-bootstrapping-pools.md)

## Continuous Clearing Auctions (CCAs)

CCAs enable market-driven price discovery through a fully on-chain auction. Bidders place orders that are split across auction blocks, with each block clearing at the identified market price.

### How CCAs Work

1. **Bidding period:** Participants submit sealed bids
2. **Block clearing:** Orders are batched and cleared at uniform prices
3. **Price discovery:** Market dynamics determine clearing prices
4. **Continuous operation:** Multiple blocks can run sequentially

### Advantages

- **Transparent:** Fully on-chain mechanics visible to all
- **MEV-resistant:** Batch clearing prevents front-running
- **True price discovery:** Market determines fair value
- **Investor confidence:** Institutional-grade auction mechanics

### Considerations

- More complex UX than simple purchases
- Requires participant education
- Final allocation may differ from bid amount

### Best For

- Projects seeking institutional credibility
- Sales where price discovery is paramount
- Teams prioritizing transparency

Learn more: [Continuous Clearing Auctions](../sale-types/continuous-clearing-auctions.md)

## Fixed-Price Sales

Set a predetermined price with optional allocation limits per wallet. Eligibility scoring and structured allocation reward long-term contributors.

### How Fixed-Price Sales Work

1. **Price setting:** Project determines token price in advance
2. **Allocation rules:** Define per-wallet limits and eligibility criteria
3. **Purchase window:** Participants buy during the sale period
4. **Distribution:** Tokens allocated based on purchase order or pro-rata

### Advantages

- **Predictable outcomes:** Known price and raise amount
- **Simple to understand:** No complex mechanics to explain
- **Controlled distribution:** Precise allocation management
- **Eligibility flexibility:** Reward loyal community members

### Considerations

- No market-driven price discovery
- May over or under-price tokens
- Potential for bot attacks without proper safeguards

### Best For

- Projects with strong existing community
- Sales with specific allocation goals
- Teams preferring predictable outcomes

Learn more: [Fixed-Price Sales](../sale-types/fixed-price-sales.md)

## Decision Framework

### Choose LBP if:

- You want the market to discover the fair price
- Broad distribution is a priority
- Your community is crypto-native

### Choose CCA if:

- Transparency and auditability are essential
- You're targeting institutional participants
- MEV resistance is important

### Choose Fixed Price if:

- You have a clear valuation in mind
- Community allocation is a priority
- Simplicity is valued over price optimization

## Combining with Compliance

All sale types can be configured with:

- KYC/KYB verification requirements
- Geographic restrictions
- Lockups and vesting schedules
- Allocation limits

See [Compliance Overview](../compliance/README.md) for details.

## Next Steps

- [Liquidity Bootstrapping Pools](../sale-types/liquidity-bootstrapping-pools.md) - Deep dive on LBPs
- [Continuous Clearing Auctions](../sale-types/continuous-clearing-auctions.md) - Deep dive on CCAs
- [Fixed-Price Sales](../sale-types/fixed-price-sales.md) - Deep dive on fixed-price mechanics
- [Running Your Sale](running-your-sale.md) - Execution guide
