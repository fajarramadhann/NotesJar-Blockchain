### Pump.fun works
pump prevents rugs by making sure that all created tokens are safe. each coin on pump is a fair-launch with no presale and no team allocation.

step 1: pick a coin that you like
step 2: buy the coin on the bonding curve
step 3: sell at any time to lock in your profits or losses
step 4: when enough people buy on the bonding curve it reaches a market cap of $100k
step 5: $17k of liquidity is then deposited in raydium and burned

### Memehunter.wtf
While virtual liquidity is innovative, the current ecosystem isn't ideal for meme coin hunters. MemeHunter improves this by introducing:

1. **Token Developer Vesting** Ensuring long-term developer commitment.
2. **Trading Fee Sharing** Distributing trading fees to developers.
3. **Revenue Resharing** Sharing revenue with the community.

# ⚖️Liquidity Pool

## What is virtual liquidity

When a token is created, it is worthless until added to a liquidity pool, which typically requires depositing Ethereum.

We address this liquidity issue with our "virtual liquidity concept." Each token created on MemeHunter will have a fixed supply of 1 billion tokens and 0.6-1.2 Virtual ETH in the pool (Depending on the Eth Price), referred to as the "carrier bag" on our platform.

This concept sets the initial market price of a token at 0.6-1.2 ETH, creating virtual liquidity equivalent to 2 times of ETH in the virtual reserve (since the value of all tokens is set to equal the value of ETH).

## What happen when it is hitting Uniswap

After accumulating some transactions, our AMM contract, CarrierBag.sol, will hold Ethereum.

When the contract contains 4 times of Real Eth compare to Virtual Eth (ie: 1 Virtual ETH and 4 Real ETH from transactions) or has 200 million tokens left, it will activate the Uniswap process.

## 

[](https://docs.memehunter.wtf/foundations/liquidity-pool#what-is-the-uniswap-process)

## What is the Uniswap process

**Our CarrierBag will then transfer all the accumulated ETH from transactions and 160 million tokens to Uniswap V3 (4/5 of token left within the pool)**

Unlike other platforms that take a percentage of ETH or Solana (typically 5-10 Solana) during this process, we deposit all the ETH into the pool. We believe this approach is fairer as it prevents immediate dilution of the token price.

We store only 160 million tokens (instead of 200 million) or 4/5 of total token left, to maintain the token's price stability when they are moved to Uniswap, because the real ETH in the pool is only 4/5 out of the reserve because 1/5 is virtual ETH. This strategy discourages dumping before the Uniswap transfer, as there is no incentive for it. Check Calculation Below

## 

[](https://docs.memehunter.wtf/foundations/liquidity-pool#calculation-for-fullfilling-the-bag)

Calculation for fullfilling the bag

The initial market cap will be set around 2800-3200, this is done so, by adjusting virtual ETH reserve to current price of Ethereum per 1 billion coins. after 80% of the supply being sold, there will only be 20% token remaining which is 200 Million, with amount of Real Eth accrued is 4 Times of virtual ETH. which will resulted Market Cap around $70000-$80000

Problem that they solve:
1. Many people got scammed by buying token that they can't sell _(Honeypot)_
2. Developer pulling out liquidity _(Rug Pull)_
3. Dev dumping supply
4. 