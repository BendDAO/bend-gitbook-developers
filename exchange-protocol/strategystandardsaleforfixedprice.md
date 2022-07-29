# StrategyStandardSaleForFixedPrice

Strategy that executes an order at a fixed price that can be taken either by a bid or an ask.

### View methods <a href="#protocol_fee" id="protocol_fee"></a>

#### PROTOCOL\_FEE[​](broken-reference) <a href="#protocol_fee" id="protocol_fee"></a>

```
function PROTOCOL_FEE() external view returns (uint256)
```

**Returns**[**​**](broken-reference)

| Name          | Type    | Description                   |
| ------------- | ------- | ----------------------------- |
| PROTOCOL\_FEE | uint256 | protocol fee (e.g., 200 = 2%) |

#### canExecuteTakerAsk[​](broken-reference) <a href="#canexecutetakerask" id="canexecutetakerask"></a>

```
function canExecuteTakerAsk(OrderTypes.TakerOrder takerAsk, OrderTypes.MakerOrder makerBid) external view returns (bool, uint256, uint256)
```

Check whether a taker ask order can be executed against a maker bid

**Parameters**[**​**](broken-reference)

| Name     | Type                  | Description     |
| -------- | --------------------- | --------------- |
| takerAsk | OrderTypes.TakerOrder | taker ask order |
| makerBid | OrderTypes.MakerOrder | maker bid order |

**Returns**[**​**](broken-reference)

| Name    | Type    | Description                                                                       |
| ------- | ------- | --------------------------------------------------------------------------------- |
| isValid | bool    | whether strategy can be executed, tokenId to execute, amount of tokens to execute |
| price   | uint256 | price of the transaction                                                          |
| amount  | uint256 | amount of tokens to transfer                                                      |

#### canExecuteTakerBid[​](broken-reference) <a href="#canexecutetakerbid" id="canexecutetakerbid"></a>

```
function canExecuteTakerBid(OrderTypes.TakerOrder takerBid, OrderTypes.MakerOrder makerAsk) external view returns (bool, uint256, uint256)
```

Check whether a taker bid order can be executed against a maker ask

**Parameters**[**​**](broken-reference)

| Name     | Type                  | Description     |
| -------- | --------------------- | --------------- |
| takerBid | OrderTypes.TakerOrder | taker bid order |
| makerAsk | OrderTypes.MakerOrder | maker ask order |

**Returns**[**​**](broken-reference)

| Name    | Type    | Description                                                                       |
| ------- | ------- | --------------------------------------------------------------------------------- |
| isValid | bool    | whether strategy can be executed, tokenId to execute, amount of tokens to execute |
| price   | uint256 | price of the transaction                                                          |
| amount  | uint256 | amount of tokens to transfer                                                      |

#### viewProtocolFee[​](broken-reference) <a href="#viewprotocolfee" id="viewprotocolfee"></a>

```
function viewProtocolFee() external view returns (uint256)
```

Return protocol fee for this strategy

**Returns**[**​**](broken-reference)

| Name        | Type    | Description  |
| ----------- | ------- | ------------ |
| protocolFee | uint256 | protocol fee |
