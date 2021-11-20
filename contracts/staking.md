# Staking

## Distributor

The distributor contract receives minted SANCT from the treasury in order to drip-feed rewards to stakers. The reward rate target as of time of writing is set to 3500, which translates to 0.35% of total supply, since the reward rate is defined in tens of thousands. Note that the reward rate determines the rebase rate and that the rebase rate determines the APY. 

## Staking

The new staking contract works with a staking helper contract. The staking helper contract calls "stake" and then "claim" of the new staking contract. When the "stake" function is called, sSANCT is put into a warmup phase and all the information about how much sSANCT a user has staked is stored in the new staking contract. When the "claim" function is called, sSANCT is retrieved from the warmup and then sent to the user's wallet.