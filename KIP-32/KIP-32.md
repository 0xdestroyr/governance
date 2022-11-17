# KIP-32: Voting Participation and Weights

```
kip: 32
title: Voting Participation and Weights
authors: @JasonW and @Wes2
status: final (adopted)
category: governance process
created: 2022-08-24
replaces: 
dependencies: KIP-0, KIP-8
```
**Proposal**

Establish and ratify voting rights and tunable voting weights for holders and stakers of ROOK across multiple platforms to use in Rook governance votes. 

**References** 

[1] [Rook Snapshot page](https://snapshot.org/#/rook.eth)
[2] [Bancor bnROOK address](https://etherscan.io/address/0xE4BeCD393eD7cfDEEf9F513A3fE6BbAAc923caA9)
[3] [Sushiswap AMM ROOK address](https://etherscan.io/address/0xf13eef1c6485348b9c9fa0d5df2d89accc5b0147)
[4] [Uniswap v2 ROOK address](https://etherscan.io/address/0x70ec2fa6eccf4010eaf572d1c1a7bcbc72dec983)
[5] [xROOK address](https://etherscan.io/address/0x8aC32F0a635a0896a8428A9c31fBf1AB06ecf489)
[6] [Bancor v3 voting strategy for Snapshot](https://github.com/snapshot-labs/snapshot-strategies/tree/master/src/strategies/bancor-pool-token-underlying-balance) 
[7] [SushiSwap voting strategy for Snapshot](https://github.com/snapshot-labs/snapshot-strategies/tree/master/src/strategies/sushiswap) 
[8] [Uniswap voting strategy for Snapshot](https://github.com/snapshot-labs/snapshot-strategies/tree/master/src/strategies/uniswap)
[9] [xROOK voting strategy for Snapshot](https://github.com/snapshot-labs/snapshot-strategies/tree/master/src/strategies/xrook-balance-of-underlying-weighted)
[10] [xROOK staking API](https://api.rook.fi/api/v1/staking)

**Background** 

Rook’s governance process uses token voting on Snapshot[1]. That process has to date operated without stated rules around which holders of ROOK can vote and which can’t. In practice, only those holding ROOK in Snapshot-compatible wallets were able to vote their ROOK until recently, when voting was expanded to include those holding xROOK (ROOK staked on the protocol’s native staking contract). This expansion gave each xROOK the equivalent of 1 ROOK of voting power, regardless of the typically larger economic weight accorded to each xROOK within the staking contract. The rationale for this change was to leave any changes to the voting weight of xROOK to be tuned through the governance process. 

More recently, Rook’s developers have identified smart contract additions available within Snapshot that - if used - could expand voting to include ROOK that are staked on Uniswap, Sushi and Bancor. Use of these contracts has been discussed in Governance Workshop but have yet to be ratified through Rook governance. 

**Summary**

This document proposes to accomplish two things: 

- Establish and ratify a set of formats for ROOK holdings to be formally included in Rook governance votes
- Establish and ratify an initial (and tunable) set of voting weights for each format

This proposal envisions subsequent amendments (via Rook governance) as the voting weights and number of holding formats change with DAO member preferences. 

**Proposal Detail**

This document proposes to expand eligibility for voting to ROOK tokens staked in liquidity pools on the following platforms: 

- Bancor v3 [3]
- Sushiswap AMM [4]
- Uniswap v2 [5]
- Rook native staking (xROOK) [6]

Doing so will require identifying (or, if necessary, writing) the appropriate voting contract or (in Snapshot’s terms) “strategy” and then implementing those strategies in Rook’s Snapshot account. Snapshot currently offers strategies for each of the three external liquidity platforms where ROOK are staked: Bancor v3 [6], SushiSwap [7] and Uniswap v2 [8]. *NB: Cited strategies for SushiSwap and Uniswap are indicative only, and may change.* 

The dev team have also developed a Snapshot strategy for reweighting the voting power of xROOK [9]. That strategy includes an adjustable parameter for tuning the voting power given to each xROOK using a voting coefficient that in turn multiplies the staking coefficient, or the number of ROOK equivalents represented by each xROOK in the staking contract. This design makes it possible to tune the voting and staking weights of xROOK separately. 

This document proposes to set the voting coefficient for xROOK to 1, meaning that each xROOK would receive voting power equal to the number of ROOK equivalents established by the staking coefficient. The staking coefficient is defined by the “xRookUnderlyingConversion” parameter in the ROOK staking contract [10]. That weight is 1.058721221017144 as of 2022-08-24, but is not fixed at that level. 

Once enacted, these changes will result in the following voting participation and power for holders of ROOK in various forms: 

| Token | Holding format | Current Voting Weight | Proposed Voting Weight |
| --- | --- | --- | --- |
| ROOK | Web-based wallet | 1 | 1 |
| xROOK | Staked with Rook | 1 | xROOK staking weight |
| ROOK | Staked on Uniswap v2 | 0 | 1 |
| ROOK | Staked on SushiSwap AMM  | 0 | 1 |
| bnROOK | Staked on Bancor v3 | 0 | 1 |

**Mission alignment and rationale**

The motivation for this document is to bring practice and codified process into alignment around an expanded and governance-defined set of voting rights for holders of ROOK across major formats. This proposal is aligned with the DAO’s values of progressive decentralization in its potential to further decentralize voting concentration by bringing more tokenholders into the voting process. It also gives a voice in the governance process to those providing liquidity for ROOK on important DeFi platforms. 

**Specification**

- Deploy the following strategies on Rook’s Snapshot page:
    - Deploy the *xrook-balance-of-underlying-weighted* [9] strategy, with ”weight” parameter set to 1
    - Deploy the *bancor-pool-token-underlying-balance* [6] strategy
    - Identify and deploy the most appropriate SushiSwap strategy
    - Identify and deploy the most appropriate Uniswap strategy
- Document strategies used in Rook's Governance repository in Github 
- Report back to the DAO when these strategies have been implemented
- Use these strategies and weights for all votes until changed by a subsequent KIP
