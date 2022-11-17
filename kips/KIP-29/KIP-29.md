## KIP-29: Management of Non-Core Treasury Assets

```
kip: 29
title: Management of Non-Core Treasury Assets
category: delegation of powers
author: @starfire <starfire@rook.fi>
status: final
created: 2022-07-13
replaces: none
dependencies: KIP-5
```
# Proposal

Establish and empower a Delegated Team with discretion to manage non-core assets under the amount of $100,000.

# References

[1] [Rook Treasury holdings](https://dune.com/0x_stubbs/Rook-Ecosystem)
[2] [Treasury Management Framework](https://docs.google.com/document/d/1fl8GPRYZ9H_SEdGnwowH_ZiezoZ4HoOa/edit#)
[3] [KIP 23](https://forum.rook.fi/t/kip-23-establish-a-discretionary-investment-limit/347/9)
[4] [KIP 5](https://forum.rook.fi/t/kip-5-acquire-cvx-position/174/3)
[5] [Rook Treasury Charter](https://forum.rook.fi/t/kip-28-rook-dao-treasury-charter/399))

# Background

## Summary

Management of non-core Treasury assets can be time-consuming and does not directly contribute to the mission of Rook DAO. Delegating this responsibility to a Delegated Team will allow our governance process to focus on more critical proposals. This proposal aims to provide discretion to the Delegated Team to manage non-core asset positions under the amount of $100,000. Powers granted to the Delegated Team include unstaking, claiming rewards, and swapping assets whose total value in USD is below the $100,000 cap. In the event the team decides to swap or liquidate a non-core asset, the resulting funds are required to be core assets.

The table below shows current non-core asset holdings in the Rook Treasury as of July 13, 2022 [1]. Of these, the ALCX position is part of a strategic partnership.

|Asset|Units|Dollar Amount|
| --- | --- | --- |
|vlCVX|372,814.74|$2,311,451.38|
|cvxCRV|17,204.39|$16,970.73|
|LDO|7,946.87|$6,708.18|
|FXS|3,415.29|$16,222.63|
|ALCX|5,355.28|$115,781.23|
|RAI|201.38|$594.06|

## Nature of Powers to be Delegated

This proposal gives the Delegated Team discretion to manage non-core Treasury assets under the amount of $100,000. This proposal defines non-core assets as tokens that DO NOT meet one of the following criteria:

* Current Treasury core asset holdings:
  * ROOK
  * ETH
  * WETH
  * renBTC
  * DAI
  * USDC
* Tokens received from strategic partnerships [2].

The Delegated Team will have the discretion to swap non-core asset positions of under $100,000 into one or more of the core assets. Non-core asset positions that carry a value above the $100,000 cap will be subject to the full governance process.

This proposal delegates discretionary management powers that are unrelated to the powers and limits ratified by KIP 23 [3].

In addition, this proposal provides a more general framework for revenue generated from KIP-5 [4]. It is intended to capture most if not all bribes received from our vlCVX position, the bulk of which are paid to Rook DAO in unrelated tokens in amounts well below the $100,000 limit established in this proposal. However, when the bribe revenue exceeds the $100,000 threshold or is the result of a strategic partnership, the management of those assets will be subject to the standard governance process.

## Term of Delegation

This proposal is intended to be in effect for as long as the Rook Treasury includes non-core assets or until a future proposal supersedes the powers granted in this document.

## Mission Alignment and Rationale

Non-core Treasury assets, that are not related to strategic investments, do not contribute to the mission of Rook Protocol. These assets can be the result of airdrops, Convex bribes earned as a result of KIP-5 [4], or token rewards from other activities. All of the pieces that make up Rook DAO should be aligned with the core values of Rook’s mission, including the Treasury. The goal of the Rook Treasury is to ensure that operations of the DAO are ongoing, sustainable, and resilient to market volatility. As such, the main focus of the Treasury Charter is to ensure that decisions are being made to support the contributors, capture market share and support key infrastructure of the DAO [5].

The reasoning for delegating this responsibility is to help eliminate noise on our governance forum. Proposals relating to non-core assets are not directly aligned with the mission of Rook DAO and have the potential to detract from more critical governance functions.

## Expected Benefits for Rook

Allowing for the creation of a Delegated Team, whose focus is to rebalance non-core assets under the amount of $100,000, will give the DAO increased flexibility. As it currently stands, a decision regarding our non-core assets would be required to go through our governance process. Subjecting decisions, about non-core assets, to the full governance process will be time consuming and can detract from critical governance proposals.

Other Potential Benefits

* This proposal allows for timely decisions to be made that take advantage of optimal pricing. (ex. airdrops)
* Contributes to the formalization of our overall treasury management framework

## Potential Risks and Mitigation

Execution risk in making these swaps will be mitigated through the use of Rook limit orders. There is a minor “risk” that the Treasury will miss the benefits of any appreciation in these non-core positions, but these positions are too small to have a material impact and seeking such appreciation is less critical than maintaining strong positions in core, known assets.

# Implementation

## Execution and Position Management

The discretionary sale of the non-core assets under the threshold will be the responsibility of the Delegated Team, with the execution being performed by the multi-sig signers. Non-core assets that are sold as a result of this proposal must be converted into one or more of the core assets listed above.

## Monitoring and Reporting

The Delegated Team will be responsible for communicating their decisions to the DAO. Updates, from the Delegated Team, will be communicated at Treasury Tuesdays with an accompanying written summary of the transaction.

## Delegated Team

@DaddyMatty - Treasury Specialist
@Stubbs - Data Analyst
@Starfire - DeFi analyst

# Specification

* Empower Delegated Team to manage non-core Treasury assets of less than $100,000 by swapping them into core assets, at the Team’s discretion.
