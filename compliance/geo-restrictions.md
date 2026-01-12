---
description: Geographic controls and regional restrictions for token sales
---

# Geo-Restrictions

Geographic restrictions help you comply with regional regulations by controlling where your token sale is accessible. Tally provides robust geo-blocking capabilities to ensure your sale only reaches permitted jurisdictions.

## Why Geo-Restrictions Matter

### Regulatory Compliance

Different jurisdictions have different rules:

- Some prohibit token sales entirely
- Others require specific registrations
- Participant protections vary by region
- Securities laws differ globally

### Risk Management

Blocking high-risk jurisdictions:

- Reduces legal exposure
- Simplifies compliance requirements
- Protects against enforcement actions
- Clarifies regulatory position

## How Geo-Blocking Works

### Detection Methods

Tally uses multiple signals to determine participant location:

**IP-based detection:**
- Primary location signal
- Geolocation databases
- Regular database updates

**VPN detection:**
- Identify common VPN services
- Data center IP flagging
- Behavioral analysis

**KYC verification:**
- Document-based location confirmation
- Address verification
- Most reliable method

### Enforcement Layers

Multiple enforcement points:

1. **Frontend blocking:** Prevent access to sale page
2. **Wallet screening:** Check address history and patterns
3. **KYC verification:** Verify location through documents
4. **Smart contract:** On-chain enforcement where applicable

## Configuration Options

### Blocklist vs. Allowlist

**Blocklist approach:**
- Block specific countries/regions
- Allow all others
- Simpler for broad sales

**Allowlist approach:**
- Allow specific countries/regions
- Block all others
- More restrictive, maximum control

### Regional Settings

Configure at multiple levels:

| Level | Example | Use Case |
|-------|---------|----------|
| Country | United States | National regulations |
| State/Province | New York | State-specific rules |
| Region | OFAC sanctioned | Sanctions compliance |
| Custom | Specific list | Project requirements |

### Restriction Severity

Different actions for restricted regions:

- **Hard block:** Cannot access or participate
- **Soft block:** Warning message, can proceed with acknowledgment
- **Limited access:** Can view but not purchase
- **Enhanced requirements:** Additional verification needed

## Common Restricted Jurisdictions

### Typically Blocked

Most token sales restrict:

<<TODO: Add list of commonly blocked jurisdictions with brief explanations (e.g., OFAC-sanctioned countries, known high-risk jurisdictions)>>

### US Considerations

United States requires special attention:

- Federal securities laws
- State-by-state variations
- Accredited investor requirements
- BitLicense states (New York)

<<TODO: Add more detailed US jurisdiction guidance>>

### EU Considerations

European Union under MiCA:

- Pan-EU framework coming into effect
- Member state variations
- Prospectus requirements
- Consumer protection rules

<<TODO: Add more detailed EU jurisdiction guidance>>

## Implementation

### Technical Setup

Tally configures geo-blocking:

1. **Define restricted regions:** Provide your blocklist/allowlist
2. **Select detection methods:** IP, VPN detection, KYC
3. **Configure enforcement:** Hard/soft blocking, warnings
4. **Test configuration:** Verify correct behavior

### Integration with KYC

Geo-restrictions work with KYC:

- Location verified through documents
- More reliable than IP-based detection
- Supports region-specific requirements
- Creates audit trail

### Smart Contract Integration

On-chain enforcement options:

- Address allowlists in contracts
- Attestation-based verification
- Integration with on-chain identity

## Region-Specific Rules

### Differentiated Treatment

Some sales need varied rules by region:

| Region | KYC Level | Lockup | Allocation |
|--------|-----------|--------|------------|
| US Accredited | KYI | 12 months | Unlimited |
| EU | KYC | 6 months | $50,000 max |
| Asia | KYC | None | $25,000 max |

### Lockup Variations

Different lockups by jurisdiction:

- Regulatory requirements may mandate lockups
- Optionally extend for certain regions
- On-chain enforcement via vesting contracts

See [Vesting & Lockups](vesting-lockups.md) for details.

## Handling Edge Cases

### VPN Usage

Participants may try to circumvent restrictions:

- VPN detection helps identify
- KYC provides verification
- Terms of service prohibit circumvention
- Technical measures are not foolproof

### Expatriates and Travelers

Address common questions:

- Citizenship vs. residence rules
- Temporary travel handling
- Document requirements for expats

### Dual Citizens

Handle multiple citizenship:

- Define policy clearly
- Most restrictive approach common
- Document in terms of service

## Compliance Documentation

### Record Keeping

Maintain records of:

- Restriction configuration
- Blocked access attempts
- Override decisions
- Policy changes

### Terms of Service

Your terms should include:

- Geographic restrictions clearly stated
- Prohibited circumvention
- Participant representation of location
- Consequences of misrepresentation

### Legal Disclaimers

Standard disclaimers:

<<TODO: Add example disclaimer language for geographic restrictions>>

## Best Practices

### Conservative Approach

When in doubt:

- Block rather than allow
- Consult legal counsel
- Document decision rationale

### Clear Communication

Inform participants:

- List restricted jurisdictions clearly
- Explain why restrictions exist
- Provide guidance for edge cases

### Regular Review

Regulations change:

- Monitor regulatory developments
- Update restrictions as needed
- Document all changes

## Testing Your Configuration

Before launch:

- [ ] Test access from blocked regions (via VPN)
- [ ] Verify blocking messages display correctly
- [ ] Confirm KYC flow respects geo-restrictions
- [ ] Test edge cases and overrides

## Next Steps

- [KYC Verification](kyc-verification.md) - Identity verification
- [Vesting & Lockups](vesting-lockups.md) - Token lockup mechanisms
- [Compliance Overview](README.md) - Full compliance guide
