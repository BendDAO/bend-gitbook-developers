# Down Payment

## How to integrate the Down Payment page?

We can provide a dedicated down payment page for our partners and partners can put our URL on their NFT buying page.

For example, X2Y2 marketplace has this down payment page URL:

https://www.benddao.xyz/app/liquidity/buy/down-payment/x2y2/{**collectionAddress**}/{**tokenId**}

**collectionAddress**: ERC721 contract address.

**tokenId**: ERC721 Token ID.

If the buyer wants to buy Bored Ape Yacht Club #9012 using a down payment, X2Y2 can navigate the link to the URL:

https://www.benddao.xyz/app/liquidity/buy/down-payment/x2y2/**0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D**/**9012**

## How to integrate the repay page?

Each NFT collection will get a 1:1 mapping boundNFT, etc. Bored Ape Yacht Club has boundBAYC.

After the borrower deposit the original NFT item into the lending pool, the original NFT item owner will become the boundNFT contract address and boundNFT will mint a token to the borrower, this boundNFT item owner is the borrower address.

```javascript
boundNFTContract = orginalNFTList[orignalNFTContract];
if (orignalNFTContract.ownerOf(tokenId) == boundNFTContract
    && boundNFTContract.ownerOf(tokenId) == userWalletAddress) {
    // display repay button and debt amount
    const loanData = uiDataProvider.getSimpleLoansData(bendAddressProvider, orignalNFTContract, tokenId);
    // debt = loanData.totalDebtInReserve
    // navigate to repay page URL
}
```

We have provided smart contract methods to query loan data for NFT items.

Contract: [UiPoolDataProvider](https://etherscan.io/address/0x132E3E3eC6652299B235A26D601aa9C68806e3FE#readContract), Methods definition at [here](https://github.com/BendDAO/bend-lending-protocol/blob/main/contracts/interfaces/IUiPoolDataProvider.sol), ABI JSON file at [here](https://github.com/BendDAO/bend-lending-protocol/blob/main/abis/UiPoolDataProvider.json).

Repay page URL: https://www.benddao.xyz/app/repay/{**collectionAddress**}/{**tokenId**}

**collectionAddress**: ERC721 contract address.

**tokenId**: ERC721 Token ID.

## Which NFT collections are supported?

Please use the UiPoolDataProvider method to query supported NFT addresses.

```javascript
const nftAddresses = uiDataProvider.getNftsList();
```
