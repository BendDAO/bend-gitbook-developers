# BendExchange

It is the core contract of the Bend exchange.

### Methods <a href="#cancelallordersforsender" id="cancelallordersforsender"></a>

#### matchAskWithTakerBid[​](broken-reference) <a href="#matchaskwithtakerbid" id="matchaskwithtakerbid"></a>

```
function matchAskWithTakerBid(OrderTypes.TakerOrder takerBid, OrderTypes.MakerOrder makerAsk) external nonpayable
```

Match a takerBid with a matchAsk

**Parameters**[**​**](broken-reference)

| Name     | Type                  | Description     |
| -------- | --------------------- | --------------- |
| takerBid | OrderTypes.TakerOrder | taker bid order |
| makerAsk | OrderTypes.MakerOrder | maker ask order |

#### matchAskWithTakerBidUsingETHAndWETH[​](broken-reference) <a href="#matchaskwithtakerbidusingethandweth" id="matchaskwithtakerbidusingethandweth"></a>

```
function matchAskWithTakerBidUsingETHAndWETH(OrderTypes.TakerOrder takerBid, OrderTypes.MakerOrder makerAsk) external payable
```

Match ask with a taker bid order using ETH

**Parameters**[**​**](broken-reference)

| Name     | Type                  | Description     |
| -------- | --------------------- | --------------- |
| takerBid | OrderTypes.TakerOrder | taker bid order |
| makerAsk | OrderTypes.MakerOrder | maker ask order |

#### matchBidWithTakerAsk[​](broken-reference) <a href="#matchbidwithtakerask" id="matchbidwithtakerask"></a>

```
function matchBidWithTakerAsk(OrderTypes.TakerOrder takerAsk, OrderTypes.MakerOrder makerBid) external nonpayable
```

Match a takerAsk with a makerBid

**Parameters**[**​**](broken-reference)

| Name     | Type                  | Description     |
| -------- | --------------------- | --------------- |
| takerAsk | OrderTypes.TakerOrder | taker ask order |
| makerBid | OrderTypes.MakerOrder | maker bid order |

#### cancelAllOrdersForSender[​](broken-reference) <a href="#cancelallordersforsender" id="cancelallordersforsender"></a>

```
function cancelAllOrdersForSender(uint256 minNonce) external nonpayable
```

Cancel all pending orders for a sender

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description        |
| -------- | ------- | ------------------ |
| minNonce | uint256 | minimum user nonce |

#### cancelMultipleMakerOrders[​](broken-reference) <a href="#cancelmultiplemakerorders" id="cancelmultiplemakerorders"></a>

```
function cancelMultipleMakerOrders(uint256[] orderNonces) external nonpayable
```

Cancel maker orders

**Parameters**[**​**](broken-reference)

| Name        | Type       | Description           |
| ----------- | ---------- | --------------------- |
| orderNonces | uint256\[] | array of order nonces |

#### CancelMultipleOrders[​](broken-reference) <a href="#cancelmultipleorders" id="cancelmultipleorders"></a>

```
event CancelMultipleOrders(address indexed user, uint256[] orderNonces)
```

**Parameters**[**​**](broken-reference)

| Name           | Type       | Description                              |
| -------------- | ---------- | ---------------------------------------- |
| user `indexed` | address    | user address                             |
| orderNonces    | uint256\[] | array of order nonces that are cancelled |

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

#### updateAuthorizationManager[​](broken-reference) <a href="#updatecurrencymanager" id="updatecurrencymanager"></a>

```
function updateAuthorizationManager(address _authorizationManager) external nonpayable
```

Update authorization manager

**Parameters**[**​**](broken-reference)

| Name                   | Type    | Description                       |
| ---------------------- | ------- | --------------------------------- |
| \_authorizationManager | address | new authorization manager address |

#### updateCurrencyManager[​](broken-reference) <a href="#updateexecutionmanager" id="updateexecutionmanager"></a>

```
function updateCurrencyManager(address _currencyManager) external nonpayable
```

Update currency manager

**Parameters**[**​**](broken-reference)

| Name              | Type    | Description                  |
| ----------------- | ------- | ---------------------------- |
| \_currencyManager | address | new currency manager address |

#### updateExecutionManager[​](broken-reference) <a href="#updateexecutionmanager" id="updateexecutionmanager"></a>

```
function updateExecutionManager(address _executionManager) external nonpayable
```

Update execution manager

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description                   |
| ------------------ | ------- | ----------------------------- |
| \_executionManager | address | new execution manager address |

#### updateProtocolFeeRecipient[​](broken-reference) <a href="#updateprotocolfeerecipient" id="updateprotocolfeerecipient"></a>

```
function updateProtocolFeeRecipient(address _protocolFeeRecipient) external nonpayable
```

Update protocol fee and recipient

**Parameters**[**​**](broken-reference)

| Name                   | Type    | Description                     |
| ---------------------- | ------- | ------------------------------- |
| \_protocolFeeRecipient | address | new recipient for protocol fees |

#### updateRoyaltyFeeManager[​](broken-reference) <a href="#updateroyaltyfeemanager" id="updateroyaltyfeemanager"></a>

```
function updateRoyaltyFeeManager(address _royaltyFeeManager) external nonpayable
```

Update royalty fee manager

**Parameters**[**​**](broken-reference)

| Name                | Type    | Description             |
| ------------------- | ------- | ----------------------- |
| \_royaltyFeeManager | address | new fee manager address |

#### updateTransferManager[​](broken-reference) <a href="#updatetransferselectornft" id="updatetransferselectornft"></a>

```
function updateTransferManager(address _transferManager) external nonpayable
```

Update transfer manager

**Parameters**[**​**](broken-reference)

| Name              | Type    | Description                  |
| ----------------- | ------- | ---------------------------- |
| \_transferManager | address | new transfer manager address |

#### updateInterceptorManager[​](broken-reference)

```
function updateInterceptorManager(address _interceptorManager) external nonpayable
```

Update interceptor manager

**Parameters**[**​**](broken-reference)

| Name                 | Type    | Description                     |
| -------------------- | ------- | ------------------------------- |
| \_interceptorManager | address | new interceptor manager address |

### View methods

#### DOMAIN\_SEPARATOR[​](broken-reference) <a href="#domain_separator" id="domain_separator"></a>

```
function DOMAIN_SEPARATOR() external view returns (bytes32)
```

**Returns**[**​**](broken-reference)

| Name              | Type    | Description                                                        |
| ----------------- | ------- | ------------------------------------------------------------------ |
| DOMAIN\_SEPARATOR | bytes32 | EIP-712 domain separator for the exchange[**​**](broken-reference) |

#### WETH[​](https://docs.looksrare.org/developers/exchange/LooksRareExchange#weth) <a href="#weth" id="weth"></a>

```
function WETH() external view returns (address)
```

**Returns**[**​**](https://docs.looksrare.org/developers/exchange/LooksRareExchange#returns-1)

| Name | Type    | Description                                    |
| ---- | ------- | ---------------------------------------------- |
| WETH | address | address of the WETH ("Wrapped Ether") contract |

#### authorizationManager[​](broken-reference) <a href="#currencymanager" id="currencymanager"></a>

```
function authorizationManager() external view returns (contract IAuthorizationManager)
```

**Returns**[**​**](broken-reference)

| Name                                               | Type                           | Description                         |
| -------------------------------------------------- | ------------------------------ | ----------------------------------- |
| <h4 id="currencymanager">authorizationManager</h4> | contract IAuthorizationManager | address of the AuthorizationManager |

#### currencyManager[​](broken-reference) <a href="#currencymanager" id="currencymanager"></a>

```
function currencyManager() external view returns (contract ICurrencyManager)
```

**Returns**[**​**](broken-reference)

| Name            | Type                      | Description                    |
| --------------- | ------------------------- | ------------------------------ |
| currencyManager | contract ICurrencyManager | address of the CurrencyManager |

#### executionManager[​](broken-reference) <a href="#executionmanager" id="executionmanager"></a>

```
function executionManager() external view returns (contract IExecutionManager)
```

**Returns**[**​**](broken-reference)

| Name             | Type                       | Description                     |
| ---------------- | -------------------------- | ------------------------------- |
| executionManager | contract IExecutionManager | address of the ExecutionManager |

#### royaltyFeeManager[​](broken-reference) <a href="#royaltyfeemanager" id="royaltyfeemanager"></a>

```
function royaltyFeeManager() external view returns (contract IRoyaltyFeeManager)
```

**Returns**[**​**](broken-reference)

| Name              | Type                        | Description                      |
| ----------------- | --------------------------- | -------------------------------- |
| royaltyFeeManager | contract IRoyaltyFeeManager | address of the RoyaltyFeeManager |

#### transferManager[​](broken-reference) <a href="#isuserordernonceexecutedorcancelled" id="isuserordernonceexecutedorcancelled"></a>

```
function transferManager() external view returns (contract ITransferManager)
```

**Returns**[**​**](broken-reference)

| Name            | Type                      | Description                             |
| --------------- | ------------------------- | --------------------------------------- |
| transferManager | contract ITransferManager | address of the TransferManager contract |

#### interceptorManager[​](broken-reference) <a href="#userminordernonce" id="userminordernonce"></a>

```
function interceptorManager() external view returns (contract IInterceptorManager)
```

**Returns**[**​**](broken-reference)

| Name               | Type                         | Description                                |
| ------------------ | ---------------------------- | ------------------------------------------ |
| interceptorManager | contract IInterceptorManager | address of the InterceptorManager contract |

#### isUserOrderNonceExecutedOrCancelled[​](broken-reference) <a href="#userminordernonce" id="userminordernonce"></a>

```
function isUserOrderNonceExecutedOrCancelled(address user, uint256 orderNonce) external view returns (bool)
```

Check whether user order nonce is executed or cancelled

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description        |
| ---------- | ------- | ------------------ |
| user       | address | address of user    |
| orderNonce | uint256 | nonce of the order |

**Returns**[**​**](broken-reference)

| Name | Type | Description                                                                                                               |
| ---- | ---- | ------------------------------------------------------------------------------------------------------------------------- |
| -    | bool | whether the user order nonce is executed or cancelled (for cancels, it needs to be checked against the minOrderNonce too) |

#### protocolFeeRecipient[​](broken-reference) <a href="#protocolfeerecipient" id="protocolfeerecipient"></a>

```
function protocolFeeRecipient() external view returns (address)
```

**Returns**[**​**](broken-reference)

| Name                 | Type    | Description                           |
| -------------------- | ------- | ------------------------------------- |
| protocolFeeRecipient | address | address of the protocol fee recipient |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### userMinOrderNonce[​](broken-reference) <a href="#userminordernonce" id="userminordernonce"></a>

```
function userMinOrderNonce(address) external view returns (uint256)
```

**Parameters**[**​**](broken-reference)

| Name | Type    | Description  |
| ---- | ------- | ------------ |
| user | address | user address |

**Returns**[**​**](broken-reference)

| Name          | Type    | Description                                                                                                                                 |
| ------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| minOrderNonce | uint256 | minimum order nonce that defines the validity of user orders. If an order has a nonce inferior to the minOrderNonce, it cannot be executed. |

### Events <a href="#newcurrencymanager" id="newcurrencymanager"></a>

#### CancelAllOrders[​](broken-reference) <a href="#newcurrencymanager" id="newcurrencymanager"></a>

```
event CancelAllOrders(address indexed user, uint256 newMinNonce)
```

**Parameters**[**​**](broken-reference)

| Name           | Type    | Description             |
| -------------- | ------- | ----------------------- |
| user `indexed` | address | user address            |
| newMinNonce    | uint256 | new minimum order nonce |

#### NewAuthorizationManager[​](broken-reference) <a href="#cancelmultipleorders" id="cancelmultipleorders"></a>

```
event NewAuthorizationManager(address indexed authorizationManager)
```

**Parameters**[**​**](broken-reference)

| Name                           | Type    | Description                             |
| ------------------------------ | ------- | --------------------------------------- |
| authorizationManager `indexed` | address | address of the new AuthorizationManager |

#### NewCurrencyManager[​](broken-reference) <a href="#newexecutionmanager" id="newexecutionmanager"></a>

```
event NewCurrencyManager(address indexed currencyManager)
```

**Parameters**[**​**](broken-reference)

| Name                      | Type    | Description                        |
| ------------------------- | ------- | ---------------------------------- |
| currencyManager `indexed` | address | address of the new CurrencyManager |

#### NewExecutionManager[​](broken-reference) <a href="#newexecutionmanager" id="newexecutionmanager"></a>

```
event NewExecutionManager(address indexed executionManager)
```

**Parameters**[**​**](broken-reference)

| Name                       | Type    | Description                         |
| -------------------------- | ------- | ----------------------------------- |
| executionManager `indexed` | address | address of the new ExecutionManager |

#### NewProtocolFeeRecipient[​](broken-reference) <a href="#newprotocolfeerecipient" id="newprotocolfeerecipient"></a>

```
event NewProtocolFeeRecipient(address indexed protocolFeeRecipient)
```

**Parameters**[**​**](broken-reference)

| Name                           | Type    | Description                               |
| ------------------------------ | ------- | ----------------------------------------- |
| protocolFeeRecipient `indexed` | address | address of the new protocol fee recipient |

#### NewRoyaltyFeeManager[​](broken-reference) <a href="#newroyaltyfeemanager" id="newroyaltyfeemanager"></a>

```
event NewRoyaltyFeeManager(address indexed royaltyFeeManager)
```

**Parameters**[**​**](broken-reference)

| Name                        | Type    | Description                          |
| --------------------------- | ------- | ------------------------------------ |
| royaltyFeeManager `indexed` | address | address of the new RoyaltyFeeManager |

#### NewTransferManager[​](broken-reference) <a href="#newtransferselectornft" id="newtransferselectornft"></a>

```
event NewTransferManager(address indexed transferManager)
```

**Parameters**[**​**](broken-reference)

| Name                      | Type    | Description                        |
| ------------------------- | ------- | ---------------------------------- |
| transferManager `indexed` | address | address of the new TransferManager |

#### NewInterceptorManager[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event NewInterceptorManager(address indexed interceptorManager)
```

**Parameters**[**​**](broken-reference)

| Name                         | Type    | Description                           |
| ---------------------------- | ------- | ------------------------------------- |
| interceptorManager `indexed` | address | address of the new InterceptorManager |

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |

#### RoyaltyPayment[​](broken-reference) <a href="#royaltypayment" id="royaltypayment"></a>

```
event RoyaltyPayment(address indexed collection, uint256 indexed tokenId, address indexed royaltyRecipient, address currency, uint256 amount)
```

**Parameters**[**​**](broken-reference)

| Name                       | Type    | Description                |
| -------------------------- | ------- | -------------------------- |
| collection `indexed`       | address | collection address         |
| tokenId `indexed`          | uint256 | tokenId                    |
| royaltyRecipient `indexed` | address | royalty fee recipient      |
| currency                   | address | currency used (e.g., WETH) |
| amount                     | uint256 | royalty amount transferred |

#### ProtocolFeePayment[​](broken-reference) <a href="#takerask" id="takerask"></a>

```
event ProtocolFeePayment(address indexed collection,uint256 indexed tokenId,address indexed protocolFeeRecipient,address currency,uint256 amount);
```

**Parameters**[**​**](broken-reference)

| Name                           | Type    | Description                |
| ------------------------------ | ------- | -------------------------- |
| collection `indexed`           | address | collection address         |
| tokenId `indexed`              | uint256 | tokenId                    |
| protocolFeeRecipient `indexed` | address | protocol fee recipient     |
| currency                       | address | currency used (e.g., WETH) |
| amount                         | uint256 | royalty amount transferred |

#### TakerAsk[​](broken-reference) <a href="#takerask" id="takerask"></a>

```
event TakerAsk(bytes32 orderHash, uint256 orderNonce, address indexed taker, address indexed maker, address indexed strategy, address currency, address collection, uint256 tokenId, uint256 amount, uint256 price)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description                       |
| ------------------ | ------- | --------------------------------- |
| orderHash          | bytes32 | order hash                        |
| orderNonce         | uint256 | user order nonce (for the maker)  |
| taker `indexed`    | address | taker address                     |
| maker `indexed`    | address | maker address                     |
| strategy `indexed` | address | address of the execution strategy |
| currency           | address | currency address                  |
| collection         | address | collection address                |
| tokenId            | uint256 | tokenId                           |
| amount             | uint256 | amount of tokens transferred      |
| price              | uint256 | gross transaction price           |

#### TakerBid[​](broken-reference) <a href="#takerbid" id="takerbid"></a>

```
event TakerBid(bytes32 orderHash, uint256 orderNonce, address indexed taker, address indexed maker, address indexed strategy, address currency, address collection, uint256 tokenId, uint256 amount, uint256 price)
```

**Parameters**[**​**](broken-reference)

| Name               | Type    | Description                       |
| ------------------ | ------- | --------------------------------- |
| orderHash          | bytes32 | order hash                        |
| orderNonce         | uint256 | user order nonce (for the maker)  |
| taker `indexed`    | address | taker address                     |
| maker `indexed`    | address | maker address                     |
| strategy `indexed` | address | address of the execution strategy |
| currency           | address | currency address                  |
| collection         | address | collection address                |
| tokenId            | uint256 | tokenId                           |
| amount             | uint256 | amount of tokens transferred      |
| price              | uint256 | gross transaction price           |
