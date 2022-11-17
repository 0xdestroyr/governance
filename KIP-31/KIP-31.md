# KIP-31: Convert renBTC to WBTC

```
kip: 31
title: Convert renBTC to WBTC
author: @DaddyMatty
status: final (adopted)
category: treasury investment
created: 2022-08-26
replaces: 
dependencies: 
```

## Proposal

Exchange renBTC held in the DAO Treasury for an equivalent amount of WBTC.

## **References**

[1] [Treasury Holdings](https://etherscan.io/address/0x9a67f1940164d0318612b497e8e6038f902a00a4) (0x9a67f1940164d0318612b497e8e6038f902a00a4)
[2] [renBTC Data](https://coinmarketcap.com/currencies/renbtc/)
[3] [WBTC Data](https://coinmarketcap.com/currencies/wrapped-bitcoin/)
[4] [KIP-19](https://forum.rook.fi/t/kip-19-sunset-the-liquidity-pools-product/331/10) 

## Background

### Summary

This is a treasury maintenance risk-management action motivated by a desire to minimize all potential risk to treasury funds, particularly for non-productive reserve assets held for long periods of time, such as renBTC.

This proposal would exchange the renBTC held in the DAO Treasury (0x9a67f1940164d0318612b497e8e6038f902a00a4) for an equivalent amount of WBTC, which carries less complexity and is a more liquid asset suitable for long-term reserve holdings.

### Investment amount and type

This document proposes that the approximately 40.672 renBTC held in the Rook DAO Treasury **[1]** be exchanged for an equivalent amount of WBTC.

## Analysis and Rationale

In regular use, renBTC and WBTC are nearly equivalent in that they should entitle the bearer to redeem BTC 1:1. However there are a number of reasons for the DAO to prefer to keep its BTC holdings in WBTC at this time. 

As of August 26, 2022, WBTC is far more liquid, with a circulating supply of 247,760 WBTC, more than 73 times higher than the total supply of 3,394 renBTC. WBTC also experiences far greater daily trading volumes, more than $250,000,000, 31 times higher than the $8,000,000 of volume traded in renBTC [**2,3**]. 

Recent regulatory developments have made it clear that the potential exists for eager regulators to impose controls that could render the DAO unable to recover the underlying BTC from a wrapped asset. In such a scenario, liquidity on a secondary market would be an important factor for recovering the value of the wrapped asset for the DAO. Given this, we cannot ignore the vast disparity in liquidity between these two derivatives of BTC.

The DAO Treasury originally held renBTC in order to seed the renBTC liquidity pool, which helped incentivize renBTC liquidity and volume by enabling zero-cost flash loans with the asset. This was done in line with our longstanding partnership with the Ren protocol, a partnership that continues today. 

However with the sunsetting of the Rook liquidity pools **[4]**, and the removal of DAO Treasury renBTC liquidity from them **[4],** our thoughts must turn towards long-term risk management as the primary measure of any reserve asset.

### Expected benefits for Rook

The expected benefits of this proposal are as follows:

- Increased liquidity in the event the DAO chooses, or is driven by necessity, to liquidate the asset.

## Implementation

### Execution

See the “Specification” section for execution details. 

### Monitoring and Reporting

The Treasury will continue to monitor the position as part of its ongoing monitoring of the DAO’s portfolio. 

## Specification

Specific steps to be taken, in bullet point form

- DAO Treasury (0x9a67f1940164d0318612b497e8e6038f902a00a4) to send the approximately 40.672 renBTC to execution wallet (0xa41164009fa1021ac3cff34813e461ca445d0712) controlled by CTO to execute swap
- Exchange the approximately 40.672 renBTC in the DAO Treasury for an equivalent amount of WBTC at prevailing market prices using the Rook Protocol ([https://app.rook.fi/en/trade](https://app.rook.fi/en/trade))
- Return funds from execution wallet (9fa1021ac3cff34813e461ca445d0712) to DAO Treasury (0x9a67f1940164d0318612b497e8e6038f902a00a4)
- Rook rewards generated from the swap will be claimed and transferred to the Treasury at a later point
- Report back to DAO the results of the swap
