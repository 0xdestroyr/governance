# KIP-27: Withdrawal of Rook's Bancor Position

```
kip: 27
title: Withdrawal of Rook’s Bancor Position
category: treasury investment
author: @starfire <starfire@rook.fi>
status: final
created: 2022-07-13
replaces: KIP-11
dependencies: none
```
## Proposal

Migrate Rook’s Bancor liquidity position from version 2 to version 3 and withdraw the tokens from Bancor.

## References

[1] [KIP-11](https://forum.rook.fi/t/kip-11-co-invest-rook-in-bancor-rook-bnt-pool/176) - proposal to co-invest 6,400 ROOK as liquidity on Bancor

[2] [Bancor Emergency Update](https://blog.bancor.network/market-conditions-update-june-19-2022-e5b857b39336) - suspension of impermanent loss protection

[3] [Rook Treasury Charter](https://forum.rook.fi/t/draft-kip-rook-dao-treasury-charter/399)

## Background

### Summary

KIP-11 initiated a deposit of 6,400 ROOK into a liquidity pool on Bancor v2 [1]. That position was motivated in part by Bancor’s promise of impermanent loss protection (ILP) on single-sided staked assets. Bancor has recently turned off this feature for an indefinite period of time due to the effects of an unexpected sell-off of BNT reward emissions. [2].

The current market environment requires diligent risk management and healthy liquidity for core Treasury assets such as ROOK. These recent developments at Bancor make it no longer wise to keep treasury assets there. This proposal seeks to address these risks by empowering the Official Team to initiate an immediate migration of Rook’s liquidity position on Bancor from v2 to v3, and then to withdraw our holdings of ROOK and return them to the Treasury.

Investment amount and type

Other (specify) - migration and removal of liquidity.

### Mission Alignment

The withdrawal of our single-sided liquidity position from Bancor is an effort to control our third-party risk exposure. The Treasury Charter states investments “must be managed in relation to each other in the aggregate including consideration of protocol risks, opportunity costs, lockup periods, etc.” [3] The current market conditions warrant conservative actions, and it is beneficial for the DAO to consolidate our liquidity and minimize overall risk.

### Expected benefits for Rook

Removing our single-sided liquidity position from Bancor will allow the DAO to consolidate its total liquidity and mitigate third-party risk for the DAO. The ROOK received from our Bancor position can be utilized in future initiatives.

## Analysis

### General

In December 2021, KIP-11 [2] empowered the DAO to co-invest 6,400 ROOK into the ROOK-BNT pool on Bancor. Bancor is known for its impermanent loss (IL) protection, but as of June 19th, 2022, they have temporarily suspended the service. Currently, liquidity providers can withdraw from Bancor without IL protection or wait until Bancor resumes the service. The timeframe for the suspension of Bancor’s IL protection is unknown. Given this uncertainty and the current market environment, it is prudent to proceed with the migration and withdrawal of our liquidity position. The migration from v2 to v3 is a required step in the Bancor withdrawal process. Removing our LP position on Bancor will allow the DAO to consolidate our third-party risk exposure and provide an opportunity to re-strategize how we deploy ROOK liquidity.

### Expected Return

The expected return is difficult to set in this case given the same lack of information that is motivating this proposal to withdraw. The potential upside is a full return of the 6,400 ROOK that we staked with Bancor, though that is impossible to estimate with the information provided.

### Potential Risks and Mitigation

* This proposal is intended to address the primary risk in Rook’s position with Bancor, which is impermanent loss risk. It is possible our position on Bancor has experienced significant IL. Bancor pairs all assets with BNT and the unexpected sell-off of BNT rewards resulted in impermanent loss across the Bancor system.
* There is a possibility that Bancor resumes the ILP service but playing a waiting game incurs opportunity cost. The DAO’s position may suffer more if left intact.
* Bancor has Rook limit orders on their platform and by pulling the DAO’s liquidity position it may damage the relationship.

## Implementation

### Execution

The Official Team will research and establish the timeframe for execution. Once established, the migration of assets from Bancor v2 to Bancor v3 and the subsequent removal of our liquidity position will be executed by the multi-sig holders as determined by the Official Team.

### Position Management

Once withdrawn, the ROOK will be returned to the DAO’s Treasury and will become part of its ongoing ROOK position.

### Monitoring and Reporting

Updates regarding the status and completion of this proposal will be provided during Treasury Tuesdays.

### Official Team and Disclosure

@DaddyMatty- Treasury Specialist

@starfire- Defi Analyst

@whatsthedeetz, Growth Lead

## Specification

* Initiate the migration and withdrawal of Rook’s total position on Bancor to 0x9a67f1940164d0318612b497e8e6038f902a00a4 (“Rook DAO Treasury”)
* Report back to DAO on completion of these transactions
