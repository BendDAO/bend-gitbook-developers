# Flash Loans

Flash Loans are special un-collateralized loans that allow the borrowing of an NFT asset, as long as the borrowed NFT is returned before the end of the transaction. There is no real world analogy to Flash Loans, so it requires some basic understanding of how state is managed within blocks in blockchains.

{% hint style="warning" %}
Flash Loans are an advanced concept aimed at developers. You must have a good understanding of Ethereum, programming, and smart contracts to take advantage of them.
{% endhint %}

## Overview

For developers, a helpful mental model to consider when developing your solution:

1. Your contract calls the BoundNFT contract, requesting a Flash Loan of a certain tokens of NFTs using flashLoan().
2. After some sanity checks, the BoundNFT transfers the requested amounts of the NFTs to your contract, then calls executeOperation() on your contract (or another contract that you specify as the \_receiver).
3. Your contract, now holding the flash loaned NFTs, executes any arbitrary operation in its code.&#x20;
4. If you are performing a 'traditional' flash loan, then when your code has finished, you transfer the flash loaned amounts of reserves back to the BoundNFT.
5. The BoundNFT contract updates the relevant details of the NFTs and pulls the flash loaned NFT + fee. If the NFT owing is not available (due to a lack of token or approval), then the transaction is reverted.
6. All of the above happens in 1 transaction (hence in a single Ethereum block).

### Applications of Flash Loans

BoundNFT Flash Loans are already used extensively with Bend for swapping and/or migrating positions.

Other examples in the wild include:

* Airdop for holders who's NFTs have been used as collateral.&#x20;
* Other examples and ideas are listed on our blog here and here.

