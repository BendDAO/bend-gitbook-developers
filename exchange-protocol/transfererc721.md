# TransferERC721

It allows the transfer of ERC-721 tokens by the BendExchange.

### Methods[​](broken-reference) <a href="#methods" id="methods"></a>

#### transferNonFungibleToken[​](broken-reference) <a href="#transfernonfungibletoken" id="transfernonfungibletoken"></a>

```
function transferNonFungibleToken(address token, address from, address to, uint256 tokenId, uint256) external nonpayable
```

Transfer ERC721 token

_For ERC721, amount is not used_

**Parameters**[**​**](broken-reference)

| Name    | Type    | Description               |
| ------- | ------- | ------------------------- |
| token   | address | address of the collection |
| from    | address | address of the sender     |
| to      | address | address of the recipient  |
| tokenId | uint256 | tokenId                   |
| -       | uint256 | -                         |
