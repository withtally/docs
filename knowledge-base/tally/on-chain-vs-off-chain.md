---
description: Why should DAOs be onchain?
---

# ⛓ Onchain vs Offchain

> _With onchain DAOs, voters don’t need to trust that admins will honor the results of a vote. Smart contracts automatically implement successful proposals._

## Why Onchain?

**Onchain votes execute proposals trustlessly. Off-chain votes don't.**

<figure><img src="../../.gitbook/assets/on-chain vs off-chain (1).jpg" alt=""><figcaption><p>Off-chain voting requires social trust.</p></figcaption></figure>

Smart contracts can be designed to execute proposals automatically based on the outcome of onchain votes, removing the need for a trusted third party or core team to enact vote results. Examples of onchain voting systems include MakerDAO, Aave, and protocols built on Compound's governance framework.

### **Benefits of Onchain Voting:**

* No trusted third party required to count or enact votes
* Passed proposals execute automatically and trustlessly
* Works well for approving protocol changes or other high-stakes votes

## How Is Tally different than Snapshot?

The big difference between Tally and off-chain voting tools like [Snapshot](https://snapshot.org/) and others is that Tally supports fully onchain DAOs.

**Onchain DAOs use smart contracts to propose, vote on and execute proposals. That makes DAO operations automated, trustless, and more decentralized.**

The [Governor smart contract](governor-framework.md) is responsible for managing proposals, counting votes and executing passed proposals onchain with no human intervention. The benefit of a Governor DAO is that the token holders or NFT membership holders have direct control over the protocol and/or treasury through voting. Holders don’t have to trust their multi-sig signers to execute a proposal vote, and they don’t have to worry about rogue multi-sig signers creating a transaction that wasn’t approved by the voters. The tradeoff is that creating onchain proposals and voting isn't free: it costs gas.

For more information about deploying or upgrading to an onchain DAO, see [deploying-daos](../../user-guides/deploying-daos/ "mention").
