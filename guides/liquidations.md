# Liquidations

The health of the Bend Protocol is dependent on the 'health' of the loans within the system, also known as the 'health factor'. When the 'health factor' of an account's total loans is below 1, anyone can make an `auction()` and `liquidate()` to the LendPool contract, paying back all of the debt owed and receiving discounted collateral in return (also known as the liquidation bonus as listed here).

This incentives third parties to participate in the health of the overall protocol, by acting in their own interest (to receive the discounted collateral) and as a result, ensure loans are sufficiently collateralized.

There are multiple ways to participate in liquidations:

* By calling the `auction()` and `liquidate()` directly in the LendPool contract.
* By creating your own automated bot or system to liquidate loans.

{% hint style="danger" %}
For liquidation calls to be profitable, you must take into account the gas cost involved in liquidating the loan. If a high gas price is used, then the liquidation may be unprofitable for you. See the 'Calculating profitability vs gas cost' section for more details.
{% endhint %}

