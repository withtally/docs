---
description: What is Tally and how is it used for on-chain DAO coordination?
---

# ⚡ Understanding Tally

> **Tally is a platform for on-chain decentralized organizations.**
>
> Tally provides a user-friendly interface that makes it accessible for anyone to start, join, and grow DAOs. DAO members use Tally to manage governance, as well as to create, pass, and execute governance proposals.

## What is a DAO?

A DAO is a **Decentralized Autonomous Organization**.&#x20;

DAOs operate via decentralized governance. Members engage in open, democratic processes to make decisions, manage their funds, maintain and improve their products, and invest in growth. For on-chain DAOs, decisions made via decentralized governance are executed _trustlessly_ using smart contracts.

## What is Governor?

DAOs typically use [DAO governance frameworks](https://blog.tally.xyz/a-pocket-guide-to-dao-frameworks-8d7ad5af3a1b) to enable decentralized governance. Tally supports [OpenZeppelin Governor](../../user-guides/smart-contract-compatibility/openzeppelin-governor.md), which is the most popular DAO governance framework.&#x20;

The Governor contract pattern is a commonly used open-source smart contract that allows token holders to control a DAO with fully on-chain voting.&#x20;

The Governor contract is responsible for managing DAO proposals. It keeps track of the status of proposals, and it counts the votes to see if they pass. If a proposal passes, the Governor executes the proposal on-chain.&#x20;

Proposals can do anything that's on chain: send funds from a treasury, update the parameters of a DeFi protocol, change permissions of sub DAOs, mint NFTs, or modify the rules of the Governor itself.

## What is a token contract?

A Governor contract needs a token contract. The token contract provides the Governor the voting power of different addresses. Tally supports Governors that work with both fungible (ERC20) and non-fungible (ERC721) token contracts.

## Why do DAOs use Governor?

The main benefit of the Governor pattern is that the DAO's decision-making happens completely on-chain. Token voters don’t need to trust a third party to count their votes or to execute their transactions, because the smart contract does it entirely on-chain.

## Is Governor customizable?

Yes! Tally’s app expects a certain interface, but there’s lots of flexibility within that interface. OpenZeppelin’s version has several different modules, and the code is fully customizable with their [deployment wizard](https://wizard.openzeppelin.com/). If you make changes to the contract, you can test them on Tally by deploying to a testnet.

To learn more about how to deploy a Governor, head over to [deploying-daos](../../user-guides/deploying-daos/ "mention").

If you want to know what changes will and won't work with Tally, check out [smart-contract-compatibility](../../user-guides/smart-contract-compatibility/ "mention").

{% content-ref url="tally-faqs.md" %}
[tally-faqs.md](tally-faqs.md)
{% endcontent-ref %}