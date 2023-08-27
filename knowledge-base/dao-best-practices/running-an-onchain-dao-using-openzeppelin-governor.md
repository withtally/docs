---
description: The best practices to ensure efficiency, security, and transparency
---

# Running an Onchain DAO Using OpenZeppelin Governor

> _Decentralized Autonomous Organizations (DAOs) have emerged as a powerful way to manage and govern decentralized projects. OpenZeppelin Governor is a popular smart contract framework that provides a robust and secure foundation for building onchain DAOs on Ethereum. These best practices will help ensure your DAO's efficiency, security, and transparency._

### 1. Use the latest version of OpenZeppelin Contracts

[OpenZeppelin Contracts](https://www.openzeppelin.com/contracts) is a library of secure and community-vetted smart contracts that provides building blocks for implementing your DAO. Always use the latest version of the library to ensure you have the most up-to-date security patches and features.&#x20;

### 2. Customize the OpenZeppelin Contract

OpenZeppelin Governor is a modular and upgradeable smart contract. It is perfectly set up right out of the box but you can customize it to suit your DAO's requirements by modifying or extending the contract. Choose the right quorum and voting mechanisms, as well as define custom actions or permissions such as the ability to cancel a proposal. If you have questions about your particular DAO requirements get in touch.&#x20;

### 3. Token Distribution

The quality of your DAO community will only be as good as its participants, thus ensuring a good token distribution at the start is key to success. Depending on your DAO's purpose, work to ensure long term alignment with token holders. Ways to do this might include a distribution heavily weighted towards users with tangible contributions to the DAO, or starting with an initially non-transferable token to prevent short-term financial speculation.&#x20;

### 4. Set a Reasonable Quorum and Voting Period

Define quorum amounts and voting durations that strike a balance between providing ample time for participants to review and vote on proposals, while ensuring the DAO can operate efficiently. Consider using Timelock Controller to enforce time restrictions on proposal execution.

Quorum represents the number of "yes" votes needed for a vote to be considered valid and pass, while the voting period is the length of time that a proposal is available to be voted on. Different DAOs will have different needs. A protocol protecting billions in dollars should have reasonably long voting periods to ensure all participants have time to vote, and a quorum that ensures a minimum number of critical participants are required for a proposal to be valid.

### 5. Encourage Delegation and Delegate Accountability

One of the most successful differentiating features of the Governor framework is the ability for voters to delegate their vote to other addresses. Using tally.xyz delegation tools is a powerful way to reward engaged, committed voters with a greater voice in your DAO. To ensure a healthy delegate system, it's important to enforce community norms around delegation and holding delegates accountable. If your DAO distribution comes from an initial airdrop, it's highly recommended that users are required to delegate to either themselves or others in order to claim tokens.&#x20;

### 6. Maintain Clear and Accessible Documentation

Provide clear and up-to-date documentation for your DAO, including the governance process, smart contract functionality, and any customizations. Accessible documentation enables a more inclusive and informed community of participants.&#x20;

### 7. Monitor and Learn from Other DAOs

Stay informed of the latest developments in the DAO ecosystem and learn from other projects' successes and challenges. Continuously iterate and improve your DAO's governance based on lessons learned from the broader community.

_This information is also available in the PDF below._

{% file src="../../.gitbook/assets/Best Practices for Running an Onchain DAO.pdf" %}
