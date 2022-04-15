# boundNFTs

boundNFTs are promissory-note tokens that are minted and burned upon borrow and repay, representing the NFT used as collateral which owed by the token holder, with same token ID.

The boundNFTs' token is pegged to the token of the corresponding NFT collateral at a 1:1. All tokens owned by the boundNFTs holders can be simply integrate into NFT wallet and social medias.

The source code can be found on [Github here](https://github.com/BendDAO/bend-protocol/blob/main/contracts/protocol/BNFT.sol).

{% hint style="info" %}
For all minting and burning actions, see Borrow() and Repay() methods in the LendPool contract, and createLoan() and repayLoan() methods in the LendPoolLoan.
{% endhint %}

## ERC721 Methods

Although boundNFT tokens are modeled on the ERC721 standard, they are non-transferrable. Therefore they do not implement any of the standard ERC721 functions relating to transfer() and allowance().

## Methods

### mint

**function mint(address to, uint256 tokenId)**

Mints boundNFT token to the user address.

|         |         |                                              |
| ------- | ------- | -------------------------------------------- |
| to      | address | The owner address receive the boundNFT token |
| tokenId | uint256 | The token id of the underlying asset of NFT  |

### burn

**function burn(uint256 tokenId)**

Burns user boundNFT token.

|         |         |                                             |
| ------- | ------- | ------------------------------------------- |
| tokenId | uint256 | The token id of the underlying asset of NFT |

### flashLoan

**function flashLoan( address receiverAddress, uint256\[] calldata nftTokenIds, bytes calldata params )**

Allows smart contracts to access the tokens within one transaction, as long as the tokens taken is returned.

|                 |            |                                                                                                                                                                                                  |
| --------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| receiverAddress | address    | The address of the contract receiving the tokens, implementing the [IFlashLoanReceiver](https://github.com/bendfi/bend-protocol/blob/main/contracts/interfaces/IFlashLoanReceiver.sol) interface |
| nftTokenIds     | uint256\[] | The token ids of the underlying asset                                                                                                                                                            |
| params          | bytes      | Variadic packed params to pass to the receiver as extra information                                                                                                                              |

## View Methods

### minterOf

Returns the owner of the token.
