# KIP-33: Stake ALCX in exchange for gALCX

```
kip: 33
title: Stake ALCX in exchange for gALCX
author: <starfire@rook.fi>
status: sophon review
category: treasury investment
created: 2022-09-21
replaces: N/A
dependencies: N/A
```
## Proposal

Stake the DAO’s ALCX holdings in Alchemix’s native single sided staking pool.

## References

[1] [Rook Treasury](https://dune.com/0x_stubbs/Rook-Ecosystem)

[2] [Alchemix](https://alchemix.fi/)

[3] [Tokemak](https://www.tokemak.xyz/)

[4] [Tokemak C.o.R.E 4 ](https://app.tokemak.xyz/core)

[5] [Alchemix Contracts](https://alchemix-finance.gitbook.io/user-docs/contracts)

[6] [Alchemix Staking UI](https://alchemix.fi/farms)

[7] [Alchemix Audits and Bug Bounty](https://alchemix-finance.gitbook.io/user-docs/audits)

## Background

The Rook Treasury currently holds 5,355.28 ALCX tokens [1]. The DAO acquired these tokens through a strategic partnership with Alchemix [2], which was critical for Rook DAO to secure a Tokemak C.o.R.E. Reactor [3]. Because of this partnership, Rook DAO received 4.4 million votes in C.o.R.E. 4 [4] and has committed to holding the ALCX tokens for one year (“Commitment Period”). The partnership between Alchemix and Rook started with the acquisition of ALCX tokens on July 22, 2022, and the Commitment Period will end on July 22, 2023.

Note: All prices and estimated APYs referenced throughout were as of 9/21/2022

### Summary

Instead of allowing the DAO’s ALCX position to sit idle in the Treasury during the Commitment Period, the Delegated Team would like to stake these tokens in Alchemix’s native staking contract [5]. The staking of ALCX tokens turns the position into a yield-bearing asset called gALCX. gALCX is an auto-compounding governance token with an estimated APY of 18.4% [6], with rewards provided in ALCX tokens.

### Investment amount and type

This proposal is for a Yield Generating investment.

### Mission Alignment

Staking the DAO’s ALCX tokens will allow the Treasury to earn ALCX staking rewards. This action signals to the market our intent to honor our commitment and is in line with the DAO’s mission of supporting strategic partners.

### Expected benefits for Rook

This proposal allows the DAO to stake its idle ALCX holdings and receive Alchemix’s governance token gALCX. gALCX is an auto-compounding wrapped version of ALCX with an estimated APY of 18.4%[6]. In addition to earning the DAO passive interest, this proposal, if passed, will strengthen the relationship between Rook and Alchemix.

## Analysis

### Expected Return

The estimated expected return is 18.4% APY received in the form of ALCX tokens.

DAO holdings: 5,355.28 ALCX ( $109,461.92 @ Price of $20.44 per ALCX)

Estimated APY: 18.4% [6]

Expected accrual: ~985.3 ALCX over one year

NB: This assumes a Commitment Period of one year, and that the current APY of 18.4% holds constant over that period.

### Potential Risks and Mitigation

|Risk|Mitigation|
| --- | --- |
|Smart Contract Risk|Alchemix’s contracts received an audit from Runtime Verification and an ImmuneFi bug bounty program.|
|Execution Risk|The execution of this proposal will be overseen by the Delegated Team and performed by the Treasury multi-sig.|
|Opportunity Cost|Honoring the terms agreed upon with Alchemix will demonstrate the DAO's commitment to strategic partners.|

## Implementation

### Execution

The Delegated Team and the Treasury multi-sig will be responsible for the execution of this proposal.

### Position Management

As per the DAO’s agreement with Alchemix, our ALCX position will be held until the Commitment Period has ended on July 22, 2023. After the Commitment Period has passed, the DAO will be responsible for deciding how the position will be managed.

### Monitoring and Reporting

The Delegated Team will be responsible for communicating the execution of this proposal and will monitor its status. Periodic updates on the position will be shared with the DAO during Treasury Tuesdays. Additionally, this position will be included and monitored within our Treasury Dashboard [1].

### Delegated Team

@DaddyMatty - Treasury Specialist

@WhatstheDeetz - Growth Lead

@Starfire - Defi Analyst

## Specification

* Rook DAO Treasury (0x9a67f1940164d0318612b497e8e6038f902a00a4) to stake 5,355.28 ALCX tokens in the ALCX native staking contract (0x93dede06ae3b5590af1d4c111bc54c3f717e4b35)
* Report to the DAO upon completion of transaction.
* ALCX and gALCX positions will be included and monitored within the DAO’s Treasury dashboard [1].
* After the Commitment Period, the DAO will decide how the position is managed.
