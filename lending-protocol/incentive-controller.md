# Incentive Controller

The incentive Controller is for the BEND tokens rewards which can be earned by the lenders and borrowers.

## Methods

### claimRewards

**function claimRewards(address\[] \_assets, uint256 \_amount)**

Claims reward for a user, on all the assets of the lending pool, accumulating the pending rewards.

| Parameter Name | Type       | Description                                                              |
| -------------- | ---------- | ------------------------------------------------------------------------ |
| \_assets       | address\[] | The addresses of the bTokens and debtTokens, etc. bendWETH, bendDebtWETH |
| \_amount       | uint256    | The rewards amount to be claimed                                         |

## View Methods

### getRewardsBalance

**function getRewardsBalance(address\[] \_assets, address \_user)**

Returns the total of rewards of a user, already accrued + not yet accrued.

| Parameter Name | Type       | Description                                                              |
| -------------- | ---------- | ------------------------------------------------------------------------ |
| \_assets       | address\[] | The addresses of the bTokens and debtTokens, etc. bendWETH, bendDebtWETH |
| \_user         | address    | The address of user                                                      |

**Return Values**

| Parameter Name | Type    | Description |
| -------------- | ------- | ----------- |
| rewards        | uint256 | the rewards |

### getUserUnclaimedRewards

**function getUserUnclaimedRewards(address \_user)**

Returns the unclaimed rewards of the user

**Return Values**

| Parameter Name | Type    | Description         |
| -------------- | ------- | ------------------- |
| \_user         | address | The address of user |

**Return Values**

| Parameter Name | Type    | Description |
| -------------- | ------- | ----------- |
| rewards        | uint256 | the rewards |
