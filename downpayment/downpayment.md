# Downpayment

This is the entrance contract for down payment

### Methods <a href="#addcurrency" id="addcurrency"></a>

#### buy[​](broken-reference)

```
function buy(address adapter,uint256 borrowAmount,bytes calldata data,Sig calldata sig) external payable;
```

Buy nft from the marketplace with downpayment

**Parameters**[**​**](broken-reference)

| Name         | Type             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------ | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| adapter      | address          | address of the marketplace adapter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| borrowAmount | uint256          | amount of borrowed from lending pool (max borrowable amount: [lendPool.getNftCollateralData.totalCollateralInReserve](../lending-protocol/lendpool.md#getnftcollateraldata))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| data         | bytes            | <p>encoded order data for the marketplace, each markeplace have different order type:<br><a href="https://github.com/BendDAO/bend-downpayment/blob/01c0f248f76cff4d599b3e3868843663afa51ae6/contracts/interfaces/IX2Y2.sol#L67">x2y2</a>, <a href="https://github.com/BendDAO/bend-downpayment/blob/01c0f248f76cff4d599b3e3868843663afa51ae6/contracts/interfaces/ISeaport.sol#L132">seaport</a>,  <a href="https://github.com/BendDAO/bend-downpayment/blob/eb344f81dace9ddbae0b919b13434690b5961c2b/contracts/interfaces/ILooksRareExchange.sol#L5">looksrare</a>, <a href="https://github.com/BendDAO/bend-downpayment/blob/eb344f81dace9ddbae0b919b13434690b5961c2b/contracts/interfaces/IBendExchange.sol#L5">bend</a></p> |
| sig          | IDownpayment.Sig | ignature of the order with nonce, can be verified by [eip721](https://eips.ethereum.org/EIPS/eip-721) and [eip1271](https://eips.ethereum.org/EIPS/eip-1271)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

#### addAdapter

```
function addAdapter(address adapter) external nonpayable
```

add new adapter

**Parameters**

| Name    | Type    | Description                        |
| ------- | ------- | ---------------------------------- |
| adapter | address | address of the marketplace adapter |

#### removeAdapter

```
function removeAdapter(address adapter) external nonpayable
```

remove adapter

**Parameters**

| Name    | Type    | Description                        |
| ------- | ------- | ---------------------------------- |
| adapter | address | address of the marketplace adapter |

#### renounceOwnership[​](broken-reference) <a href="#renounceownership" id="renounceownership"></a>

```
function renounceOwnership() external nonpayable
```

_Leaves the contract without owner. It will not be possible to call `onlyOwner` functions anymore. Can only be called by the current owner. NOTE: Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner._

#### transferOwnership[​](broken-reference) <a href="#transferownership" id="transferownership"></a>

```
function transferOwnership(address newOwner) external nonpayable
```

_Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner._

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description              |
| -------- | ------- | ------------------------ |
| newOwner | address | address of the new owner |

### View methods

#### WETH

```
function WETH() external view returns (address)
```

**Returns**

| Name | Type    | Description                                    |
| ---- | ------- | ---------------------------------------------- |
| WETH | address | address of the WETH ("Wrapped Ether") contract |

#### getFee

```
function getFee(address adapter) external view returns (uint256)
```

****

**Parameters**

| Name    | Type    | Description                        |
| ------- | ------- | ---------------------------------- |
| adapter | address | address of the marketplace adapter |

**Returns**

| Name | Type    | Description                   |
| ---- | ------- | ----------------------------- |
| fee  | uint256 | protocol fee (e.g., 200 = 2%) |

#### getFeeCollector

```
function getFeeCollector() external view returns (address)
```

**Returns**

| feeCollector | address |  address of fee collector |
| ------------ | ------- | ------------------------- |

#### getBendLendPool

```
function getBendLendPool() external view returns (ILendPool)
```

**Returns**

| Name         | Type               | Description                |
| ------------ | ------------------ | -------------------------- |
| bendLendPool | contract ILendPool |  address of bend lend pool |

#### getAaveLendPool

```
function getAaveLendPool() external view returns (IAaveLendPool)
```

**Returns**

| Name         | Type                   | Description                |
| ------------ | ---------------------- | -------------------------- |
| aaveLendPool | contract IAaveLendPool |  address of aave lend pool |

#### nonces

```
function nonces(address owner) external view returns (uint256)
```

**Parameters**

| Name  | Type    | Description          |
| ----- | ------- | -------------------- |
| owner | address | address of the owner |

**Returns**

| Name  | Type    | Description         |
| ----- | ------- | ------------------- |
| nonce | uint256 | next nonce of owner |

#### isAdapterWhitelisted[​](broken-reference) <a href="#viewcountwhitelistedcurrencies" id="viewcountwhitelistedcurrencies"></a>

```
function isAdapterWhitelisted(address adapter) external view returns (bool)
```

Returns if a adapter is in the system

**Parameters**[**​**](broken-reference)

| Name    | Type    | Description            |
| ------- | ------- | ---------------------- |
| adapter | address | address of the adapter |

**Returns**[**​**](broken-reference)

| Name | Type | Description                    |
| ---- | ---- | ------------------------------ |
| -    | bool | whether adapter is whitelisted |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### viewCountWhitelistedAdapters[​](broken-reference) <a href="#removecurrency" id="removecurrency"></a>

```
function viewCountWhitelistedAdapters() external view returns (uint256)
```

View number of whitelisted adapters

**Returns**[**​**](broken-reference)

| Name | Type    | Description                                 |
| ---- | ------- | ------------------------------------------- |
| -    | uint256 | number of adapters valid on the downpayment |

#### viewWhitelistedAdapters <a href="#viewwhitelistedcurrencies" id="viewwhitelistedcurrencies"></a>

```
function viewWhitelistedAdapters(uint256 cursor, uint256 size) external view returns (address[], uint256)
```

See whitelisted adapters in the system

**Parameters**[**​**](broken-reference)

| Name   | Type    | Description                                  |
| ------ | ------- | -------------------------------------------- |
| cursor | uint256 | cursor (should start at 0 for first request) |
| size   | uint256 | size of the response (e.g., 50)              |

**Returns**[**​**](broken-reference)

| Name   | Type       | Description                |
| ------ | ---------- | -------------------------- |
| -      | address\[] | array of adapter addresses |
| cursor | uint256    | cursor position            |

### &#x20;<a href="#currencyremoved" id="currencyremoved"></a>
