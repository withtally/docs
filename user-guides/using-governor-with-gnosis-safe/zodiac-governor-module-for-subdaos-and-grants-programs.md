# Zodiac Governor Module for SubDAOs and grants programs

About Gnosis Zodiac

Zodiac is a collection of tools built according to an open standard by the team behind Gnosis Safe. The Zodiac open standard enables DAOs to act more like constellations, connecting protocols, platforms, and chains, no longer confined to monolithic designs. To learn more about the ideas behind Zodiac, visit the [Gnosis Guild blog](http://gnosisguild.mirror.xyz/) or read the [Introduction: Zodiac Standard](https://zodiac.wiki/index.php/Introduction:\_Zodiac\_Standard).\


### Introduction

The [Zodiac Governor module](https://zodiac.wiki/index.php/Category:Governor\_Module) facilitates the management and control of Gnosis Safes by a decentralized autonomous organization (DAO). With the Zodiac Governor module, a DAO can become a privileged member of the Safe, allowing it to manage signers and execute transactions. This document will guide you through the use case of creating SubDAOs and managing Grants Programs using the Zodiac Governor module.

### Features

#### 1. Privileged Management

Once integrated, the Governor DAO becomes a privileged member of the Safe. This privilege includes the ability to add or remove signers on the safe, giving the Governor DAO full control over membership.

#### 2. Transaction Control

The Governor DAO maintains control over the Safe's funds. It can spend money and execute transactions, allowing the parent DAO to maintain executive authority over its subsidiary structures.

#### 3. Safety Measures

The Zodiac Governor module includes Delay modules which can require a waiting period for the multi-sig signers. This delay provides the DAO with a veto period to block funding requests that may be contrary to the DAO's goals or may pose legitimacy concerns.

### Benefits

This design opens up several unique opportunities for DAO management:

* It allows for the creation of **SubDAOs**, where a committee of experts act as signers on the multisig. Even while they operate independently, the parent DAO retains ultimate authority.
* It is an ideal mechanism for delegating funds to **Grants programs**. The DAO maintains authority over both the funds and the Grants program administrators, ensuring a chain of responsibility.
* The mechanism helps in avoiding **centralization dangers**, where Grants program administrators could potentially misuse funds without any on-chain recourse.
* It offers a solution to **political disagreements** among signers, preventing funds loss due to indecision or conflict.
* It serves as a vital component in the operation of **decentralized Grants programs**.

### Fund Control Mechanism

Instead of directly transferring funds to the Gnosis safe, the DAO gives the Gnosis safe a spend approval of a certain amount. For instance, rather than transferring $1 million from the treasury, the DAO could give the Gnosis safe a Spend Approval of $1 million. This ensures that the funds only leave the DAO when the multi-sig signers create a transaction. As a result, the funds always remain under the control of the DAO.

### How to Create a SubDAO

Creating a SubDAO for grants oversight or multisig management is straightforward.&#x20;

Use the [Zodiac Governor Module no-code tool](https://zodiac.wiki/index.php/Governor\_Module:\_Operator\_Tutorial) to initiate the creation of a Grants Oversight DAO, and follow the steps below:

1. Select your existing parent DAO token during the creation flow.
2. Create a new Governor for the SubDAO with your desired parameters for oversight. You can use the same parameters as the parent DAO or opt for different ones to match your specific needs.

The Safe App will automatically create your Governor SubDAO and add it to your multisig.

Finally, a couple of steps are needed to get your new SubDAO fully represented on Tally.

1. Copy the contract address of the Governor that was created by the Zodiac Governor Module no-code tool and [add it directly to Tally](../../knowledge-base/managing-a-dao/).&#x20;
2. [Link the contract address](../../knowledge-base/managing-a-dao/gnosis-safe.md) of the multisig that was created via the Zodiac Governor Module to your Parent DAO, making it easily visible from the parent DAO on Tally.

### Conclusion

The Zodiac Governor module provides an efficient, secure, and decentralized way to manage SubDAOs and Grants Programs. Its unique features and benefits make it an ideal tool for any DAO aiming to retain control while fostering growth and collaboration.