---
description: Identity verification for token sale participants
---

# KYC Verification

Know Your Customer (KYC) verification helps ensure your token sale meets regulatory requirements by verifying participant identities. Tally integrates KYC seamlessly into the sale flow, balancing compliance with user experience.

## Types of Verification

### KYC - Know Your Customer

Standard individual identity verification:

- **Purpose:** Verify individual participant identity
- **Documents:** Government ID, proof of address
- **Use case:** Retail participants

### KYB - Know Your Business

Business entity verification:

- **Purpose:** Verify business entities and beneficial owners
- **Documents:** Business registration, ownership structure
- **Use case:** Corporate participants, DAOs

### KYI - Know Your Investor

Accredited investor verification:

- **Purpose:** Verify accredited investor status
- **Documents:** Financial statements, professional certifications
- **Use case:** Sales requiring accredited investors

## How KYC Works in Tally

### Participant Flow

1. **Connect Wallet:** Participant connects their wallet to the sale page
2. **Start Verification:** Redirected to KYC provider interface
3. **Submit Documents:** Upload required identity documents
4. **Verification:** Provider verifies documents (usually minutes)
5. **Approval:** Wallet address is approved for participation
6. **Purchase:** Participant can now buy tokens

### Project Configuration

Configure KYC requirements:

| Setting | Options | Description |
|---------|---------|-------------|
| Verification Level | KYC, KYB, KYI | Type of verification required |
| Required Documents | ID, Proof of Address, etc. | Documents participants must provide |
| Approval Flow | Auto, Manual | Automatic or manual approval |
| Validity Period | 30-365 days | How long verification remains valid |

## Integrated Providers

Tally integrates with leading KYC providers:

<<TODO: List specific KYC provider integrations with brief descriptions of each>>

### Provider Selection Criteria

When choosing a provider, consider:

- **Geographic coverage:** Support for your target regions
- **Verification speed:** Time to complete verification
- **User experience:** Ease of use for participants
- **Document support:** ID types accepted
- **Compliance standards:** Certifications and audits

## Configuration Options

### Verification Requirements

Define what's required:

**Minimum verification:**
- Government-issued photo ID
- Selfie/liveness check

**Enhanced verification:**
- Proof of address
- Source of funds declaration
- Additional screening

### Approval Workflows

**Automatic approval:**
- Verification completes instantly when documents clear
- Best for standard KYC requirements
- Faster participant experience

**Manual review:**
- Team reviews before final approval
- Required for edge cases or enhanced due diligence
- Adds processing time

### Re-verification

Set policies for ongoing verification:

- Validity period before re-verification required
- Triggers for additional verification (large purchases, etc.)
- Handling of expired verifications

## User Experience Considerations

### Minimizing Friction

KYC can create friction. Reduce impact by:

- Allowing pre-registration before sale starts
- Clear communication about requirements
- Fast verification provider
- Responsive support for issues

### Communication

Set expectations clearly:

- Explain why KYC is required
- List required documents in advance
- Provide estimated verification time
- Offer support channels

### Common Issues

**Document rejection:**
- Provide clear guidance on acceptable documents
- Allow multiple submission attempts
- Have support available to assist

**Verification delays:**
- Set realistic time expectations
- Consider opening verification early
- Plan for peak demand

## Privacy and Data Handling

### Data Storage

KYC data is handled securely:

- Stored by KYC provider, not Tally
- Encrypted at rest and in transit
- Retention policies per regulations
- Deletion upon request where permitted

### Participant Privacy

Respect participant privacy:

- Collect minimum necessary data
- Clear privacy policies
- Transparent about data usage
- Honor deletion requests

<<TODO: Add specific data handling policies and privacy commitments>>

## Compliance Considerations

### Regulatory Requirements

Different jurisdictions require different verification levels:

| Jurisdiction | Typical Requirement |
|--------------|---------------------|
| United States | KYC + Accredited (for some sales) |
| European Union | KYC per MiCA framework |
| Singapore | KYC per MAS guidance |
| Other | Varies by jurisdiction |

### Sanctions Screening

All verifications include:

- OFAC screening (US sanctions)
- EU sanctions list screening
- Other relevant sanctions lists
- Ongoing monitoring

### Record Keeping

Maintain compliance records:

- Verification completion records
- Document retention per regulations
- Audit trail for approvals
- Compliance reporting

## Best Practices

### Pre-Sale Preparation

Before your sale:

- Select and test KYC provider
- Open verification 1-2 weeks early
- Prepare support documentation
- Train support team on common issues

### During the Sale

Active management:

- Monitor verification queue
- Respond quickly to escalations
- Track completion rates
- Communicate proactively about issues

### Post-Sale

Ongoing compliance:

- Retain records per requirements
- Monitor for regulatory changes
- Update processes as needed

## Troubleshooting

### Common Issues

**Low completion rates:**
- Review document requirements
- Check user experience friction
- Verify geographic coverage

**Slow verification:**
- Check provider capacity
- Review manual review queue
- Consider additional provider

**High rejection rates:**
- Improve document guidance
- Review rejection reasons
- Adjust requirements if appropriate

## Next Steps

- [Geo-Restrictions](geo-restrictions.md) - Geographic controls
- [Vesting & Lockups](vesting-lockups.md) - Token lockup mechanisms
- [Running Your Sale](../token-sales/running-your-sale.md) - Execution guide
