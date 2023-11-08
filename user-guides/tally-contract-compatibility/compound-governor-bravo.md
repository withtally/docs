---
description: How to deploy a Governor Bravo or Alpha that's compatible with Tally
---

# Compound Governor Bravo

Tally supports [Compound Governor Bravo](https://github.com/compound-finance/compound-protocol/blob/master/contracts/Governance/GovernorBravoDelegate.sol) and Alpha, but we consider it deprecated. If you are deploying a new Governor, we recommend [OpenZeppelin's Governor.](../smart-contract-compatibility/openzeppelin-governor.md) OZ Governor is more actively maintained and has all of Bravo's features.

&#x20;If you're already using a direct fork of Governor Bravo, then your DAO should work with Tally out of the box. If you insist on making changes to the base contract, then you can use this guide to make sure that your changes are compatible with Tally's API and web interface.

### Event signatures

Tally's API listens to event logs from Governor contracts when indexing them. Your contract will need to maintain the same event signatures that OZ Governor implements:

```
event ProposalCreated(
    uint id, 
    address proposer, 
    address[] targets, 
    uint[] values, 
    string[] signatures, 
    bytes[] calldatas, 
    uint startBlock, 
    uint endBlock, 
    string description
);

event VoteCast(
    address indexed voter, 
    uint proposalId, 
    uint8 support, 
    uint votes, 
    string reason
);

event ProposalCanceled(uint id);
event ProposalQueued(uint id, uint eta);
event ProposalExecuted(uint id);
```

### Function signatures

Tally's frontend app helps users make web3 calls to your Governor contract. The app lets users create Proposals as well as vote on, queue and execute them.

To be compatible with Tally, your Governor will need these function signatures:

```
function castVote(uint proposalId, uint8 support) external
function castVoteWithReason(
    uint proposalId, 
    uint8 support, 
    string reason
) external

function castVoteBySig(
    uint proposalId, 
    uint8 support, 
    uint8 v, 
    bytes32 r, 
    bytes32 s
) external

function state(uint proposalId) public view returns (ProposalState)

function propose(
    address[] memory targets, 
    uint[] memory values, 
    string[] memory signatures, 
    bytes[] memory calldatas, 
    string memory description
) public returns (uint)

function execute(uint proposalId) external payable
function queue(uint proposalId) external
function cancel(uint proposalId) external
```

### State variables

The Tally app need reads state from the public getters of these state variables:

```
uint public votingDelay;
uint public votingPeriod;
uint public proposalThreshold;
uint public constant quorumVotes;
```

#### Quorum

Tally needs the quorum to figure out whether a proposal passed.

Tally expects a `quorum` constant:

```
uint public constant quorumVotes;
```

_Note that the_ [_OpenZeppelin interface_](../smart-contract-compatibility/openzeppelin-governor.md) _uses a function instead of a constant for quorum._

#### Voting Delay

For Governor Bravo, Tally uses the voting delay to know when voting starts. Governor Alpha does not have a voting delay. For Governor Bravo, a `votingDelay` constant on Governor is required:

```
uint public votingDelay;
```

_Note that the_ [_OpenZeppelin interface_](../smart-contract-compatibility/openzeppelin-governor.md) _uses a function instead of a constant for voting delay._

#### Voting Period

Tally uses the voting period to correctly show the end of voting. A `votingPeriod()` constant on Governor is required:

```
uint public votingPeriod;
```

_Note that the_ [_OpenZeppelin interface_](../smart-contract-compatibility/openzeppelin-governor.md) _uses a function instead of a constant for voting period._

### Proposal state lifecycle

Tally's app expects the following proposal states. If your Governor uses a custom proposal lifecycle, those states won't show up correctly on on Tally:

```
enum ProposalState {
    Pending,
    Active,
    Canceled,
    Defeated,
    Succeeded,
    Queued,
    Expired,
    Executed
}
```



### Governor Parameter Changes

Governors can change their own parameters, like proposal times and the amount of voting power required to create and pass proposals. To make sure that Tally indexes your Governor's parameter changes, implement these event signatures:

```
 event VotingDelaySet(uint256 oldVotingDelay, uint256 newVotingDelay);
 event VotingPeriodSet(uint256 oldVotingPeriod, uint256 newVotingPeriod);
 event ProposalThresholdSet(uint256 oldProposalThreshold, uint256 newProposalThreshold);
```
