# KIP-35: Streamlined tokenomics

```
kip: 35
title: Streamlined tokenomics
author: @hazard
status: sophon review
category: protocol 
created: 2022-10-22
replaces: N/A
dependencies: N/A
```
## Proposal

Align Rook’s tokenomics to reflect user and partner preferences by: 

- Replacing ROOK with wETH for bids and rebates, and
- Streamlining the bid distribution to 90% user and 10% to the DAO Treasury.

## Background and Rationale

Orderflow through the Rook Coordinator is by far the most important metric for the long-term sustainability of our ecosystem. Until Rook technology is processing a substantial volume of orderflow, we cannot call the project or its products a success in any way. The orderflow landscape is evolving rapidly, and the next 6-12 months will be crucial. 

For a system like Rook, the technology must fit the exact needs and specifications of its integration partners. Today, it does not. For nearly everyone we talk to, our tokenomics presents a major barrier to integration. Potential partners are uncomfortable with ROOK as the bid token for a neutral auction, and they unanimously do **not** want to receive MEV rebates in ROOK, a sentiment shared by average users. They also do not like the distribution of the bid and the way it is split between so many different parties.

The key to our mission is orderflow, and so we must update our tokenomics to reflect the new information we have gathered from these potential partners, which is today limiting any impact we can have.

## Proposal Detail

### Bid wETH, not ROOK

We talk to users, searchers, researchers, and potential integration partners constantly, from the largest of the large firms down to individual user stories. They are all unanimous: they do **not** want us to bid ROOK, and they do **not** want to receive MEV rebates in ROOK.

We hear many variations of the same sets of concerns, ranging from worries about neutrality, not wanting to appear biased to customers, not wanting them or their users to handle a strange token, not wanting to hold ROOK in their inventory, and also not wanting to liquidate the ROOK, and so on. But using ROOK for bids or rebates is always a no-go for them, and the larger the amount of orderflow they handle, the more likely it is that the preferential use of ROOK in the system will absolutely kill the integration.

What they want us to do is to bid wETH, and what they want to receive is wETH or ETH. When we ask potential integration partners whether they would feel more comfortable if the token were wETH or ETH, their eyes light up. They smile again. “Oh, that would be awesome!” they say. This happens every. single. time. If we want to succeed, moving to wETH or ETH is a required change, full stop.

![Untitled](https://github.com/rookprotocol/kips/blob/master/KIP-35/kip35image.png)

From a technical perspective, this is not a difficult change to make. The Coordinator is capable of handling any ERC20 as the bid token and redistributing the same as the MEV rebate. As part of this proposal, we have prepared upgrades to the relevant smart contracts that would not only allow the use of wETH for searchers to stake and bid with, but would allow users to claim either wETH or ETH, as desired. The work is already done and can be made live very rapidly.

### Set the bid distribution to 90% user, 10% DAO

The other major concern they have is our complicated bid distribution, which carves some out for burning, some for the DAO treasury, some for stakers, and some for the user. There may also be some for the partner if they program part of the user distribution as a fee. The searcher is also taking some. This is all just far more complicated than it needs to be, and turns every conversation into a math exercise. We got this wrong — simplicity is best and always was.

We care about orderflow and helping users get better transactions. Today, this complex tokenomics is not helping anybody. We need to walk before we can run, and that means streamlining this tokenomics into something clean and easy to understand.

The proposal is for a simple 90/10 split between the user and the DAO Treasury. Why? The other categories, burn and user staking, have been completely ineffective and would continue to be.

- Even under optimistic models, the total ROOK supply burned would be very minimal, especially if a “flywheel” was in full effect. As the value of a ROOK token increased, the effect of the burn would vanish.
- The current APR for user staking is less than half of the deposit fee - there is no incentive to stake ROOK as a user and even after we begin to drive orderflow, this would not be certain to change. Market forces would compress the amount of ROOK returned to the user through staking. And the incentives do not work out. If the value of a ROOK token increased, the APR would decrease, leading stakers to unstake and liquidate. This would decrease the value of a ROOK token, leading APR to increase, leading others to buy and stake. Rinse and repeat. A volume-pegged MEV stablecoin.

Neither of these mechanisms drive orderflow through the Coordinator in any way. Neither of them contribute to increasing volume, and in both the added complexity and reduction of user reward, they in fact stand in the way of adoption. They should be removed from the bid distribution.

### Where does that leave us?

If we make these changes, it allows us to make a very stark and simple proposition to users and potential partners: “Rook is a neutral system that runs on ETH. Use Rook, and you will automatically earn ETH. The system will always return 90% of the MEV to you.” This is a powerful message that we already know excites every user and partner we speak to.

The ROOK token will remain a crucial part of the DAO’s infrastructure, and its tokenomics will continue to evolve. As the governance token of the Rook DAO, it will grant staked tokenholders the ability to vote on key matters and decisions of the DAO, and on all proposals, such as this one. This is a solid starting point from which we can explore some of the new ideas and directions we have in mind for the token and its role in the ecosystem. In the short-term, orderflow is the most important thing, bar none.

## Specification

- Following ratification, deploy an updated Coordinator smart contract allow wETH staking and bidding, rather than ROOK.
- Update all relevant associated software and documentation to reflect the change.
