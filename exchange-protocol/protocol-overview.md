# Protocol Overview

The BendDAO Exchange Protocol repository can be found on [Github here](https://github.com/BendDAO/bend-exchange-protocol).

## Main Contracts

The main contracts in Exchange Protocol and their purposes are:

### BendExchange

The core contract of the Bend exchange, and main entry point into the Exchange Protocol. Most interactions will happen via the BendExchange, including:

* matchAskWithTakerBidUsingETHAndWETH
* matchBidWithTakerAsk
* matchAskWithTakerBid

### AuthorizationManager

Used to register authorized proxy, each user has their own independent proxy.
