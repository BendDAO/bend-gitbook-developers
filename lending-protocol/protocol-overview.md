# Protocol Overview

The BendDAO Lending Protocol repository can be found on [Github here](https://github.com/BendDAO/bend-protocol).

## Main Contracts

{% hint style="info" %}
Both LendPoolAddressesProvider and LendPoolAddressesProviderRegistry control the upgradeability of the protocol, including reserves and NFTs listings and changes to protocol parameters. BEND holders will be in control of both, via BendDAO Governance.
{% endhint %}

The main contracts in BendDAO and their purposes are:

### LendPool

The main entry point into the Bend Protocol. Most interactions with Bend will happen via the LendPool, including:

* deposit
* withdraw
* borrow
* repay
* auction
* redeem
* liquidate

### LendPoolLoan

The NFT loan manager of the protocol, generate unique loan when NFTs are used as collateral in the borrowing, and maintain relationship between NFT and loan.

### LendPoolAddressesProvider

The main addresses register of the protocol, for particular markets. The latest contract addresses should be retrieved from this contract by making the appropriate calls.

### LendPoolAddressesProviderRegistry

Contains a list of active LendPoolAddressesProvider addresses, for different markets.

### bTokens

The interest bearing, tokenized deposits used throughout the Bend protocol. They implement most of the standard ERC20 token methods with slight modifications, as well as Bend specific methods including:

* scaledBalanceOf
* scaledTotalSupply
* getScaledUserBalanceAndSupply

### debtTokens

The tokenized borrow positions used throughout the Bend protocol. Most of the standard ERC20 methods are disabled, since debt tokens are non-transferrable.

### boundNFTs

The promissory note, tokenized collaterals used throughout the Bend protocol. Most of the standard ERC721 methods are disabled, since boundNFT tokens are non-transferrable.

## Supporting Contracts

The following contracts should generally not be interacted with directly, but are used throughout the Bend Protocol via contract calls.

### Lend Pool Configurator

Provides configuration functions for the LendPool contracts. It also has a number of important functions:

* Activates / Deactivates reserves,&#x20;
* Enables / Disables borrowing for a reserve,&#x20;
* Freezes / Unfreezes reserves,&#x20;
* Updates a reserve's decimals,
* Updates a reserve's interest rate strategy address,&#x20;
* Activates / Deactivates NFT collections,
* Freezes / Unfreezes NFT collections,
* Enables / Disables using a NFT collection as collateral,&#x20;
* Updates a NFT collection's Loan to Value,&#x20;
* Updates a NFT collection's liquidation threshold,&#x20;
* Updates a NFT collection's liquidation bonus, &#x20;
* Activates / Deactivates all functions of a LendPool in emergencies.&#x20;

For all of the above functions, relevant events are emitted to the blockchain. Anyone can monitor these changes to know when values have been modified or added/removed.

### Interest Rate Strategy

Holds the information needed to calculate and update the interest rates of specific reserves. Each contract stores the optimized base curves using the corresponding parameters of each currency. This means that there is a mathematical function which determines the interest rate of each asset pool, with the interest rate changing based on the amount of borrowed funds and the total liquidity (i.e. utilization) of the asset pool. The parameters for the optimized base curves are:&#x20;

* baseVariableBorrowRate
* variableRateSlope1
* variableRateSlope2

The interest rates are calculated depending on the available liquidity and the total borrowed amount.

### Price Oracle Provider

Provides reserves and NFTs asset price data required throughout the Bend protocol, using Chainlink and a fallback when necessary. More details [on the page](nft-oracle.md).

### Library Contracts

Various libraries are also used throughout the Bend Protocol, which can be found on our [Github here](https://github.com/BendDAO/bend-protocol/tree/main/contracts/libraries).
