---
description: Price discovery through declining price curves
---

# Liquidity Bootstrapping Pools (LBPs)

Liquidity Bootstrapping Pools enable price discovery through a declining price curve. The price starts high and decreases over time, discouraging early speculation and allowing broader participation at fair prices.

Tally builds custom interfaces that abstract away the complexity of interacting with Balancer directly, providing a seamless experience for your participants.

## How LBPs Work

### The Basic Mechanism

1. **Initial Setup:** Tokens are deposited into a weighted pool with a starting weight ratio (e.g., 96% project token / 4% USDC)
2. **Weight Shift:** Over the sale duration, weights gradually shift (e.g., ending at 50/50)
3. **Price Decline:** As weights shift, the price naturally decreases
4. **Participant Entry:** Buyers enter when the price reaches their target
5. **Equilibrium:** Buy pressure slows the decline, finding market equilibrium

### Price Dynamics

The LBP price follows a predictable curve:

```
Starting Price: High (set above expected fair value)
        |
        |  \
        |   \
Price   |    \  <- Price decline from weight change
        |     \
        |      \_____ <- Buy pressure slows decline
        |            \____
        |                 \
        +-------------------------> Time
                   Sale Duration
```

When no one buys, price declines according to the weight curve. When participants buy, they push the price up, creating a dynamic equilibrium.

## Configuration Parameters

### Weight Configuration

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Starting Weight | Initial token weight in pool | 90-98% |
| Ending Weight | Final token weight in pool | 30-50% |
| Curve Shape | Linear or custom decay | Linear default |

### Timing Parameters

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Sale Duration | Total length of the LBP | 24-72 hours |
| Start Time | When the sale begins | Scheduled |
| End Time | When the sale concludes | Scheduled |

### Price Parameters

| Parameter | Description | Guidance |
|-----------|-------------|----------|
| Starting Price | Initial token price | 2-5x expected fair value |
| Reserve Price | Optional price floor | Project discretion |

## Advantages of LBPs

### Anti-Whale Mechanics

The declining price structure discourages large early purchases:

- Buying early means paying a premium
- Waiting risks missing out if others buy
- Natural game theory promotes patience
- Results in broader distribution

### Fair Price Discovery

Market dynamics determine the fair price:

- No predetermined price to get wrong
- Participants vote with capital
- Transparent mechanism for all
- Price reflects genuine demand

### Simple Participant Experience

Despite complex mechanics, the UX is straightforward:

- Connect wallet
- See current price
- Decide to buy or wait
- Execute purchase

### Proven Track Record

LBPs have been used successfully by major projects:

<<TODO: Add specific examples of successful LBP launches with metrics>>

## Considerations

### Starting Price Setting

Setting the starting price too high or too low creates issues:

- **Too high:** Few early participants, may not sell out
- **Too low:** Immediate buying pressure, less price discovery

Work with Tally to model appropriate starting prices based on your targets.

### Duration Selection

Sale duration affects outcomes:

- **Too short:** Less time for price discovery, favors fast actors
- **Too long:** Participant fatigue, prolonged uncertainty

24-72 hours is typical for most LBPs.

### Market Conditions

External market volatility can affect your sale:

- Crypto market movements impact participant sentiment
- Payment currency fluctuations affect real values
- Consider timing relative to broader market conditions

## Technical Implementation

### Smart Contracts

Tally deploys audited contracts on Balancer:

- Pool creation and configuration
- Weight shift programming
- Integration with compliance layer

### Frontend Experience

Tally provides a white-labeled interface:

- Real-time price display
- Purchase flow with wallet integration
- KYC verification (if required)
- Transaction status and confirmation

### Monitoring

During the sale, access real-time dashboards:

- Current price and weight status
- Participation metrics
- Funds raised
- Time remaining

## Best Practices

### Communication

Educate your community before the sale:

- Explain how LBPs work
- Set expectations about price dynamics
- Encourage patience over FOMO

### Timing

Consider launch timing carefully:

- Avoid major competing events
- Account for global time zones
- Ensure team availability during sale

### Post-Sale

Plan for what happens when the LBP concludes:

- Token distribution mechanism
- Remaining liquidity handling
- Community communication

## Demo

{% embed url="https://youtu.be/UGoy6At6H6M" %}

## Learn More

- [Balancer LBP Documentation](https://docs.balancer.fi/concepts/explore-available-balancer-pools/liquidity-bootstrapping-pool.html)
- [Choosing Your Sale Type](../token-sales/choosing-your-sale-type.md)
- [Running Your Sale](../token-sales/running-your-sale.md)
