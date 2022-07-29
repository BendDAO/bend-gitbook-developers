# Taker order

Bend exchange protocol is built on a hybrid system (off-chain/on-chain), which incorporates off-chain signatures (these are called Maker Orders) and on-chain orders (named Taker Orders). The design is similar to other NFT marketplaces (e.g., OpenSea, Rarible) running on the Ethereum blockchain.

Taker Orders are **executed on-chain** against Maker Orders, which exist off-chain. A taker order is an active order, which triggers an execution against an existing maker order.

Since the execution of a taker order is done on-chain, network gas fees is always paid by the taker user.

Taker Orders are standardized in a Solidity struct named `TakerOrder`.

The `TakerOrder` struct contains 6 distinct parameters:

* `isOrderAsk` - Whether the order is an ask (executing an active order to sell an NFT against a maker bid orders) or a bid (executing an active order to buy an NFT against a maker ask order).
* `taker` — The `msg.sender` address. If the transaction sender tries to execute a taker order with a different address, it will naturally revert.
* `price` — The final price of the order. The price is expressed in BigNumber based on the number of decimals of the "currency". Since the currency is defined in the maker order, it is not defined explicitly in the taker order.
* `tokenId` — The id of the token for the order. For collection orders, this field is used in the execution (for taker ask orders).
* `minPercentageToAsk` —The minimum percentage required to be transferred to the Ask (seller) or the trade is rejected (e.g., 8500 = 85% of the trade price).
* `params` - Can contain additional parameters that are not used for standard orders (e.g., Merkle root... for future advanced order types!).
*   `interceptor`

    This field is only avaiable for ask order and used to execute specific logic before transferring the collection, For BNFT, it is used to repay the debt and redeeming the original NFT.
*   `interceptorExtra`

    Additional parameters when executing interceptor.

#### isOrderAsk[​](broken-reference) <a href="#isorderask" id="isorderask"></a>

Like most exchange marketplaces & protocols (including non-NFT marketplaces), an order can be of two distinct types: Ask or Bid.

In the exchange protocol, `Ask` means the user is selling a NFT whereas `Bid` means the user is buying a NFT (with a fungible currency like WETH).

| Bool  | Description            |
| ----- | ---------------------- |
| true  | Taker order is a `Ask` |
| false | Taker order is a `Bid` |

#### taker[​](broken-reference) <a href="#taker" id="taker"></a>

This is the sender address (`msg.sender`). If the transaction sender tries to execute a taker order with a different address, it reverts.

#### price[​](broken-reference) <a href="#price" id="price"></a>

The price for the order. It is a `uint256` value, which doesn't contain any decimal. [Ethereum does not support float numbers](https://stackoverflow.com/questions/58277234/does-solidity-supports-floating-point-number). Price must be displayed as a number in "BigNumber" formatting.

| Price   | Value displayed in the signature |
| ------- | -------------------------------- |
| 0.1 ETH | 100000000000000000               |
| 1 ETH   | 1000000000000000000              |
| 100 ETH | 100000000000000000000            |

[Converters](https://eth-converter.com/) can be useful to convert WETH (or other assets with **18 decimals**) to wei.

> For strategies such as Dutch Auction, the taker price is used as the final settlement price (and valid only if greater than the current auction price at the timestamp of the block where the taker order is included).

#### tokenId[​](broken-reference) <a href="#tokenid" id="tokenid"></a>

The `tokenId` that the taker is looking to purchase/sell.

> For collection orders, this field is used to determine what item matches the collection (maker) bid.

#### minPercentageToAsk[​](broken-reference) <a href="#minpercentagetoask" id="minpercentagetoask"></a>

The `minPercentageToAsk` protects ask users from potential unexpected changes in royalty fees prior to the trade being matched. It acts as a protection that the trade would revert if a specific percentage of the platform gross price does not go to the ask users when the trade is executed on-chain.

> For instance, if Alice executes an order for her item with `minPercentageToAsk = 8500`. If the protocol fee for the strategy is 2% and the royalty fee is changed to 16% prior to the taker order being minted, the trade would revert since 18% > 15%.

#### params[​](broken-reference) <a href="#params" id="params"></a>

This field is used for additional parameters specific to complex orders that are less frequent (e.g., complex order types). The set of additional parameters is represented as `bytes`, where parameters are concatenated.

#### interceptor

This field is only avaiable for ask order and used to execute specific logic before transferring the collection, For BNFT, it is used to repay the debt and redeeming the original NFT.

#### interceptorExtra

Additional parameters when executing interceptor.
