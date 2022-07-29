# ExecutionManager

It allows adding/removing execution strategies for trading on the Bend exchange.

### Methods <a href="#addstrategy" id="addstrategy"></a>

#### addStrategy[​](broken-reference) <a href="#addstrategy" id="addstrategy"></a>

```
function addStrategy(address strategy) external nonpayable
```

Add an execution strategy in the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description                    |
| -------- | ------- | ------------------------------ |
| strategy | address | address of the strategy to add |

#### removeStrategy[​](broken-reference) <a href="#removestrategy" id="removestrategy"></a>

```
function removeStrategy(address strategy) external nonpayable
```

Remove an execution strategy from the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description                       |
| -------- | ------- | --------------------------------- |
| strategy | address | address of the strategy to remove |

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

### View methods <a href="#viewcountwhitelistedstrategies" id="viewcountwhitelistedstrategies"></a>

#### isStrategyWhitelisted[​](broken-reference) <a href="#viewcountwhitelistedstrategies" id="viewcountwhitelistedstrategies"></a>

```
function isStrategyWhitelisted(address strategy) external view returns (bool)
```

Returns if an execution strategy is in the system

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description             |
| -------- | ------- | ----------------------- |
| strategy | address | address of the strategy |

**Returns**[**​**](broken-reference)

| Name | Type | Description                         |
| ---- | ---- | ----------------------------------- |
| -    | bool | whether execution strategy is valid |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### viewCountWhitelistedStrategies[​](broken-reference) <a href="#removestrategy" id="removestrategy"></a>

```
function viewCountWhitelistedStrategies() external view returns (uint256)
```

View number of whitelisted strategies

**Returns**[**​**](broken-reference)

| Name | Type    | Description                                          |
| ---- | ------- | ---------------------------------------------------- |
| -    | uint256 | number of execution strategies valid on the exchange |

#### viewWhitelistedStrategies[​](broken-reference) <a href="#viewwhitelistedstrategies" id="viewwhitelistedstrategies"></a>

```
function viewWhitelistedStrategies(uint256 cursor, uint256 size) external view returns (address[], uint256)
```

See whitelisted strategies in the system

**Parameters**[**​**](broken-reference)

| Name   | Type    | Description                                  |
| ------ | ------- | -------------------------------------------- |
| cursor | uint256 | cursor (should start at 0 for first request) |
| size   | uint256 | size of the response (e.g., 50)              |

**Returns**[**​**](broken-reference)

| Name   | Type       | Description                           |
| ------ | ---------- | ------------------------------------- |
| -      | address\[] | array of execution strategy addresses |
| cursor | uint256    | cursor position                       |

### Events <a href="#ownershiptransferred" id="ownershiptransferred"></a>

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |

#### StrategyRemoved[​](broken-reference) <a href="#strategyremoved" id="strategyremoved"></a>

```
event StrategyRemoved(address indexed strategy)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description                       |
| ------------------ | ------- | --------------------------------- |
| strategy `indexed` | address | address of the execution strategy |

#### StrategyWhitelisted[​](broken-reference) <a href="#strategywhitelisted" id="strategywhitelisted"></a>

```
event StrategyWhitelisted(address indexed strategy)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description                       |
| ------------------ | ------- | --------------------------------- |
| strategy `indexed` | address | address of the execution strategy |
