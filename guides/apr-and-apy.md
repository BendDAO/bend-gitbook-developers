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

APR: getAssetData to fetch liquidity mining incentives for bToken/debtToken.

APY: getReserveDatato fetch deposit and borrow rates of asset.

```
[, liquidityIndex, variableBorrowIndex, 
currentLiquidityRate, currentVariableBorrowRate, ,
bTokenAddress,
debtTokenAddress, , ] = LendPool.getReserveData(asset.address) 
// asset is the ERC20 deposited or borrowed, eg. DAI, WETH

[,bEmissionPerSecond,] = IcentivesController.getAssetData(bTokenAddress)
[,dEmissionPerSecond,] = IcentivesController.getAssetData(debtTokenAddress)

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
    
    bEmissionPerSecond
    dEmissionPerSecond
    
    totalBTokenSupply
    totalCurrentVariableDebt
  }
}
```

### Compute Data

```

RAY = 10**27 // 10 to the power 27
SECONDS_PER_YEAR = 31536000

// Deposit and Borrow calculations
// APY and APR are returned here as decimals, multiply by 100 to get the percents

depositAPR = liquidityRate/RAY
variableBorrowAPR = variableBorrowRate/RAY

depositAPY = ((1 + (depositAPR / SECONDS_PER_YEAR)) ^ SECONDS_PER_YEAR) - 1
variableBorrowAPY = ((1 + (variableBorrowAPR / SECONDS_PER_YEAR)) ^ SECONDS_PER_YEAR) - 1
// Incentives calculation

bEmissionPerYear = bEmissionPerSecond * SECONDS_PER_YEAR
dEmissionPerYear = dEmissionPerSecond * SECONDS_PER_YEAR

incentiveDepositAPRPercent = 100 * (bEmissionPerYear * REWARD_PRICE_ETH * TOKEN_DECIMALS)/
                          (totalBTokenSupply * TOKEN_PRICE_ETH * REWARD_DECIMALS)
                          
incentiveBorrowAPRPercent = 100 * (dEmissionPerYear * REWARD_PRICE_ETH * TOKEN_DECIMALS)/
                          (totalCurrentVariableDebt * TOKEN_PRICE_ETH * REWARD_DECIMALS)

```
