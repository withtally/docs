---
description: Market-driven price discovery through on-chain auctions
---

# Continuous Clearing Auctions (CCAs)

Continuous Clearing Auctions enable market-driven price discovery through a fully on-chain auction mechanism. Bidders place orders that are split across auction blocks, with each block clearing at the identified market price. Transparent mechanics give buyers and investors confidence in the sale.

## How CCAs Work

### The Basic Mechanism

1. **Bidding Period:** Participants submit bids specifying quantity and maximum price
2. **Order Batching:** Bids are collected into auction blocks
3. **Price Discovery:** Each block's clearing price is calculated based on supply and demand
4. **Uniform Clearing:** All winning bids in a block pay the same clearing price
5. **Continuous Operation:** Multiple blocks can run sequentially for extended sales

### Clearing Price Calculation

The clearing price for each block is determined by finding the price where:

```
Supply (tokens available) = Demand (sum of bids at or above clearing price)
```

All participants who bid at or above the clearing price receive tokens at that price, regardless of their maximum bid.

### Example Clearing

```
Block Supply: 1,000 tokens

Bids:
- Alice: 500 tokens @ max $2.00
- Bob: 300 tokens @ max $1.80
- Carol: 400 tokens @ max $1.50
- Dave: 200 tokens @ max $1.20

Clearing: At $1.50, demand = 1,200 (Alice + Bob + Carol)
          Tokens allocated pro-rata to bids >= $1.50

Result: All pay $1.50 per token
```

## Configuration Parameters

### Auction Structure

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Block Size | Tokens per auction block | Varies by sale size |
| Block Duration | Time per auction block | 1-24 hours |
| Number of Blocks | Total blocks in sale | 1-10+ |
| Reserve Price | Minimum clearing price | Project discretion |

### Bidding Parameters

| Parameter | Description | Guidance |
|-----------|-------------|----------|
| Minimum Bid | Smallest allowed bid | Low barrier preferred |
| Maximum Bid | Largest allowed bid | Anti-whale measure |
| Bid Currencies | Accepted payment tokens | USDC, USDT, ETH |

## Advantages of CCAs

### Full Transparency

Every aspect is visible on-chain:

- All bids are recorded
- Clearing calculations are verifiable
- No hidden mechanics or special treatment
- Auditable by anyone

### MEV Resistance

Batch clearing prevents common attack vectors:

- No front-running individual transactions
- Order of submission doesn't determine allocation
- All participants pay the same clearing price
- Reduces bot advantage over regular users

### True Price Discovery

Market participants collectively determine fair value:

- No predetermined price to manipulate
- Aggregated demand signals true willingness to pay
- Institutional-grade auction mechanics
- Results reflect actual market conditions

### Investor Confidence

Professional investors appreciate CCA mechanics:

- Familiar auction format from traditional finance
- Clear rules and predictable execution
- Equal treatment for all participants
- Transparent allocation methodology

## Considerations

### Participant Education

CCAs require more explanation than simple purchases:

- Bid vs. purchase distinction
- Clearing price concept
- Pro-rata allocation
- Timing within blocks

Plan to educate your community before the sale.

### Allocation Uncertainty

Participants don't know their exact allocation until clearing:

- Bids may be partially filled
- Final price unknown until block closes
- Requires comfort with uncertainty

### Technical Complexity

Implementation is more complex than fixed-price sales:

- Tally handles all technical aspects
- More parameters to configure correctly
- Requires careful testing

## Technical Implementation

### Smart Contracts

Tally deploys battle-tested CCA contracts:

- Bid submission and management
- Clearing price calculation
- Token allocation and distribution
- Integration with compliance layer

### Powered by Uniswap

CCAs leverage Uniswap's auction infrastructure:

- Audited, production-ready contracts
- Proven at scale
- Continuous improvement and maintenance

### Frontend Experience

Tally provides an intuitive interface:

- Clear bid submission flow
- Real-time block status
- Allocation tracking
- Claim interface post-clearing

### Monitoring

Access comprehensive dashboards:

- Current bids and demand curves
- Estimated clearing prices
- Block progress
- Participation metrics

## Best Practices

### Setting Reserve Prices

Consider floor pricing carefully:

- Too high may result in unfilled blocks
- Too low provides little protection
- Base on fundamental analysis

### Block Timing

Structure blocks for optimal participation:

- Allow sufficient time for bids
- Consider global time zones
- Account for blockchain confirmation times

### Communication

Keep participants informed:

- Explain mechanics clearly before sale
- Provide real-time updates during blocks
- Communicate results promptly

## Demo

{% embed url="https://youtu.be/ycZv_XrzcKo" %}

## Learn More

- [Uniswap CCA Documentation](https://cca.uniswap.org/)
- [Choosing Your Sale Type](../token-sales/choosing-your-sale-type.md)
- [Running Your Sale](../token-sales/running-your-sale.md)
