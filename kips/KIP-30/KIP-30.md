## KIP-30: Temporarily Empower and Fund a Strategy Testing Multisig
```
kip: 30
title: Temporarily Empower and Fund a Strategy Testing Multisig
category: delegation of powers
authors: @DaddyMatty <[matt@rook.fi](mailto:matt@rook.fi)>, @Pai-Sho <[paisho@rook.fi](mailto:paisho@rook.fi)>, @zakhtar ([zakhtar@rook.fi](mailto:zakhtar@rook.fi)>
status: final
created: 2022-07-07
replaces: N/A
dependencies: N/A
```
## Proposal

Establish and fund a new multisig wallet for the purposes of testing passive strategies using the Rook Protocol, and empower a Delegated Team to create and test the strategies.

## References

[1] [Rook Protocol dashboard](https://dune.com/0x_stubbs/ROOK-Protocol)
[2] [Rook Treasury holdings](https://dune.com/0x_stubbs/Rook-Ecosystem)
[3] [Stablecoin Research ](https://deathereum.substack.com/p/chasing-stability-a-stablecoin-deepdive)

## Background

### Summary

The Rook Protocol has seen close to $300m in total volume in the short period of time since its launch in April 2022. While this volume has created a wealth of information and metrics (see Dune dashboard **[1]**) about the activity occurring within the Rook Protocol, it has been driven mainly by external parties whose strategies we as a DAO have no control over. All internal testing has been mainly geared towards assessing the soundness of the protocol rather than to investigate profitable strategies. So that we may better understand the potential for such strategies, we must put in the work of exploring and capturing their potential ourselves, so that we can offer them to others who follow.

This proposal seeks to establish a sandbox with which we can implement and monitor the profitability of passive trading strategies using the Rook Protocol. Specifically, this KIP proposes to:

1. Establish a new delegated 2 of 3 multisig (the "Strategy Testing Wallet").
2. Fund the wallet using assets from the DAO Treasury (the "Budgeted Funds").
3. Empower a working group of key contributors (the "Delegated Team") to use the Strategy Testing Wallet to develop and test novel strategies using the Rook Protocol.

### Nature of powers to be delegated

This proposal delegates power over the Strategy Testing Wallet controlling the Budgeted Funds to the Delegated Team. Additionally, this proposal empowers the Delegated Team to swap exclusively between Approved Assets at their discretion, using the Rook Protocol. Approved Assets consist of:

* USDC
* DAI
* USDT
* FRAX

These assets will be used to execute 1:1 limit orders between approved stablecoins on the Rook Protocol. This ensures that the number of units of each asset will be preserved, with the only risk being the devaluation of one or more due to loss of peg. We will monitor the frequency and profitability of each swap, the amount of ROOK that each yields, and investigate the potential for offering the strategy as a product.

### Term of delegation

The powers as defined above will stay in effect until 180 days post-ratification of this proposal, at which point funds will be returned to the treasury multisig. The results of the study will also be published with a comprehensive, data-driven report.

### Budget

To effectively gather sufficient data, a base amount of each stablecoin is needed. Additionally, 1 ETH is being requested to accommodate gas fees for fund transfers and rewards claiming. More specifically, this document proposes the transfer of the following amounts (“Budgeted Funds”):

|Asset|Amount (Units)|
| --- | --- |
|USDC|150,000|
|DAI|150,000|
|USDT|150,000|
|FRAX|150,000|
|ETH|1|
|Total Funds Requested|600,000$ + 1 ETH|

### Mission Alignment and Rationale

Our goal here at Rook is to be on the cutting edge of blockchain technology and DeFi thought leadership. To accomplish this goal, we must constantly be evolving our product suite, capabilities, and mindshare in the ecosystem. For this ongoing evolution to occur, we must gather as much data about our current and future strengths and weaknesses from a product standpoint; data is power.

Internally, a need has been identified to analyze the effects of HidingBook-native stablecoin liquidity on order execution and routing efficiency for users and Keepers. By ratifying this proposal, we enable ourselves to rapidly and efficiently capture this data and utilize it to more effectively evolve the Rook Protocol.

### Expected benefits for Rook

The expected benefits derived from this proposal are as follows:

* Enables collection of data that will assist Rook Labs in:
  * Developing new trading strategies to increase future revenues
  * Gaining insight into the effects of native HidingBook stablecoin liquidity on Keeper routing opportunities and order execution efficiency
  * Understanding the viability of future products we can offer to integration partners and other external parties
  * Developing data-driven marketing content displaying the power of the Rook Protocol
  * Identifying potential areas of improvement within the Rook Protocol

### Potential risks and mitigation

As with all investments, the benefits earned come with numerous risks that are both financial and non-financial in nature. These risks and related mitigations should be assessed by the DAO in conjunction with the benefits stated above and would include:

|Risk|Related Mitigation|
| --- | --- |
|Smart Contract Risk|All testing will be done exclusively through the Rook Protocol which has been thoroughly audited and battle-tested.|
|Stablecoin Risk|All 4 of the proposed stablecoin assets are relatively low-risk in terms of depegging. See stablecoin research **[3]**|
|Loss of funds via fraud or mismanagement|Funds will be held in a delegated 2-of-3 multisig controlled by the Delegated Team, who are all full-time contributors to the DAO.|
|Fragmentation of liquidity|The budgeted amount requested is relatively immaterial (~1% of Treasury holdings **[2]** as of 2022-07-07). Because the Delegated Team consists of full-time contributors to the DAO, these funds will be readily available to send back to the DAO Treasury when needed.|
|Opportunity cost|The insight derived from the availability of new data with respect to new trading strategies, marketing potential, and general improvement of the protocol is expected to far outweigh the potential yield gained through depositing these assets into an external protocol.|

### Delegated Team

The full-time contributors to be delegated the powers in this proposal are:

|Contributor|Signing Address|
| --- | --- |
|@Deetz|0x722f531740937fc21A2FaC7648670C7f2872A1c7|
|@Pai-Sho|0xDAAf6D0ab259053Bb601eeE69880F30C7d8e5853|
|@Zakhtar|0x3C3ca4E5AbF0C1Bec701375ff31342d90D8C435E|

### Oversight and Recourse

To ensure the proper stewardship of the funds managed by the Delegated Team, the Treasury Team will monitor the utilization of these funds and report back to the DAO on at least a monthly basis. Additionally, the wallet’s address will be made public so that any interested parties can assess the activity in real time. A public dashboard along with a Hiding Book viewer will be made available by the Treasury Team and the Protocol Team to better assist interested parties in evaluating the metrics and trading history in real-time.

Lastly, the Delegated Team will strive to provide reasonable insight into the nature and results of testing being performed as it becomes available.

## Specification

* Create a new 2-of-3 multisig Strategy Testing Wallet and publicly announce the address of the wallet
* Add the Delegated Team as signers of the Strategy Testing Wallet multisig
* Empower the Treasury multisig (0x9a67f1940164d0318612b497e8e6038f902a00a4) to deploy the budgeted funds as defined above to the Strategy Testing Wallet within 30 days of ratification of this proposal
* Delegated Team begins testing Approved Assets within Rook Protocol at their discretion
