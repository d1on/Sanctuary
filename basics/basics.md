# FAQ

## Why do we need Sanctuary in the first place?

Dollar-pegged stablecoins have become an essential part of crypto due to their
lack of volatility as compared to tokens such as Bitcoin and Ether. Users are
comfortable with transacting using stablecoins knowing that they hold the same
amount of purchasing power today vs. tomorrow. But this is a fallacy. The dollar
is controlled by the US government and the Federal Reserve. This means a
depreciation of dollar also means a depreciation of these stablecoins.

Sanctuary aims to solve this by creating a free-floating reserve currency, SANCT,
that is backed by a basket of assets. By focusing on supply growth rather than price
appreciation, Sanctuary hopes that SANCT can function as a currency that is able
to hold its purchasing power regardless of market volatility.

## Is SANCT a stable coin?

No, SANCT is not a stable coin. Rather, SANCT aspires to become an algorithmic reserve currency backed by other decentralized assets. Similar to the idea of the gold standard, SANCT provides free floating value its users can always fall back on, simply because of the fractional treasury reserves SANCT draws its intrinsic value from.

## SANCT is backed, not pegged.

Each SANCT is backed by 1 DAI, not pegged to it. Because the treasury backs every SANCT with at least 1 DAI, the protocol would buy back and burn SANCT when it trades below 1 DAI. This has the effect of pushing SANCT price back up to 1 DAI. SANCT could always trade above 1 DAI because there is no upper limit imposed by the protocol. Think pegged == 1, while backed &gt;= 1.

You might say that the SANCT floor price or intrinsic value is 1 DAI. We believe that the actual price will always be 1 DAI + premium, but in the end that is up to the market to decide.

## How does it work?

At a high level, Sanctuary consists of its protocol managed treasury, protocol owned liquidity \([POL](../references/glossary.md#pol)\), bond mechanism, and staking rewards that are designed to control supply expansion.

Bond sales generate profit for the protocol, and the treasury uses the profit to mint SANCT and distribute them to stakers. With [liquidity bonds](../references/glossary.md#liquidity-bonds), the protocol is able to accumulate its own liquidity. Check out the entry below on [the importance of POL](basics.md#why-is-pol-important).

## Why is PCV important?

As the protocol controls the funds in its treasury, SANCT can only be minted or burned by the protocol. This also guarantees that the protocol can always back 1 SANCT with 1 DAI. You can easily define the risk of your investment because you can be confident that the protocol will indefinitely buy SANCT below 1 DAI with the treasury assets until no one is left to sell. You can't trust the FED but you can trust the code.

As the protocol accumulates more PCV, more runway is guaranteed for the stakers. This means the stakers can be confident that the current staking APY can be sustained for a longer term because more funds are available in the treasury.

## Why is the market price of SANCT so volatile?

It is extremely important to understand how early in development the Sanctuary protocol is. A large amount of discussion has centered around the current price and expected a stable value moving forward. The reality is that these characteristics are not yet determined. The network is currently tuned for expansion of SANCT supply, which when paired with the staking, bonding, and yield mechanics of Sanctuary, result in a fair amount of volatility.

SANCT could trade at a very high price because the market is ready to pay a hefty premium to capture a percentage of the current market capitalization. However, the price of SANCT could also drop to a large degree if the market sentiment turns bearish. We would expect significant price volatility during our growth phase so please **do your own research** whether this project suits your goals.

## What is the point of buying it now when SANCT trades at a very high premium?

When you buy and stake SANCT, you capture a percentage of the supply \(market cap\) which will remain close to a constant. This is because your staked SANCT balance also increases along with the circulating supply. The implication is that if you buy SANCT when the market cap is low, you would be capturing a larger percentage of the market cap.

## What is a rebase?

Rebase is a mechanism by which your staked SANCT balance increases automatically. When new SANCT are minted by the protocol, a large portion of it goes to the stakers. Because stakers only see staked SANCT balance instead of SANCT, the protocol utilizes the rebase mechanism to increase the staked SANCT balance so that 1 staked SANCT is always redeemable for 1 SANCT.

## What is reward yield?

Reward yield is the percentage by which your staked SANCT balance increases on the next epoch. It is also known as _rebase rate_. You can find this number on the [Sanctuary staking page](https://app.Sanctuary.fi/#/stake).

## What is APY?

APY stands for annual percentage yield. It measures the real rate of return on your principal by taking into account the effect of compounding interest. In the case of Sanctuary, your staked SANCT represents your principal, and the compound interest is added periodically on every epoch \(2200 Ethereum blocks, or around 8 hours\) thanks to the rebase mechanism.

One interesting fact about APY is that your balance will grow not linearly but exponentially over time! Assuming a daily compound interest of 2%, if you start with a balance of 1 SANCT on day 1, after a year, your balance will grow to about 1377. That is a lot!

![The power of compounding](../.gitbook/assets/apy.png)

## How is the APY calculated?

The APY is calculated from the reward yield \(a.k.a rebase rate\) using the following equation:

$$
APY = ( 1 + rewardYield )^{1095}
$$

It raises to the power of 1095 because a rebase happens 3 times daily. Consider there are 365 days in a year, this would give a rebase frequency of 365 \* 3 = 1095.

Reward yield is determined by the following equation:

$$
rewardYield = SANCT_{distributed} / SANCT_{totalStaked}
$$

The number of SANCT distributed to the staking contract is calculated from SANCT total supply using the following equation:

$$
SANCT_{distributed} = SANCT_{totalSupply} \times rewardRate
$$

Note that the reward rate is subject to change by the protocol.

## Why does the price of SANCT become irrelevant in long term?

As illustrated above, your SANCT balance will grow exponentially over time thanks to the power of compounding. Let's say you buy an SANCT for $400 now and the market decides that in 1 year time, the intrinsic value of SANCT will be $2. Assuming a daily compound interest rate of 2%, your balance would grow to about 1377 SANCTs by the end of the year, which is worth around $2754. That is a cool $2354 profit! By now, you should understand that you are paying a premium for SANCT now in exchange for a long-term benefit. Thus, you should have a long time horizon to allow your SANCT balance to grow exponentially and make this a worthwhile investment.

## What will be SANCT's intrinsic value in the future?

There is no clear answer for this, but the intrinsic value can be determined by the treasury performance. For example, if the treasury could guarantee to back every SANCT with 100 DAI, the intrinsic value will be 100 DAI. It can also be decided by the DAO. For example, if the DAO decides to raise the price floor, its intrinsic value will rise accordingly.

## How does the protocol manage to maintain the high staking APY?

Let’s say the protocol targets an APY range of 1,000% to 10,000%, this would translate to a *minimum* reward yield of about 0.2105%,
or a daily growth of about 0.6328%.

If there are 100,000 of SANCT staked right now, the protocol would need to mint an
additional 632.8 SANCT to achieve this daily growth. This is achievable if the protocol
can bring in at least $632.80 of daily revenue from bond sales. Even if the protocol
doesn't bring in that much revenue, it can still sustain 1,000% APY for a considerable
amount of time (see the [runway chart](https://dune.xyz/queries/102766/207436)
for instance) due to the excess reserve in the treasury.

## Do I have to unstake and stake SANCT on every epoch to get my rebase rewards?

No. Once you have staked SANCT with Sanctuary, your staked SANCT balance will auto-compound on every epoch. That increase in balance represents your rebase rewards.