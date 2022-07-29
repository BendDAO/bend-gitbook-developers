# CurrencyManager

It allows adding/removing currencies for trading on the Bend exchange.

### Methods <a href="#addcurrency" id="addcurrency"></a>

#### addCurrency[​](broken-reference) <a href="#addcurrency" id="addcurrency"></a>

```
function addCurrency(address currency) external nonpayable
```

Add a currency in the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description                    |
| -------- | ------- | ------------------------------ |
| currency | address | address of the currency to add |

#### removeCurrency[​](broken-reference) <a href="#removecurrency" id="removecurrency"></a>

```
function removeCurrency(address currency) external nonpayable
```

Remove a currency from the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description                       |
| -------- | ------- | --------------------------------- |
| currency | address | address of the currency to remove |

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

### View methods <a href="#viewcountwhitelistedcurrencies" id="viewcountwhitelistedcurrencies"></a>

#### isCurrencyWhitelisted[​](broken-reference) <a href="#viewcountwhitelistedcurrencies" id="viewcountwhitelistedcurrencies"></a>

```
function isCurrencyWhitelisted(address currency) external view returns (bool)
```

Returns if a currency is in the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description             |
| -------- | ------- | ----------------------- |
| currency | address | address of the currency |

**Returns**[**​**](broken-reference)

| Name | Type | Description                  |
| ---- | ---- | ---------------------------- |
| -    | bool | whether currency is tradable |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### viewCountWhitelistedCurrencies[​](broken-reference) <a href="#removecurrency" id="removecurrency"></a>

```
function viewCountWhitelistedCurrencies() external view returns (uint256)
```

View number of whitelisted currencies

**Returns**[**​**](broken-reference)

| Name | Type    | Description                                |
| ---- | ------- | ------------------------------------------ |
| -    | uint256 | number of currencies valid on the exchange |

#### viewWhitelistedCurrencies[​](broken-reference) <a href="#viewwhitelistedcurrencies" id="viewwhitelistedcurrencies"></a>

```
function viewWhitelistedCurrencies(uint256 cursor, uint256 size) external view returns (address[], uint256)
```

See whitelisted currencies in the system

**Parameters**[**​**](broken-reference)

| Name   | Type    | Description                                  |
| ------ | ------- | -------------------------------------------- |
| cursor | uint256 | cursor (should start at 0 for first request) |
| size   | uint256 | size of the response (e.g., 50)              |

**Returns**[**​**](broken-reference)

| Name   | Type       | Description                 |
| ------ | ---------- | --------------------------- |
| -      | address\[] | array of currency addresses |
| cursor | uint256    | cursor position             |

### Events <a href="#currencyremoved" id="currencyremoved"></a>

#### CurrencyRemoved[​](broken-reference) <a href="#currencyremoved" id="currencyremoved"></a>

```
event CurrencyRemoved(address indexed currency)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description             |
| ------------------ | ------- | ----------------------- |
| currency `indexed` | address | address of the currency |

#### CurrencyWhitelisted[​](broken-reference) <a href="#currencywhitelisted" id="currencywhitelisted"></a>

```
event CurrencyWhitelisted(address indexed currency)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description             |
| ------------------ | ------- | ----------------------- |
| currency `indexed` | address | address of the currency |

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |
