---
description: Deep dive into each sale mechanism Tally supports
---

# Sale Types Overview

Tally supports multiple token sale mechanisms, each designed to meet different project needs. This section provides detailed documentation on each sale type, helping you understand the mechanics, advantages, and implementation details.

## Available Sale Types

### Liquidity Bootstrapping Pools (LBPs)

LBPs enable price discovery through a declining price curve. The price starts high and decreases over time, discouraging early speculation and allowing broader participation at fair prices.

**Key characteristics:**
- Automated price decline over time
- Anti-whale mechanics built-in
- Proven mechanism used by major projects
- Simple participant experience

[Learn more about LBPs](liquidity-bootstrapping-pools.md)

### Continuous Clearing Auctions (CCAs)

CCAs enable market-driven price discovery through a fully on-chain auction. Bidders place orders that are split across auction blocks, with each block clearing at the identified market price.

**Key characteristics:**
- Fully transparent on-chain mechanics
- MEV-resistant batch clearing
- Institutional-grade auction design
- True market-driven pricing

[Learn more about CCAs](continuous-clearing-auctions.md)

### Fixed-Price Sales

Set a predetermined price with optional allocation limits per wallet. Eligibility scoring and structured allocation reward long-term contributors.

**Key characteristics:**
- Predictable pricing and outcomes
- Fine-grained allocation control
- Community reward mechanisms
- Simple to understand and participate

[Learn more about Fixed-Price Sales](fixed-price-sales.md)

## Choosing the Right Mechanism

| Factor | LBP | CCA | Fixed Price |
|--------|-----|-----|-------------|
| **Price Discovery** | Market-driven via curve | Market-driven via auction | Project-determined |
| **Distribution Control** | Lower | Medium | Higher |
| **Complexity** | Medium | Medium | Low |
| **Best For** | Broad distribution | Institutional sales | Community allocations |
| **MEV Risk** | Medium | Low | Medium |

## Common Configuration Options

All sale types support:

- **KYC Integration:** Identity verification for participants
- **Geographic Restrictions:** Block or allow specific regions
- **Allocation Limits:** Maximum purchase per wallet
- **Vesting Schedules:** Post-sale lockup periods
- **Multiple Payment Currencies:** USDC, USDT, ETH

## Technical Implementation

Tally handles all smart contract deployment and infrastructure:

- Audited, battle-tested contracts
- White-labeled frontend experience
- Real-time monitoring dashboards
- Launch-day support

## Next Steps

- [Liquidity Bootstrapping Pools](liquidity-bootstrapping-pools.md) - Detailed LBP documentation
- [Continuous Clearing Auctions](continuous-clearing-auctions.md) - Detailed CCA documentation
- [Fixed-Price Sales](fixed-price-sales.md) - Detailed fixed-price documentation
- [Choosing Your Sale Type](../token-sales/choosing-your-sale-type.md) - Decision framework
