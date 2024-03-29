# BoundNFT Registry

BoundNFT Registry is the hub of all boundNFT tokens.

The source code can be [found here](https://github.com/BoundNFT/boundnft-protocol), with the latest deployed address listed in the [Deployed Contracts](broken-reference).

## Methods

### allBNFTAssetLength

**function allBNFTAssetLength()** external view returns (uint256)

Query the length of all NFT assets.

### getBNFTAddressesByIndex

**function getBNFTAddressesByIndex(uint256 index)** external view returns (address bNftProxy, address bNftImpl)

Query boundNFT contract address of given index.

### getBNFTAddresses

**function getBNFTAddresses(address nftAsset)** external view returns (address bNftProxy, address bNftImpl)

Query boundNFT contract address of given NFT asset.

| Parameter Name | Type    | Description                         |
| -------------- | ------- | ----------------------------------- |
| nftAsset       | address | The address of the underlying asset |

**Return Values**

| Parameter Name | Type    | Description                            |
| -------------- | ------- | -------------------------------------- |
| bNftProxy      | address | the proxy address of boundNFT          |
| bNftImpl       | address | the implementation address of boundNFT |
