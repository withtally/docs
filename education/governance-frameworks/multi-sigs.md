# Multi-sigs

**Key Facts:**

* Usually paired with [off chain voting](https://wiki.withtally.com/docs/on-chain-vs-off-chain-voting)
* Signers may be elected by vote, or unelected team members

**Protocols:**

* Synthetix
* Yearn Finance
* Sushiswap

**What is a multisig?:**

A multisig (also known as a multisignature wallet) is a smart contract that offers hightened security for funds or sensative admin controls. Control over the contract is split between several individual "signers" (other individuals with a linked wallet address), and "M of N" signers are required to approve any transactions from the multisig.

As an example, a 2 of 3 multisig would require 2 of the 3 linked signer addresses to approve a transaction before it can be sent. By splitting authority among several signers, multisigs help reduce the risk of governance attacks or self dealing.

[Gnosis Safe](https://gnosis-safe.io/) is the most prominent Ethereum multisig, with hundreds of millions of assets secured over several years.

**Background:**

While fully on chain voting and proposal execution is often seen as the gold standard of decentralized governance, there are several tradeoffs.

Protocols could face technical or crypto economic vulnerabilities in their governance mechanism, or be faced with a hostile takeover. Even without any adverse events taking place, on chain governance is necessarily more costly and less agile than other execution methods such as multisigs. Each voter needs to submit a transaction on chain to participate (costing gas), and proposal voting and timelock periods add considerable delay.

Multisigs offer a different set of pros and cons. While protocols must rely on multisig signers to act honestly and respond to signature requests, relying on known individuals can in some cases be less risky than granting all power to anonymous token holders.

There are tradeoffs between multisig and on chain governance mechanisms, but it is generally accepted that they are both much better and more reliable than allowing a single signer to control governance. In one example from mid 2020, pseudonomous Sushiswap founder Chef Nomi [cashed out over $10 million](https://www.coindesk.com/sushiswap-creator-chef-nomi-returns-dev-fund), made possible by his directly control over the development fund through a single signature wallet with no oversight.

**Governance Process:**

Multisig governance is typically paired with a signal voting mechanism to maintain legitimacy. As an example, Yearn, Synthetix, and Sushiswap all use the Snapshot voting tool to let token holders make key decisions and delegate authority.

After considering a proposal in the community's discussion venue, a signal vote will be held to assess support. While this typically involves voting with Snapshot, in some cases communities may use on chain signal voting (eg. early Yearn [ygov.finance voting tool](https://ygov.finance/vote)) or off chain voting which is weighted by user accounts instead of token holdings (eg. polls in Discourse forums or Discord).

Regardless of voting system used (on or off chain, weighted by users or token holdings), the vote itself doesn't trigger execution of the proposal's effects. Instead, the vote serves as instructions for the multisig signers to execute the proposal using their admin priveledges.

**Drawbacks:**

Multisigs can act against the will of their community or voters. With tokens used merely for signalling but lacking any executive control, it's possible for multisigs to slowly diverge from their community's interest. If multisigs are comprised of core team members, there may also be conflict on compensation and profit sharing.

Multisigs have a small number of identifiable signers, which makes them a clear target for government regulation, legal actions, or other attacks. Multisig signers' discretion in executing their authority could also cause liability issues. So a distributed set of token holders could potentially offer greater censorship resistance.

**Resources:**

* Synthetix Spartan Council announcements: [https://blog.synthetix.io/tag/spartan-council/](https://blog.synthetix.io/tag/spartan-council/)
* Synthetix protocol DAO announcement: [https://blog.synthetix.io/synthetix-foundation-decommissioned/](https://blog.synthetix.io/synthetix-foundation-decommissioned/)
* Sushiswap multisig announcement (via DefiRate): [https://defirate.com/sushiswap-admin-multisig/](https://defirate.com/sushiswap-admin-multisig/)
* Yearn Finance multisig governance proposal: [https://gov.yearn.finance/t/empower-the-multisig/2891](https://gov.yearn.finance/t/empower-the-multisig/2891)
* Gnosis multisig app: [https://gnosis-safe.io/](https://gnosis-safe.io/)
* Gnosis multisig github: [https://github.com/gnosis/MultiSigWallet](https://github.com/gnosis/MultiSigWallet)