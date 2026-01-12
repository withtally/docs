---
description: Decentralized decision-making for your protocol
---

# Governance Overview

Deploy production-ready governance that scales with your protocol without requiring vendor migrations or custom integration work. As your governance matures, add advanced features like MultiGov, optimistic governance, or security council elections to meet the evolving needs of your community.

## What is On-Chain Governance?

On-chain governance enables decentralized decision-making through transparent voting:

- **Proposals:** Community members suggest changes
- **Voting:** Token holders express preferences
- **Execution:** Approved proposals execute automatically
- **Treasury:** Funds distributed through governance

### Why Governance Matters

After a token sale, governance:

- Gives stakeholders a voice in protocol direction
- Enables decentralized treasury management
- Builds community trust and engagement
- Supports regulatory positioning as utility

## Key Features

### Voting and Proposal Management

Secure, transparent voting mechanisms:

- **Proposal creation:** Structured proposal process
- **Collaborative drafting:** Multi-author proposals
- **No-code fund transfers:** Treasury distributions without coding
- **Automatic execution:** Approved proposals execute on-chain

### Delegation

Enable representative democracy:

- **Full delegation:** Transfer all voting power to a delegate
- **Partial delegation:** Split power across multiple delegates
- **Liquid delegation:** Change delegates at any time
- **Delegation without transfer:** Keep tokens, delegate votes

### Gasless Participation

Remove barriers to voting:

- **Free voting:** Organization pays gas costs
- **Free delegation:** No cost to delegate
- **Broader participation:** Smaller holders can participate

### Multichain Support

With MultiGov, govern from any chain:

- **Cross-chain voting:** Vote from Ethereum, L2s, or Solana
- **Unified governance:** Single governance system across chains
- **Meet users where they are:** No bridge requirements for voting

## Governance Models

### Standard Governor

OpenZeppelin Governor compatible:

- Industry-standard implementation
- Flexible parameter configuration
- Wide ecosystem support
- Audited and battle-tested

### Optimistic Governance

Faster execution with veto protection:

- Proposals pass unless vetoed
- Reduces governance overhead
- Maintains community oversight
- Suitable for routine decisions

### Timelocked Governance

Added security for critical decisions:

- Delay between approval and execution
- Time for community review
- Emergency cancellation possible
- Standard for high-stakes changes

## Configuration Options

### Voting Parameters

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Voting Period | Duration of voting | 3-7 days |
| Voting Delay | Time before voting starts | 1-2 days |
| Proposal Threshold | Tokens needed to propose | 0.1-1% of supply |
| Quorum | Minimum participation | 4-10% of supply |

### Execution Parameters

| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| Timelock Delay | Time before execution | 2-7 days |
| Grace Period | Time to execute after approval | 7-14 days |

## Getting Started with Governance

### For New Projects

1. **Define parameters:** Set voting periods, thresholds, quorum
2. **Deploy contracts:** Tally deploys Governor and Timelock
3. **Configure interface:** Branded governance portal
4. **Launch:** Go live with governance

### For Existing Projects

1. **Compatibility check:** Verify contract compatibility
2. **Add to Tally:** Register your DAO on Tally
3. **Configure features:** Enable advanced features
4. **Migrate users:** Direct community to Tally interface

## Integration with Token Sales

### Post-Sale Governance

After your token sale:

- Governance can be active from day one
- Locked tokens can participate in voting
- Delegation available for all holders
- Treasury immediately under governance control

### Progressive Decentralization

Start controlled, become decentralized:

1. **Phase 1:** Team retains significant voting power
2. **Phase 2:** Community gains majority
3. **Phase 3:** Full community control

## Advanced Features

### Security Council Integration

Combine with security councils:

- Councils handle emergencies
- Governance handles routine decisions
- Clear separation of concerns
- Maximum decentralization with safety

See [Security Councils](security-councils.md)

### Staking Integration

Governance participation can be rewarded:

- Voting rewards for active participants
- Delegation rewards for representatives
- Staking with governance rights preserved

See [Staking & Incentives](staking-incentives.md)

## Supported Contract Standards

### OpenZeppelin Governor

Full support for OZ Governor:

- All standard extensions
- Custom extensions possible
- Upgrade paths available

### Compound Governor Bravo

Support for legacy contracts:

- Bravo compatibility
- Migration to OZ available

## Best Practices

### Parameter Selection

Choose parameters carefully:

- **Voting period:** Long enough for participation, short enough for agility
- **Quorum:** High enough for legitimacy, low enough to pass
- **Thresholds:** Low enough for access, high enough to prevent spam

### Proposal Guidelines

Establish clear guidelines:

- Proposal format standards
- Discussion requirements before voting
- Voting rationale expectations

### Delegation Culture

Encourage healthy delegation:

- Delegate discovery and profiles
- Delegate accountability metrics
- Regular delegate elections or reviews

## Resources

For detailed technical documentation:

- [Deploying DAOs](/set-up-and-technical-documentation/deploying-daos/)
- [Governor Proposals](/set-up-and-technical-documentation/governor-proposals/)
- [DAO Settings](/set-up-and-technical-documentation/managing-a-dao/dao-settings.md)

## Next Steps

- [Voting & Delegation](voting-delegation.md) - Participation mechanisms
- [Security Councils](security-councils.md) - Oversight and security
- [Staking & Incentives](staking-incentives.md) - Reward programs
- [Talk to our team](http://tally.xyz/contact) - Launch governance
