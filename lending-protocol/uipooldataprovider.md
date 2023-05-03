# UIPoolDataProvider

This Contract returns an array of all reserves, NFTs, loans, and user data for the lending protocol, used by the BendDAO frontend to display some dashboard data.

## Methods

### getReservesList

`function getReservesList(address provider)`

Returns the list of initialized reserves in the Pool associated with the given `provider`.

### getReservesData

`function getReservesData(address provider)`

Returns the list of aggregated reserves data for all the initialized reserves in the Pool associated with the given `provider`.

### getUserReservesData

`function getUserReservesData(address provider, address user)`

Returns the list of user reserves data for all user reserves in the Pool associated with the given `provider`.

### getNftsList

`function getReservesList(address provider)`

Returns the list of initialized NFTs in the Pool associated with the given `provider`.

### getNftsData

`function getReservesData(address provider)`

Returns the list of aggregated NFTs data for all the initialized reserves in the Pool associated with the given `provider`.

### getUserNftsData

`function getUserReservesData(address provider, address user)`

Returns the list of user NFTs data for all user reserves in the Pool associated with the given `provider`.

### getSimpleReservesData

`function getSimpleReservesData(address provider)`

Returns the list of simple reserve data for all reserves in the Pool associated with the given `provider`.

### getSimpleNftsData

`function getSimpleNftsData(address provider)`

Returns the list of simple NFT data for all NFTs in the Pool associated with the given `provider`.

### getSimpleLoansData

`function getSimpleLoanData(address provider, address[] nftAssets, uint256[] nftTokenIds)`

Returns the list of simple loan data for the specified tokens in the Pool associated with the given `provider`.

## ABI

The ABI JSON file is [here](https://github.com/BendDAO/bend-lending-protocol/blob/main/abis/UiPoolDataProvider.json).
