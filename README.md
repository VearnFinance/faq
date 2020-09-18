---
title: faq.vearn.finance
---

# General

## Is it safe to invest money in vearn?
- Please do your own research and decide for yourself.

## Is vearn audited?
- Yes, you can find the list of audits [here](https://github.com/vearnfinance/audits)

<br>

# Feedback & Support
If you have questions about how to do anything, we can help you on:
- [Discord](https://discord.gg/????)
- [Telegram](https://t.me/vearnfinance)

<br>

But if you think something can be improved, or you found a bug, we want to squash it. Please post it here:
- [Github](https://github.com/vearnfinance) — create a new issue in the relevant repository
- [Forum](https://gov.vearn.finance/c/feedback/) — post in the feedback category
<br>

# Products

## [vearn.finance](https://vearn.finance/)
- Vearn.Finance hosts UIs for the **Earn**, **Zap**, **APR**, and **Vaults** products
### [Earn](https://vearn.finance/earn)
- Yield aggregator for lending platforms that rebalances for highest yield during contract interaction.
- Deposit DAI, USDC, USDT, TUSD, or sUSD and it will auto lend to the highest lending rate on these platforms [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/), or [Aave](https://app.aave.com/home) (Ddex and Fulcrum are currently disabled)
- Info on this can be found in the [Vearn Docs](https://docs.vearn.finance/vearn.finance/vearn)
- Profit switching lender to optimize lending yields (live)

### [Zaps](https://vearn.finance/zap)

#### What is a Zap?
- Zap allows users to convert supported tokens with just one contract interaction to reduce transaction costs
- Zaps were made by DefiZap which is now [Zapper.fi](https://zapper.fi) as a type of all in one defi routing service. 

#### Why use a Zap?
- "Zaps allow you get into a DeFi position in one transaction—it’s called zapping in." - [How to use Zaps guide](https://defitutorials.substack.com/p/how-to-use-defizap)
    - Note that this is an old article and [Zapper](https://zapper.fi) was formed as a result of DeFiSnap + DeFiZap coming together to create the ultimate hub for Decentralized Finance aka #DeFi. So some of the stuff in the article above is out of date, but you can still use Zaps on Zapper.fi

#### So what can I do with Zaps on yearn?
- With as zap you can take your DAI, for example, and get vCurve with it in one transaction. Normally, to turn DAI in to vCRV, you would have to go to earn, deposit DAI and receive vDAI, then go to [Curve.fi - Vearn pool](https://www.curve.fi/vearn/deposit) and deposit your vDAI and then you would get vCRV. This is alot to do so instead you can do it in one transaction!

#### That sounds awesome, what's the downside?
- Well, it does take a lot of gas and could be costly, even more so than doing it yourself manually, but if you have a big transaction and are in a rush it is a great method to get into a DeFi position or liquidity pool fast. 

### [APR](https://vearn.finance/apr)
#### What is this even for?
- It's a table that shows you the current APR for some yearn-supported tokens across lending platforms. The highest APR for each coin is the provider that Earn is lending these coins to at the moment.

### [Vaults](https://vearn.finance/vaults)

#### What is a Vault? How is it different from Earn?
- A Vault takes a more active approach than simply lending out coins for the highest APY. Via strategies it can farm coins such as CRV and then sell them, into the best DEX, to higher profits than simple lending. Yield is achieved by providing the asset for lending, LP, or farming strategies. These are opportunities that exist in defi. Vaults automate these processes and provide the highest (risk adjusted) yield available.
- Andre explains vaults here [Yearn Finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) and here [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) in these two blog posts.
- Simply put vaults can do this:
    - Provided liquidity can be any asset.
    - Use liquidity as collateral
        - Manage collateral at a safe level so you never default
    - Borrow stablecoins
    - Put the stablecoin to work on some farming
    - Any stablecoin earned above the debt (i.e. gains) are sold for the vault asset and returned to the vault.

#### Can't I just do all this myself though?
- Yes you could, but vaults help you save on gas, keep it at a good collateral/debt ratio so you dont default, and auto optimizes for highest yielding stablecoin strategies, even when you are sleeping.

#### I see ROI on the vaults page is the current APY?
- No. This is the historical average for that vault. Current APY / returns are not shown as the vaults is a beta product and being tested live. The returns are posted around once a day on [twitter](https://twitter.com/vearnfinance)

#### Risks
- While the assets deposited can't decrease, the debt of the vault can. If a strategy does not manage to outperform the debt, then a portion of the asset will be impermanently locked. If a strategy then outperforms the debt again, this asset will become unlocked.
    - There are mechanisms in the vaults to help this not to happen, but nothing is foolproof
- As of now, the Vaults have not been audited
- Smart contract risk with any contracts that the vaults interact with.

#### Currently Active Vaults
- v2 Vaults
    - aLINK
        - Why is the yield different for the two link vaults on [stats.finance/vearn](https://stats.finance/vearn)?
            - [aLINK has a 0.5% insurance fee](https://twitter.com/iearnfinance/status/1293772592004976641)
    - ChainLink
- v1 Vaults
    - Curve.fi/v (vCRV)
    - DAI
    - TUSD
    - USD Coin
        - You will receive vvUSDC. It's not the same token you will receive in Earn, even if everybody calls them the same.
    - USDT

#### If the current strategy for the vCRV vault is farming crv does it just get added to my balance when I withdrawal?
- No. The vault will farm CRV then sell it on the market automatically. When you withdrawal you will get more vCRV.

#### Why isn't vCRV worth $1, it's a stable coin right?
- No, vCRV is not worth $1 and no it is NOT a stablecoin. You can think of vCRV as an index of yield bearing stablecoins (vDAI+vUSDC+vUSDT+vTUSD) that also generates yield (trading fees from the Curve V pool) as well. Therefore the price of vCRV is always increasing.

#### If I unstake my vCRV from the vCRV vault does that then revert it back to the Curve V pool at Curve, or do I have to do something else like restake it there?
- When you withdraw your vCRV from the vault, you get back vCRV + plus interest accrued - fees, all in vCRV. Since it is the vCRV token you got back, it is already staked in Curve V pool making stablecoin swap fees. No need to do anything else with Curve, unless you want to stake it [here](https://dao.curve.fi/minter/gauges) to generate CRV.

#### I deposited into a vault what will I get out when I withdrawal?
- You will always withdrawal only the coin type you put in + the pool yield - fees.

#### Fees
- The fee on all vaults is 0.5% on withdrawals and a 5% fee whenever the harvest() function is called on the vaults which helps subsidize gas costs. The harvest function does the selling of the farmed asset on the market.
- Fees can be changed by governance.
- If you deposit and withdraw immediately, you will lose 0.5% of your principle

#### Yield
- We plan to make a dashboard in the future that will clearly show your current APY of all the positions you have open. Currently for the Vaults as they are still in beta we are not showing the APY live, but it is post on [twitter](https://twitter.com/vearnfinance) around once a day. You can roughly estimate the yield you are getting by looking at what the [current strategy](https://feel-the-vearn.vercel.app/) is farming and checking what its apy is.
- For example if vCRV vault is farming the CRV token, you can check what the yield is on [Curve's homepage](https://www.curve.fi/) for the V pool

### Vault Strategies

#### What is a Vault Strategy?
- Vearn's vault strategies are modular smart contracts for each vault that tells it what assets to borrow, which coins to farm, and where it should sell the farmed assets.

#### What are the current strategies?
- You can view the current strategies implemented at [feel-the-vearn](https://feel-the-vearn.vercel.app/)
- In the future we plan to make a dashboard to make the strategies and APY easy to understand.

#### Who is in control of the strategies?
- Andre writes them but the multi-sig decides if they will be implemented or not.

#### How can I make a strategy?
- For now you can post your strategy on the forum in the strategy section. Detailing what it should buy/sell/farm and what the current apy is. There will be a template to help you get started.

#### What is the process for getting my strategy onto yearn?
- Post it on the forum and if it gets approved it will be used in the vaults and you can get paid for it.

#### When does a strategy changes and who changes it? Is it automatic?
- For now Andre watches the markets and writes strategies that he and the multi-sig thinks are safe while giving the highest yield. They change them according to current yields on the market.

## [vtrade.finance](https://vtrade.finance/)
- Leveraged stable coin trades (testnet)

## [vliquidate.finance](https://vliquidate.finance/)
- 0 capital automated liquidations for Aave (testnet)

## [vswap.exchange](https://vswap.exchange/)
- Single sided automated market maker (testing in mainnet)

## [vborrow.finance](https://vborrow.finance/)
- Credit delegation vaults for smart contract to smart contract lending (testnet)

## [vinsure.finance](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896) 
- Prototype for a new kind of tokenized insurance (testnet)

<br>

# Tokens

## VFI
- Vearn Governance token
- Only 30,000 minted and already fully distributed
    - Governance can mint more, if proposal to do so passes.

## vTokens
- When you deposit into any yearn service your depost is wrapped and returned as a vToken representing the liquidity provided
- For example, if you deposit DAI in v.curve.fi you will receive vDAI in return
- Amounts of vToken and deposited token will differ since the vToken represents a share of a pool that is increasing in value
- If you deposit a vToken into another yearn service you will get a vvToken back


## vCRV
- LP token for vearn's V pool at Curve.fi
- Aka `vDAI+vUSDC+vUSDT+vTUSD`
- Interest earning token representing your share of the V pool composed of DAI, USDT, USDC, and TUSD 
- Via [How to provide liquidity on Curve.fi V pool?](https://guides.curve.fi/how-to-provide-liquidity-on-curve-fi-y-pool/)
    - Curve Finance V pool has long been one of the most popular pools on Curve Finance due to its strong returns from trading fees supplemented by iEarn which also lends your stable coin in the background to the lending protocol with the best lending rates out of Compound, dYdX and AAVE.


## vvCRV
- LP token for vearn's vCRV vVault
- aka `vvDAI+vUSDC+vUSDT+vTUSD`
- When you deposit vCRV into the vVault you receive vvCRV LP tokens
- earns interest via vCRV, fees and yield farming rewards via the vault strategy

<br>

# Communication
- [Forum](https://gov.vearn.finance/)
    - A lot of real-time discussion happens on the telegram and discord, but for a proposal to turn into a VIP (Vearn Improvement Proposal) it needs to be posted and discussed on the forum.
    - This is the main place token holders check for governance related issues.
- [Discord](https://discord.gg/????)
    - Including non-English channels
- [Telegram - Main Chat](https://t.me/vearnfinance)
- [Telegram - Trading/Social/Fork Chat](https://t.me/vearncommunity)
- Twitter
    - [vearn.finance - Official Twitter of Vearn](https://twitter.com/vearnfinance)
    - [Andre Cronje - Lead Developer of Yearn](https://twitter.com/AndreCronjeTech?s=20)

<br>

# Governance

## All about VIPs

### What is a VIP? Why do they matter?
- A VIP or Vearn Improvement Proposal is how features are added to the yearn ecosystem. Users start a proposal on the forum, discuss it, and gauge the sentiment of if the proposal will be accepted. If a lot of users agree with it, then it can be posted on-chain for everyone to vote on. 

### How many people need to vote to pass a VIP proposed on-chain?
- The quorum is 33%. Which means that 33% of the staked VFI needs to vote on a proposal for it to pass, or else it will fail. Also, it has to have at least 66% of the votes for yes.
- You can post your proposal on-chain first, but if people haven't talked about it, they probably won't vote for it.

### How do I make a proposal?
- The default template for proposals can be found on [Github](https://github.com/vearnfinance/VIPS/blob/master/vip-X.md) + on the [forum](https://gov.vearn.finance/) if you make a post under proposals or discussion it will auto-fill in the template as well. 

### Who can make a proposal?
- Anyone can post a proposal both on the forum and on-chain.

## Voting 

### How do I vote? 
- Stake your VFI and then you can cast your vote for VIPs that are on-chain on the [voting dashboard](https://vgov.finance/vote)

### Where can I view the VIPs?
- You can view them on the [voting dashboard](https://vgov.finance/vote) if you login to your web3 account or at [vips.yearn.finance](https://vips.yearn.finance/all-vip)

### Why should I stake? What is the APY (Annual Percentage Yield)?
- You should stake if you want to vote on VIPs and get rewards that are generated from the yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.

### What do I have to do to get rewards with my VFI?
- All you need to do is stake VFI at [vgov.finance/stake](https://vgov.finance/stake) and you will get rewards IF the treasury is at or above 500k usd. You can check the treasury address [here](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
- Note that if you stake you get rewards (as long as they are not going to the treasury), but you can only claim them within 3 days of voting. 

### Does staking my VFI matter for voting?
- Yes. You have to stake your VFI at [vgov.finance/stake](https://vgov.finance/stake) in the v2 tab under Governance V2 to have your votes count. As of now, you can vote without staking, but you will waste your gas and it won't count so make sure you have staked first if you want to vote.

### What if I want to take my VFI out before the end of the vote lock?
- You can't, sorry. The lock lasts 3 days after you last voted, until then you cannot unstake your tokens.

### I voted and I know the vote lock is 3 days, is there anywhere I can see exactly how long I have left till I can unstake my VFI?
- Yes! You can read the contract directly [vgov.finance staking contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) go to 28 votelock and input your eth address. This will give you the eth block number when you can unstake.

### What’s the difference between voting for a poll on the forum and an on-chain vote?
- A poll just gauges the sentiment of what the community is feeling on the proposal while a on-chain vote will be binding and will take effect if it passes.

### How long is my VFI tied up if I stake it?
- Your VFI is locked for 3 days after you vote

### Why can't I claim my staking rewards! 
- To claim your staking rewards you have to 1) be staked and 2) have voted. Within 3 days to be able to claim them. This will be fixed in an update soon.

## [vDAO](https://gov.vearn.finance/t/ydao-for-community-funding/2243) 

### What is its purpose?
- Used to fund value-added contributions to the yearn ecosystem.

### Who cares, how do I make money from this?
- You don't. This is solely for allocating funding for projects, and the VFI donated will be spent and your share value will be diluted.

### Who can join?
- Open for anyone to join with a base rate of 1 Share = 0.1 VFI

### How can I join?
- Go here to [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) sign in with your web3 account. Click New Proposal button in the top right. Click member. 
    - Title: your name/entity
    - Description: “Pledging X amount of VFI in exchange for Y Shares” (Please make this consistent with the amount being pledged at 0.1 VFI per share.)
    - Link: Link to you or your entity (Website, Twitter, Linkedin)
    - Shares Requested: The number of Shares being requested
    - Token Tribute: The amount of VFI being pledged (you will need to unlock VFI)
    - Loot: The number of shares being requested
    - After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [vDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)

### How can I request funding?
- The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

### I don't speak English, when will everything be translated?
- We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](https://discord.gg/94CmMdt).


<br>


# Community

## Is Sam or Mark in charge of vearn?
- Sam isn't in charge of vearn, nor is Mark, the VFI token holders make the decisions on what to build and governance decisions, but Sam is the lead developer of the vearn ecosystem.

## What does Sam do?
- Sam is the main developer building out the products that comprise the yearn ecosystem: Vearn, Vtrade, Vswap, Vliquidate, Vborrow. He is also currently in charge of running the Vaults and overseeing them. 

## What is the multisig and what do they do?
- The multi-signature address is explained in detail in this [thread](https://gov.vearn.finance/t/yfi-minting-ownership/155). Basically it is a 6 of 9 multi-signature account that has control over minting VFI, if a vote to mint tokens has passed successfully.

## Who are the 9 multisig signers?
- [Adam]
- [Mark]
- [nsldlr]
- [VRx93]
- [Other Person 5]
- [Other Person 6]
- [Other Person 7]
- [Other Person 8]
- [Other Person 9]

## What decisions can Sam make on his own?
- Sam can build out the Vearn ecosystem and come up with new products. Usually he posts his thoughts and ideas on the [forum](https://gov.vearn.finance/) for everyone to see.

## Does the multisig group tell him what to do?
- They are in close contact with one another, but Sam's priorities are decided by VFI token holders via VIPS.

## Who else writes code for vearn? Is there a team?
- Right now it's just Sam and nsldlr

## Does anyone get paid for working on yearn?
- As of this moment, not yet, but thanks to the passage of [VIP 36](https://yips.yearn.finance/VIPS/vip-36) and the creation of a community pool of funds that will be kept at 500k usd, we can now pay Sam for his work, fund audits, and pay for new devs to be hired along with anything else the the vearn ecosystem needs.

## How can I work for vearn?
- You can make a VIP to apply for funding from the 500k USD treasury directly or ask the vDAO for funding.

## Do you have any job openings?
- Yes, we do! We need all kinds of people to help make the vEarn ecosystem a thriving product and to give value to VFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Vearn, and how much you think you should be paid from the community pool. Also, you can go to the [vDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Vearn ecosystem.

## How to Participate
- You can participate in VFI by voting on VIPs that are active, discussing the VIPs yet to be proposed on-chain on the forums, and talking about VFI in the telegram and discord. If you know a second language help us translate the site and VIPs into that language. 

## Ongoing efforts to improve the Vearn ecosystem
- You can view the active VIPs [here](https://vips.vearn.finance/all-vip)

<br>

# User Interface
## Can I use the Vearn ecosystem dApps on my phone?
- Yes, you have to use the Metamask browser

<br>

# Related Projects
## [Curve](https://www.curve.fi/)
- Curve is an exchange liquidity pool on Ethereum (like [Uniswap](https://app.uniswap.org/#/)) designed for (1) extremely efficient stablecoin trading (2) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users (and smart contracts like 1inch, Paraswap, Totle and Dex.ag) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
- Curve [FAQ](https://www.curve.fi/rootfaq)

## [Aave](https://app.aave.com/home)
- Aave is an open source and non-custodial protocol enabling the creation of money markets. Users can earn interest on deposits and borrow assets.

<br>

# Resources

## Where can I learn more about vearn?
- [Learn Vearn](https://www.learnvearn.finance/)
- [Medium.com/vearn](https://medium.com/vearn)
- [vCosystem](https://vcosystem.info/)

## Lists of Smart Contracts
- https://gov.yearn.finance/t/yearn-contracts/1951
- https://etherscan.io/accounts/label/yearn-finance
    - sign-in required
- [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
- [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
- [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
- [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
- [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
- [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
- [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
- [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
- [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

## Registry of Tokens and Utility Contracts
- https://docs.yearn.finance/yearn.finance/yearn-1

## Vaults Detail Reference
- https://vaults.finance/

## Statistics

- [yieldfarming.info](https://yieldfarming.info/)
- [yVault ROI Calculator](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Yearn Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)


## Latest Yearn News
- [yearn.finance - Offical Twitter of Yearn](https://twitter.com/iearnfinance)
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance - Offical Blog](https://medium.com/iearn)

## Podcasts
- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers | Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

## Blogs
- [Yearn Finance - Offical Blog](https://medium.com/iearn)
    - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
    - [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
    - [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
    - [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
    - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
    - [YFI](https://medium.com/iearn/yfi-df84573db81)

## Logos
- Can be found in the discord under [#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
