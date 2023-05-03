# Protocol Data Provider

The contract returns some reserves, and NFTs data for the lending protocol, its purpose is to help integrators and developers more easily use the BendDAO Lending Protocol data.

### Methods <a href="#methods" id="methods"></a>

#### getAllReservesTokenDatas <a href="#getallreservestokens" id="getallreservestokens"></a>

Returns an array of all reserve (ERC20) tokens for the current pool, in the form of a TokenData struct consisting of the token symbol and token address.

#### getReserveTokenData

Returns the associated addresses for a reserve (ERC20).

#### getReserveConfigurationData

Returns the configuration data for a reserve asset (ERC20).

#### getReserveData

Returns the associated data for a reserve asset.

#### getUserReserveData

Returns the associated user data for a reserve asset.

#### getAllNftsTokenDatas <a href="#getallreservestokens" id="getallreservestokens"></a>

Returns an array of all NFTs tokens for the current pool, in the form of a TokenData struct consisting of the token symbol and token address.

#### getNftTokenData

Returns the associated addresses for an NFT (ERC721).

#### getNftConfigurationData

Returns the configuration data for an NFT asset (ERC721).

#### getLoanDataByCollateral

Returns the loan data for the collateral (ERC721).

#### getLoanDataByLoanId

Returns the loan data for a loan.

### ABI

The ABI JSON file is [here](https://github.com/BendDAO/bend-lending-protocol/blob/main/abis/BendProtocolDataProvider.json).
