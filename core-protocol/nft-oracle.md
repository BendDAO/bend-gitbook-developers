# NFT Oracle

Throughout the Bend Protocol, we require reliable, up to date, and secure price feeds for NFTs. Our proxy price provider contract provides this capability and works by:

1. NFTs floor price are calculated using complicated algorithm, original price data come from well-known NFT marketplace such as OpenSea.
2. The NFT price oracle is currently maintained by the Bend team.
3. In the future, Bend governance mechanisms will manage the selection of sources.

## View Methods

### getAssetPrice

Returns the floor price of the supported NFT asset in ETH wei units (18 decimals).
