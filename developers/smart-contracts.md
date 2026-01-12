---
description: Smart contract documentation and integration guide
---

# Smart Contracts

This documentation covers the smart contracts used in Tally's token sale and governance infrastructure, including addresses, ABIs, and integration patterns.

## Contract Overview

### Token Sale Contracts

| Contract | Purpose | Chains |
|----------|---------|--------|
| LBP Controller | Manages LBP sales | Ethereum, L2s |
| CCA Controller | Manages CCA auctions | Ethereum, L2s |
| Fixed Sale | Fixed-price sale logic | Ethereum, L2s |
| Vesting | Token lockups | All supported |

### Governance Contracts

| Contract | Purpose | Standard |
|----------|---------|----------|
| Governor | Proposal and voting | OZ Governor |
| Timelock | Execution delay | OZ TimelockController |
| Token | Governance token | ERC20Votes |

### Staking Contracts

| Contract | Purpose | Features |
|----------|---------|----------|
| Staking | Token staking | Rewards, governance |
| LST | Liquid staking token | ERC20, composable |
| Rewards | Distribution logic | Multiple tokens |

## Contract Addresses

### Mainnet

<<TODO: Add mainnet contract addresses>>

| Contract | Address | Verified |
|----------|---------|----------|
| LBP Controller | `0x...` | Etherscan |
| CCA Controller | `0x...` | Etherscan |
| Vesting Factory | `0x...` | Etherscan |

### Arbitrum

<<TODO: Add Arbitrum contract addresses>>

### Base

<<TODO: Add Base contract addresses>>

### Testnets

<<TODO: Add testnet contract addresses for development>>

## ABIs

### Obtaining ABIs

ABIs are available via:

1. **Verified contracts:** Etherscan and block explorers
2. **NPM package:** `@tally/contracts`
3. **GitHub:** Contract repository
4. **API:** `GET /v1/contracts/{address}/abi`

### NPM Package

```bash
npm install @tally/contracts
```

```typescript
import { LBPController__factory } from '@tally/contracts';

const controller = LBPController__factory.connect(
  contractAddress,
  signer
);
```

## Integration Patterns

### Reading Sale Data

Query sale state from contracts:

```typescript
// Get sale information
const saleInfo = await controller.getSaleInfo(saleId);

// Get participant allocation
const allocation = await controller.getAllocation(saleId, userAddress);

// Check if sale is active
const isActive = await controller.isActive(saleId);
```

### Participating in Sales

Interact with sale contracts:

```typescript
// Approve token spend (for payment token)
await paymentToken.approve(controllerAddress, amount);

// Participate in sale
await controller.participate(saleId, amount, {
  gasLimit: estimatedGas
});
```

### Claiming Tokens

Claim purchased/vested tokens:

```typescript
// Check claimable amount
const claimable = await vesting.getClaimableAmount(userAddress);

// Claim tokens
await vesting.claim();
```

### Governance Integration

Interact with governance:

```typescript
// Create proposal
const proposalId = await governor.propose(
  targets,
  values,
  calldatas,
  description
);

// Cast vote
await governor.castVote(proposalId, support);

// Execute proposal
await governor.execute(
  targets,
  values,
  calldatas,
  descriptionHash
);
```

## Events

### Sale Events

Monitor sale activity:

```solidity
event SaleCreated(uint256 indexed saleId, address indexed creator);
event Participated(uint256 indexed saleId, address indexed participant, uint256 amount);
event SaleCompleted(uint256 indexed saleId, uint256 totalRaised);
event TokensClaimed(uint256 indexed saleId, address indexed participant, uint256 amount);
```

### Governance Events

Monitor governance activity:

```solidity
event ProposalCreated(uint256 proposalId, address proposer, ...);
event VoteCast(address indexed voter, uint256 proposalId, uint8 support, uint256 weight);
event ProposalExecuted(uint256 proposalId);
```

### Listening to Events

```typescript
// Filter for participation events
const filter = controller.filters.Participated(saleId, null, null);

// Listen for new events
controller.on(filter, (saleId, participant, amount, event) => {
  console.log(`${participant} participated with ${amount}`);
});

// Query historical events
const events = await controller.queryFilter(filter, fromBlock, toBlock);
```

## Security Considerations

### Contract Verification

Always verify contracts before interaction:

1. Check contract is verified on block explorer
2. Verify address matches official documentation
3. Review audit reports
4. Compare bytecode if needed

### Transaction Safety

Safe transaction practices:

- Simulate transactions before sending
- Set appropriate gas limits
- Use slippage protection where applicable
- Verify transaction parameters

### Approval Management

Manage token approvals carefully:

- Approve only required amounts
- Revoke unused approvals
- Use permit where supported
- Monitor approval status

## Audit Reports

### Token Sale Contracts

<<TODO: Add links to audit reports>>

| Auditor | Date | Report |
|---------|------|--------|
| [Auditor 1] | 2024-XX | [Link] |
| [Auditor 2] | 2024-XX | [Link] |

### Governance Contracts

Tally uses OpenZeppelin contracts:

- [OpenZeppelin Governor Audit](https://github.com/OpenZeppelin/openzeppelin-contracts/tree/master/audits)
- Additional custom logic audits: <<TODO: Add links>>

### Staking Contracts

<<TODO: Add staking contract audit links>>

## Upgradeability

### Upgrade Patterns

Tally contracts use established upgrade patterns:

- **Proxy patterns:** UUPS or Transparent Proxy
- **Governance-controlled:** Upgrades require governance approval
- **Timelock protection:** Upgrade delay for review

### Checking Implementations

```typescript
// Get implementation address (for proxy contracts)
const implementation = await upgrades.erc1967.getImplementationAddress(
  proxyAddress
);
```

## Gas Optimization

### Estimated Gas Costs

<<TODO: Add gas estimates for common operations>>

| Operation | Estimated Gas |
|-----------|---------------|
| Participate in sale | ~150,000 |
| Claim tokens | ~80,000 |
| Cast vote | ~100,000 |
| Delegate | ~80,000 |

### Optimization Tips

- Batch operations where possible
- Use multicall for read operations
- Consider L2s for cost-sensitive operations
- Monitor gas prices for optimal timing

## Multichain Considerations

### Cross-Chain Deployment

Contracts are deployed on multiple chains:

- Same logic, different addresses
- Chain-specific optimizations
- Cross-chain messaging for some features

### Chain-Specific Details

<<TODO: Add chain-specific notes for each supported chain>>

## Testing

### Test Networks

Test integrations on:

- Sepolia (Ethereum)
- Arbitrum Sepolia
- Base Sepolia

### Test Tokens

<<TODO: Add faucet links and test token information>>

### Local Testing

Fork mainnet for local testing:

```bash
anvil --fork-url https://eth-mainnet.alchemyapi.io/v2/YOUR_KEY
```

## Troubleshooting

### Common Issues

**Transaction reverts:**
- Check allowances are sufficient
- Verify sale is active
- Ensure eligibility requirements met
- Review error message

**Gas estimation fails:**
- Transaction would revert
- Check contract state
- Verify parameters

**Events not appearing:**
- Check block range
- Verify filter parameters
- Consider indexing delay

## Support

For contract-related questions:

- Technical documentation: This page
- Developer Discord: <<TODO: Add link>>
- Security issues: security@tally.xyz

## See Also

- [API Documentation](api-documentation.md) - API reference
- [Developers Overview](README.md) - Getting started
