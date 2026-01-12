---
description: Democratic oversight for protocol security
---

# Security Councils

Security council elections are a pivotal aspect of decentralized governance, ensuring that the guardianship of a protocol remains in the hands of its community. With Tally's custom-built council elections, elevate your organization's oversight to the highest standards of excellence and integrity.

## What is a Security Council?

A security council is a group of elected members with authority to take rapid action in emergencies. Unlike slow governance processes, councils can respond quickly to threats while maintaining community legitimacy through elections.

### Roles and Responsibilities

Council members typically handle:

- **Emergency actions:** Rapid response to critical situations threatening user funds
- **Routine operations:** Software updates, maintenance, parameter adjustments
- **Protocol oversight:** Monitoring for risks and vulnerabilities
- **Upgrade execution:** Implementing governance-approved changes

### Why Councils Matter

Councils solve the speed vs. decentralization tradeoff:

- **Security:** Rapid response to threats
- **Legitimacy:** Community-elected members
- **Accountability:** Regular elections enforce accountability
- **Resilience:** Distributed control prevents single points of failure

## Election Process

Tally runs democratic elections to select council members:

### Election Phases

1. **Nomination:** Candidates register and meet minimum requirements
2. **Compliance:** Foundation or team vets nominees
3. **Voting:** Delegates vote for preferred candidates
4. **Results:** Top candidates become council members
5. **Implementation:** New members onboarded to council

### Typical Timeline

| Phase | Duration | Activities |
|-------|----------|------------|
| Nomination | 1-2 weeks | Candidate registration, endorsement gathering |
| Compliance | 1 week | Background verification, eligibility confirmation |
| Voting | 2 weeks | Community voting, often with declining weight |
| Transition | 1 week | Outgoing/incoming member handoff |

### Voting Mechanics

Elections can use various voting methods:

- **Weighted voting:** Based on token holdings or delegation
- **Declining weight:** Voting power decreases over time (encourages early voting)
- **Quadratic voting:** Reduces whale influence
- **Ranked choice:** Multiple preferences per voter

## Council Structure

### Composition

Typical council structures:

| Element | Example | Rationale |
|---------|---------|-----------|
| Total Members | 12 | Enough for diversity, small enough for coordination |
| Cohorts | 2 (6 each) | Staggered elections for continuity |
| Term Length | 12 months | Regular accountability |
| Election Frequency | Every 6 months | Half council elected each cycle |

### Quorum Requirements

Different actions require different approval levels:

| Action Type | Typical Quorum | Example |
|-------------|----------------|---------|
| Emergency | 9/12 (75%) | Pause contracts |
| Non-Emergency | 7/12 (~58%) | Parameter changes |
| Routine | 5/12 (~42%) | Minor updates |

## Security Measures

### Constrained Access

Councils operate with limited, defined powers:

- Access only to specific functions
- No unilateral control over treasury
- Actions logged and auditable
- Emergency powers time-limited

### Timelocks and Delays

Non-emergency actions include delays:

- Gives community time to review
- Enables veto through governance if needed
- Balances speed with oversight

### Transparency

All council actions are visible:

- On-chain execution
- Public meeting notes
- Decision documentation
- Regular community updates

## Integration with Governance

### Separation of Concerns

Councils and governance have distinct roles:

| Domain | Governance | Council |
|--------|------------|---------|
| Routine decisions | Yes | No |
| Treasury allocation | Yes | No |
| Emergency response | No | Yes |
| Technical upgrades | Approval | Execution |
| Parameter changes | Major | Minor |

### Governance Oversight

Councils remain accountable to governance:

- Elections through governance process
- Council actions can be reviewed
- Governance can modify council powers
- Community retains ultimate authority

## Use Cases

### Protocol Security

Respond to vulnerabilities:

- Pause affected contracts
- Deploy fixes rapidly
- Coordinate disclosure
- Manage communication

### Network Operations

Maintain protocol health:

- Update contract parameters
- Deploy approved upgrades
- Monitor network status
- Coordinate with operators

### Compliance Response

Handle regulatory issues:

- Implement required changes
- Coordinate with legal counsel
- Document decisions
- Maintain compliance

## Implementation

### Setup Process

1. **Design structure:** Members, terms, quorums
2. **Define powers:** What can the council do?
3. **Deploy contracts:** Multisig with appropriate controls
4. **Run election:** Select initial members
5. **Go live:** Council begins operations

### Technical Requirements

- **Multisig wallet:** Safe or similar for execution
- **Governance integration:** For elections and oversight
- **Communication channels:** For coordination
- **Documentation system:** For transparency

## Best Practices

### Candidate Selection

Look for council members with:

- Technical expertise
- Protocol familiarity
- Security background
- Availability and commitment
- Community trust

### Operational Excellence

Run effective councils:

- Regular meetings and communication
- Clear escalation procedures
- Documented decision processes
- Transparent reporting

### Accountability

Maintain community trust:

- Public meeting notes
- Decision rationale documentation
- Regular community updates
- Responsiveness to community concerns

## Case Study: Arbitrum DAO

<<TODO: Add detailed case study of Arbitrum's Security Council implementation, including structure, election process, and outcomes>>

## Next Steps

- [Governance Overview](governance-overview.md) - Governance integration
- [Voting & Delegation](voting-delegation.md) - Election mechanics
- [Staking & Incentives](staking-incentives.md) - Council compensation
- [Talk to our team](http://tally.xyz/contact) - Implement councils
