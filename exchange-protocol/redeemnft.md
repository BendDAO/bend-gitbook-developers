# RedeemNFT

it is used to repay the debt and redeeming the original NFT.

### Methods[​](broken-reference) <a href="#methods" id="methods"></a>

#### beforeCollectionTransfer[​](broken-reference) <a href="#transfernonfungibletoken" id="transfernonfungibletoken"></a>

```
function beforeCollectionTransfer(address token,address from,address to,uint256 tokenId,uint256 amount,bytes memory extra) external returns (bool);D
```

**Parameters**[**​**](broken-reference)

| Name    | Type    | Description                    |
| ------- | ------- | ------------------------------ |
| token   | address | address of the collection      |
| from    | address | address of the sender          |
| to      | address | address of the recipient       |
| tokenId | uint256 | tokenId                        |
| amount  | uint256 | token amount, used for erc1155 |
| extra   | bytes   | extra data from the order      |
