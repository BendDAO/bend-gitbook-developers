# StakeManager

Contract used for manager staking

### Methods <a href="#addcurrency" id="addcurrency"></a>

#### stake[​](broken-reference)

```
function stake(
    DataTypes.ApeStaked memory apeStaked,
    DataTypes.BakcStaked memory bakcStaked,
    DataTypes.CoinStaked memory coinStaked
) external 
```

stake ape & bakc & coin

Parameters[**​**](broken-reference)

| Name       | Type                | Description                      |
| ---------- | ------------------- | -------------------------------- |
| apeStaked  | DataTypes.ApeStaked | the  data struct for ape staking |
| bakcStaked | DataTypes.BakcOffer | the data struct for bakc staking |
| coinStaked | DataTypes.CoinOffer | the data struct for coin staking |

#### approveOperator

```
function approveOperator(address operator) external
```

approve a operator for unStake

Parameters

| Name     | Type    | Description             |
| -------- | ------- | ----------------------- |
| operator | address | the address of operator |

#### revokeOperator

```
function revokeOperator() external 
```

remove the operator for `msg.sender`

#### unStake[​](broken-reference) <a href="#renounceownership" id="renounceownership"></a>

```
function unStake(IStakeProxy proxy) external 
```

_UnStake the proxy_

Parameters

| Name  | Type    | Description                |
| ----- | ------- | -------------------------- |
| proxy | address | the address of stake proxy |



#### claim[​](broken-reference) <a href="#transferownership" id="transferownership"></a>

```
function claim(IStakeProxy proxy) external
```

Claim rewards for `msg.sender` from stake proxy

Parameters[**​**](broken-reference)

| Name  | Type    | Description                |
| ----- | ------- | -------------------------- |
| proxy | address | the address of stake proxy |

#### claimFor

```
function claimFor(IStakeProxy proxy, address staker) external
```

Claim rewards for staker from stake proxy

Parameters

| Name   | Type    | Description                              |
| ------ | ------- | ---------------------------------------- |
| proxy  | address | the address of stake proxy               |
| staker | address | the address of staker to receive rewards |

#### borrowETH

```
function borrowETH(
    uint256 amount,
    address apeAsset,
    uint256 apeTokenId
) external
```

Borrow ETH when the ape staked

Paremeters

| Name       | Type    |                                        |
| ---------- | ------- | -------------------------------------- |
| amount     | uint256 | the amount of ETH need to borrow       |
| apeAsset   | address | the address of ape used as collateral  |
| apeTokenId | uint256 | the token id of ape used as collateral |

### View methods

#### claimable

```
function claimable(IStakeProxy proxy, address staker) external view returns (uint256)
```

Query claimable rewards amount for staker from stake proxy

Paremeters

| Name   | Type    | Description                              |
| ------ | ------- | ---------------------------------------- |
| proxy  | address | the address of stake proxy               |
| staker | address | the sddress of staker to receive rewards |

Returns

| Name   | Type    | Description                     |
| ------ | ------- | ------------------------------- |
| amount | uint256 | the amount of claimable rewards |

****

### &#x20;<a href="#currencyremoved" id="currencyremoved"></a>
