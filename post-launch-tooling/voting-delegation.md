---
description: Enable flexible governance participation
---

# Voting and Delegation

Effective governance requires broad participation. Voting and delegation mechanisms enable token holders to participate directly or through trusted representatives, ensuring all voices can be heard regardless of holdings size or technical expertise.

## Why Delegation Matters

Not every token holder can:

- Stay informed on every proposal
- Understand technical implications
- Be available during voting periods
- Pay gas costs for every vote

Delegation solves these problems by allowing holders to transfer voting power to engaged representatives while retaining token ownership.

## Voting Mechanisms

### Direct Voting

Token holders vote themselves:

- **Full control:** Voter makes every decision
- **Simple:** Connect wallet, cast vote
- **Transparent:** Votes recorded on-chain

### Delegated Voting

Transfer voting power to representatives:

- **Representative democracy:** Delegates vote on behalf of delegators
- **Flexibility:** Change delegates anytime
- **No transfer:** Tokens stay in your wallet

### Partial Delegation

Split voting power across multiple delegates:

- **Diversification:** Multiple representatives
- **Nuanced:** Different delegates for different expertise
- **Control:** Retain portion for direct voting

## Delegation Features

### Delegate Discovery

Find the right representatives:

- **Delegate profiles:** Background, expertise, positions
- **Voting history:** How delegates have voted
- **Delegation stats:** How much voting power they hold
- **Communication:** Links to delegate communications

### Delegate Statements

Delegates can share:

- Governance philosophy
- Areas of expertise
- Availability and commitment
- Contact information

### Delegation Tracking

Monitor your delegation:

- Current delegates and amounts
- Delegate voting activity
- Proposals your delegates voted on
- Alerts for important votes

## Gasless Participation

Remove financial barriers with Relay:

### Free Voting

Organizations can sponsor voting:

- Token holders vote without gas costs
- Organization pays transaction fees
- Enables participation from small holders
- Increases governance participation

### Free Delegation

Delegation without cost:

- Change delegates freely
- No barrier to participation
- Encourage active delegation management

### How It Works

1. Voter signs a message (no gas)
2. Tally submits transaction
3. Organization's wallet pays gas
4. Vote or delegation recorded on-chain

## Configuration Options

### Voting Settings

| Setting | Description | Options |
|---------|-------------|---------|
| Voting Type | How votes are cast | Simple, Weighted, Ranked |
| Vote Options | Available choices | For/Against, For/Against/Abstain |
| Voting Period | Duration for voting | Configurable |

### Delegation Settings

| Setting | Description | Options |
|---------|-------------|---------|
| Partial Delegation | Allow split delegation | On/Off |
| Delegation Cap | Max delegation to one address | Optional |
| Delegation History | Track delegation changes | On/Off |

## Integration with Token Sales

### Locked Token Voting

Participants with locked tokens can still govern:

- Voting power active during lockup
- Delegation available
- Full governance participation
- No governance disadvantage

### Early Governance Participation

Even before tokens unlock:

- Vote on proposals
- Delegate to representatives
- Shape protocol direction
- Build governance culture

## Best Practices

### For Token Holders

**If you want to vote directly:**
- Stay informed on proposals
- Review proposal details carefully
- Consider long-term implications
- Vote consistently

**If you prefer delegation:**
- Research delegates thoroughly
- Choose delegates aligned with your values
- Monitor delegate behavior
- Change delegates if needed

### For Delegates

**Build trust:**
- Publish a clear delegate statement
- Vote consistently with stated positions
- Explain voting rationale
- Communicate actively with delegators

**Participate actively:**
- Review all proposals
- Vote on every relevant proposal
- Engage in governance discussions
- Represent delegators faithfully

### For Organizations

**Encourage participation:**
- Educate on governance process
- Highlight delegate opportunities
- Enable gasless participation
- Recognize active participants

**Support delegates:**
- Provide tools for delegate discovery
- Consider delegate compensation
- Create delegate accountability mechanisms

## Advanced Features

### Delegate Compensation

Reward engaged delegates:

- Automatic compensation for active participation
- Tied to governance participation metrics
- Configurable compensation criteria

See [Staking & Incentives](staking-incentives.md) for delegate compensation details.

### Delegate Reputation Score (DRS)

Track delegate performance:

- Participation rate
- Voting consistency
- Communication quality
- Community engagement

### Flexible Voting Extension

Advanced voting patterns:

- Vote with tokens in DeFi positions
- Aggregate voting across protocols
- Preserve voting rights in complex setups

## Technical Implementation

### Supported Standards

Tally supports standard delegation:

- ERC20Votes (OpenZeppelin)
- Compound-style delegation
- Custom delegation implementations

### Integration Requirements

To enable delegation:

- Token must implement delegation
- Governor must support delegated voting
- Both standard in modern deployments

## Common Questions

### Does delegation transfer my tokens?

No. Delegation only transfers voting power. Your tokens remain in your wallet under your full control.

### Can I vote and delegate?

With partial delegation, yes. Keep some voting power for yourself and delegate the rest.

### How do I change my delegate?

Simply delegate to a new address. The previous delegation is automatically replaced.

### What happens if my delegate doesn't vote?

Your voting power goes unused for that proposal. Consider delegating to more active representatives.

## Next Steps

- [Governance Overview](governance-overview.md) - Full governance guide
- [Staking & Incentives](staking-incentives.md) - Participation rewards
- [Security Councils](security-councils.md) - Advanced oversight
- [Talk to our team](http://tally.xyz/contact) - Enable delegation
