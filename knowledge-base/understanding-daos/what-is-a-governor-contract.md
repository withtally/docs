---
description: What is a Governor contract, and why do DAOs use them?
---

# What is a Governor Contract?

## What is Governor?

The Governor contract pattern is a commonly used open-source smart contract that allows token holders to control a DAO with fully [on-chain](off-chain-vs-on-chain.md) voting.&#x20;

The Governor contract is responsible for managing DAO proposals. It keeps track of the status of proposals, and it counts the votes to see if they pass. If a proposal passes, the Governor [executes the proposal](queueing-and-executing-proposals.md) on-chain.&#x20;

Proposals can do anything that's on chain: send funds from a treasury, update the parameters of a DeFi protocol, change permissions of sub DAOs, mint NFTs, or modify the rules of the Governor itself.

## How does Governor work?

A Governor contract manages proposals and their lifecycle. For example, Compound’s proposals go through this lifecycle:

<figure><img src="https://lh4.googleusercontent.com/JrpIZE6-b5SrEwvFFx0ROL9leIvA4lAKUD8zGEWfa33Qe4DD6WVLjreV5wAqq47Y6LAGjw8KY4jR2KDKr3izH8_m-ROPV2Kd2WfRRM0U5d02h7CJxGJz1ovHxAqTjTV8FZ0l8260-Sl5j8RGqxkFVqs" alt=""><figcaption></figcaption></figure>

A Governor contract needs a **token contract**. The token contract provides the Governor the voting power of different addresses. Tally supports Governors that work with both fungible (ERC20) and non-fungible (ERC721) token contracts.

{% hint style="info" %}
_**Implementation Details**_

_The token contract needs to implement a_ [_voting interface_](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#ERC20Votes) _so that a Governor can get the voting power of voters’ addresses. If your token doesn’t already have that interface, you can_ [_deploy a wrapper contract_](https://blog.tally.xyz/how-to-add-dao-governance-to-existing-token-contracts-397855f081ac) _that does._
{% endhint %}

## Why do DAOs use Governor?

The main benefit of the Governor pattern is that the DAO's decision-making happens completely on-chain. Token voters don’t need to trust a third party to count their votes or to execute their transactions, because the smart contract does it entirely on-chain.

{% content-ref url="off-chain-vs-on-chain.md" %}
[off-chain-vs-on-chain.md](off-chain-vs-on-chain.md)
{% endcontent-ref %}

Additionally, DAOs can use whatever application interface(s) they want to interact with governance, because anyone can call the smart contract. Tally is, of course, a widely-used interface, but people also use [Sybil](https://sybil.org/#/connect) or [their own UI](https://nouns.wtf/vote). Contributors also commonly make calls directly from Etherscan or the command line.

## Who made Governor?

Governor was originally released by [Compound](https://compound.finance/docs/governance) as Governor Alpha and later Governor Bravo to run their lending protocol. That proved to be very popular! Many other projects forked that pattern.

Governor was later standardized by OpenZeppelin. They maintain [the most widely used versions of the contract](https://docs.openzeppelin.com/contracts/4.x/api/governance) as part of [their standard contracts library](https://github.com/OpenZeppelin/openzeppelin-contracts/).

## Is Governor customizable?

Yes! Tally’s app expects a certain interface, but there’s lots of flexibility within that interface. OpenZeppelin’s version has several different modules, and the code is fully customizable with their [deployment wizard](https://wizard.openzeppelin.com/). If you make changes to the contract, you can test them on Tally by deploying to a testnet.

To learn more about how to deploy a Governor, head over to [deploying-daos](../../user-guides/deploying-daos/ "mention").

If you want to know what changes will and won't work with Tally, check out [smart-contract-compatibility](../../user-guides/smart-contract-compatibility/ "mention").

## Add your Governor contract to Tally

If your DAO already has a Governor deployed, [add it to Tally here](https://tally.xyz/start-a-dao)! Tally provides an easy-to-use Governor user interface for delegating votes, creating proposals, and voting on proposals.

{% hint style="success" %}
#### _Helpful Links_

* [Compound Governor](https://compound.finance/docs/governance)
* [OpenZeppelin wizard](https://docs.openzeppelin.com/contracts/4.x/wizard)
* [OpenZeppelin docs](https://docs.openzeppelin.com/contracts/4.x/governance)
* [OpenZeppelin forums](https://forum.openzeppelin.com/)
* [OpenZeppelin Introducing OZ Governor](https://blog.openzeppelin.com/governor-smart-contract/)
* [Build your DAO with OpenZeppelin Governor ft. ENS](https://www.youtube.com/watch?v=Lltt6j6Hmww)
{% endhint %}

\