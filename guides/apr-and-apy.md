---
description: You can query latest APR and APY on chain and subgraph
---

# APR and APY

{% hint style="info" %}
All rates queried on chain or subgraph, are expressed in RAY units i.e. 10^27. All emissions are expressed in WAD units i.e. 10^18.
{% endhint %}

{% hint style="info" %}
APY: Compounding interest accrued by deposit or borrow on LendPool.

APR: Non Compounding rewards earned as part of LiquidityIncentives.
{% endhint %}

The deposit and borrow APR displayed on the BendDAO front-end is calculated in real-time when the lending pool utilization ratio is changed.

## Conversions

Both of these conversions take the input and output in decimal form. Multiply the output by 100 to get the percentage.

### APR -> APY

To convert the APR to APY compounded per second the formula is:

$$
APY =  (1 + (APR/secondsPerYear)) ^ {secondsPerYear} - 1
$$

​APY -> APR

To convert the APY compounded per second to APR the formula is:

$$
APR = ((1 + APY) ^ {1/secondsPerYear} - 1) * secondsPerYear
$$

## ​Query Data

### On-Chain

APR: using assets method to fetch liquidity mining incentives for bToken/debtToken.

APY: using getReserveData method to fetch deposit and borrow rates of assets.

```
[, liquidityIndex, variableBorrowIndex, 
currentLiquidityRate, currentVariableBorrowRate, ,
bTokenAddress,
debtTokenAddress, , ] = LendPool.getReserveData(asset.address) 
// asset is the ERC20 deposited or borrowed, eg. DAI, WETH

totalBTokenSupply = bTokenAddress.totalSupply()
totalCurrentVariableDebt = debtTokenAddress.totalSupply()

[bEmissionPerSecond,,] = IcentivesController.assets(bTokenAddress)
[dEmissionPerSecond,,] = IcentivesController.assets(debtTokenAddress)

```

### Subgraph (GraphQL)

Use subgraph to query reserve data

```
{
  reserves {
    name
    underlyingAsset
    
    liquidityRate 
    variableBorrowRate
    
    totalBTokenSupply
    totalCurrentVariableDebt
  }
}
```

### Compute Data

```

RAY = 10**27 // 10 to the power 27
SECONDS_PER_YEAR = 31536000
TOKEN_DECIMALS = 18 // same as the underlying asset, etc.18 for WETH, 6 for USDT
REWARD_DECIMALS = 18 // BEND token is 18 always
TOKEN_PRICE_ETH = ??? // using Chainlink to get the price, 1e18 for WETH
REWARD_PRICE_ETH = ??? // using Uniswap V2 BEND/ETH pair to calculate the price 

// Deposit and Borrow calculations for reserve (etc. WETH, USDT)
// APY and APR are returned here as decimals, multiply by 100 to get the percents

depositAPR = liquidityRate/RAY
variableBorrowAPR = variableBorrowRate/RAY

depositAPY = ((1 + (depositAPR / SECONDS_PER_YEAR)) ^ SECONDS_PER_YEAR) - 1
variableBorrowAPY = ((1 + (variableBorrowAPR / SECONDS_PER_YEAR)) ^ SECONDS_PER_YEAR) - 1

// Incentives calculations for BEND token

bEmissionPerYear = bEmissionPerSecond * SECONDS_PER_YEAR
dEmissionPerYear = dEmissionPerSecond * SECONDS_PER_YEAR

incentiveDepositAPRPercent = 100 * (bEmissionPerYear * REWARD_PRICE_ETH * TOKEN_DECIMALS)/
                          (totalBTokenSupply * TOKEN_PRICE_ETH * REWARD_DECIMALS)

incentiveBorrowAPRPercent = 100 * (dEmissionPerYear * REWARD_PRICE_ETH * TOKEN_DECIMALS)/
                          (totalCurrentVariableDebt * TOKEN_PRICE_ETH * REWARD_DECIMALS)

```
