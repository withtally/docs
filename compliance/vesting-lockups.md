---
description: Token lockup periods and vesting schedules for compliance
---

# Vesting & Lockups

Token lockups and vesting schedules control when participants can access their purchased tokens. These mechanisms serve both regulatory compliance and tokenomics goals, ensuring aligned incentives and meeting jurisdictional requirements.

## Why Lockups Matter

### Regulatory Compliance

Many jurisdictions require or recommend lockups:

- Securities regulations may mandate holding periods
- Lockups can help distinguish utility from security
- Different regions may require different periods
- Demonstrates long-term alignment

### Tokenomics Benefits

Beyond compliance, lockups serve project goals:

- Prevent immediate sell pressure
- Encourage long-term holding
- Align participant incentives
- Support price stability at launch

## Types of Lockups

### Linear Vesting

Tokens unlock gradually over time:

```
       100% |................._____
            |            ___/
Unlocked    |        ___/
            |    ___/
            |___/
         0% +----------------------
            Start            End
                   Time
```

**Example:** 12-month linear vesting releases ~8.33% per month

### Cliff Vesting

Initial lockup followed by partial or full unlock:

```
       100% |................_____
            |               |
Unlocked    |               |
            |               |
            |_______________|
         0% +----------------------
            Start  Cliff    End
                   Time
```

**Example:** 6-month cliff, then linear vesting for remaining 6 months

### Milestone Vesting

Tokens unlock based on specific events:

- Product launches
- Revenue targets
- Governance votes
- Time-based checkpoints

### Region-Specific Lockups

Different vesting for different jurisdictions:

| Region | Lockup Period | Vesting Type |
|--------|---------------|--------------|
| US Accredited | 12 months | Cliff |
| EU | 6 months | Linear |
| Asia-Pacific | 3 months | Linear |
| Other | None | Immediate |

## Configuration Options

### Timing Parameters

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Cliff Period | Initial lockup before any unlock | 0-12 months |
| Vesting Duration | Total time until fully vested | 6-48 months |
| Unlock Frequency | How often tokens vest | Daily/Weekly/Monthly |

### Unlock Amounts

| Parameter | Description | Options |
|-----------|-------------|---------|
| Initial Unlock | Tokens available at purchase | 0-25% typical |
| Cliff Unlock | Released at cliff end | 10-50% typical |
| Linear Release | Ongoing vesting rate | Remaining balance |

### Triggers

| Trigger | Description | Use Case |
|---------|-------------|----------|
| Time-based | Calendar date/duration | Standard vesting |
| Block-based | Blockchain blocks | Chain-native timing |
| Event-based | Specific conditions | Milestone vesting |

## Technical Implementation

### On-Chain Enforcement

Lockups are enforced via smart contracts:

- Tokens held in vesting contracts
- Participants claim as tokens vest
- Non-custodial design
- Audited, battle-tested contracts

### Vesting Contract Mechanics

1. **Deposit:** Tokens locked at sale close
2. **Tracking:** Contract tracks vested amounts
3. **Claiming:** Participants claim vested tokens
4. **Verification:** Contract verifies eligibility

### Integration with Sale

Vesting integrates with your sale:

- Configured during sale setup
- Applied automatically at distribution
- Region-specific rules applied per KYC
- Unified participant experience

## Claim Interface

### Participant Experience

Tally provides a claim interface:

1. **Connect wallet:** Participant connects verified wallet
2. **View schedule:** See full vesting timeline
3. **Check vested:** View currently claimable amount
4. **Claim tokens:** Execute on-chain claim transaction
5. **Track history:** View past claims

### Dashboard Information

Participants see:

- Total tokens purchased
- Vested (claimable) amount
- Claimed amount
- Remaining locked amount
- Next unlock date
- Full vesting schedule

## Region-Specific Configuration

### US Requirements

<<TODO: Add specific US lockup requirements, including Regulation D/S considerations, accredited investor holding periods>>

### EU Requirements

<<TODO: Add EU-specific lockup considerations under MiCA>>

### Other Jurisdictions

<<TODO: Add guidance for other major jurisdictions>>

## Common Configurations

### Conservative (High Compliance)

For sales requiring maximum compliance:

```
Initial unlock: 0%
Cliff: 12 months
Vesting: 24 months linear after cliff
Total lockup: 36 months
```

### Balanced

For standard compliance with some liquidity:

```
Initial unlock: 10%
Cliff: 6 months
Vesting: 12 months linear after cliff
Total lockup: 18 months
```

### Minimal

For sales with fewer restrictions:

```
Initial unlock: 25%
Cliff: None
Vesting: 3 months linear
Total lockup: 3 months
```

## Best Practices

### Clear Communication

Before the sale:

- Publish vesting schedules clearly
- Explain regional differences
- Provide claim instructions
- Set expectations on timing

### Fair Design

Balance stakeholder interests:

- Sufficient lockup for compliance
- Reasonable access for participants
- Consistent with tokenomics
- Aligned with team vesting

### Technical Testing

Before launch:

- Test vesting contracts on testnet
- Verify claim flow works correctly
- Test regional differentiation
- Audit smart contracts

## Modifying Lockups

### Can Lockups Be Changed?

Generally, on-chain lockups are immutable:

- Provides participant certainty
- Enforces committed schedules
- Cannot be shortened unilaterally

### Emergency Provisions

In rare cases:

- Governance-approved changes (if applicable)
- Migration to new contracts (complex)
- Generally avoid if possible

## Integration with Governance

### Locked Token Voting

Locked tokens may retain governance rights:

- Configure voting with locked tokens
- Delegation while locked
- Integration with Tally governance

See [Governance Overview](../post-launch-tooling/governance-overview.md)

### Staking Integration

Locked tokens may be stakeable:

- Earn rewards while locked
- Compounding vesting
- Integration with Tally staking

See [Staking & Incentives](../post-launch-tooling/staking-incentives.md)

## Troubleshooting

### Common Issues

**Participants can't claim:**
- Verify wallet connection
- Check vested amount is non-zero
- Confirm gas available for transaction

**Wrong vesting schedule:**
- Check KYC-determined region
- Verify configuration applied correctly
- Review purchase records

**Contract issues:**
- Contact Tally support
- Review transaction errors
- Check contract status

## Next Steps

- [KYC Verification](kyc-verification.md) - Identity verification
- [Geo-Restrictions](geo-restrictions.md) - Geographic controls
- [After Your Sale](../token-sales/after-your-sale.md) - Post-sale operations
