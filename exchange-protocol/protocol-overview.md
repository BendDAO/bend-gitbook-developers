# Protocol Overview

The BendDAO Exchange Protocol repository can be found on [Github here](https://github.com/BendDAO/bend-exchange-protocol).

## Main Contracts

The main contracts in Exchange Protocol and their purposes are:

### BendExchange

The core contract of the Bend exchange, and main entry point into the Exchange Protocol. Most interactions will happen via the BendExchange, including:

#### matchAskWithTakerBid <a href="#matchaskwithtakerbid" id="matchaskwithtakerbid"></a>

```
function matchAskWithTakerBid(OrderTypes.TakerOrder takerBid, OrderTypes.MakerOrder makerAsk) external 
```

#### matchBidWithTakerAsk <a href="#matchbidwithtakerask" id="matchbidwithtakerask"></a>

```
function matchBidWithTakerAsk(OrderTypes.TakerOrder takerAsk, OrderTypes.MakerOrder makerBid) external nonpayable
```

#### matchAskWithTakerBidUsingETHAndWETH <a href="#matchaskwithtakerbidusingethandweth" id="matchaskwithtakerbidusingethandweth"></a>

```
function matchAskWithTakerBidUsingETHAndWETH(OrderTypes.TakerOrder takerBid, OrderTypes.MakerOrder makerAsk) external payable
```

Trades exist such as a combination of taker/order and bid/ask. here are four primary orders:

* **MakerBid** — a passive order that exists off-chain where the user wishes to acquire a NFT using a specific ERC-20 token.
* **MakerAsk** — a passive order that exists off-chain where the user wishes to sell a NFT for a specific ERC-20 token.
* **TakerBid** — an order that is executed on-chain that matches the `MakerAsk`, e.g., the taker accepts the offer from the maker and buys the NFT for the ERC-20 token specified.
* **TakerAsk** — an order that is executed on-chain that matches the `MakerBid`, e.g., the taker accepts the offer from the maker and sells the NFT for the ERC-20 token specified.

