# LendPool

The LendPool contract is the main contract of the protocol. It exposes all the user-oriented actions that can be invoked using either Solidity or web3 libraries.

If you need development support, join the #developers channel on the [Bend community Discord server](https://discord.gg/H8b6Ynjefx).

{% hint style="info" %}
LendPool methods deposit, borrow, withdraw and repay are only for ERC20 and ERC721, if you want to deposit, withdraw, borrow or repay using native ETH use WETHGateway instead, and if you want to borrow or repay using CryptoPunks as collaterals use PunkGateway.
{% endhint %}

## Methods

### deposit

**function deposit(address asset, uint256 amount, address onBehalfOf, uint16 referralCode)**

Deposits an `amount` of underlying asset into the reserve, receiving in return overlying bTokens. E.g. User deposits 100 USDC and gets in return 100 bUSDC.

| Parameter Name | Type    | Description                                                                                                                  |
| -------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------- |
| asset          | address | The address of the underlying asset to deposit                                                                               |
| amount         | uint256 | The underlying amount to be deposited, expressed in underlying asset decimals units                                          |
| onBehalfOf     | address | <p>address whom will receive the bTokens. <br>Use <code>msg.sender</code> when the aTokens should be sent to the caller.</p> |
| referralCode   | uint16  | referral code for our referral program. Use 0 for no referral.                                                               |

### withdraw

**function withdraw( address asset, uint256 amount, address to )**

Withdraws an `amount` of underlying asset from the reserve, burning the equivalent bTokens owned.&#x20;

| Parameter Name | Type    | Description                                                                                                                                                                      |
| -------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| asset          | address | The address of the underlying asset to deposit                                                                                                                                   |
| amount         | uint256 | The underlying amount to be withdrawn, expressed in underlying asset decimals units                                                                                              |
| to             | address | Address that will receive the underlying, same as msg.sender if the user wants to receive it on his own wallet, or a different address if the beneficiary is a different wallet. |

### borrow

**function borrow( address asset, uint256 amount, address nftAsset, uint256 nftTokenId, address onBehalfOf, uint16 referralCode )**

Allows users to borrow a specific `amount` of the reserve underlying asset. E.g. User borrows 100 USDC, receiving the 100 USDC in his wallet and lock collateral asset in contract.

| Parameter Name | Type    | Description                                                                                                                                                       |
| -------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| asset          | address | The address of the underlying asset to borrow                                                                                                                     |
| amount         | uint256 | The underlying amount to be borrowed, expressed in underlying asset decimals units                                                                                |
| nftAsset       | address | The address of the underlying NFT used as collateral                                                                                                              |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                                                                                                             |
| onBehalfOf     | address | Address of the user who will receive the loan. Should be the address of the borrower itself calling the function if he wants to borrow against his own collateral |
| referralCode   | uint16  | referral code for our referral program. Use 0 for no referral.                                                                                                    |

### repay

**function repay( address nftAsset, uint256 nftTokenId, uint256 amount )**

Repays a borrowed `amount` on a specific reserve, burning the equivalent loan owned. E.g. User repays 100 USDC, burning loan and receives collateral asset.

| Parameter Name | Type    | Description                                                                                                                                                                                                                                                                                                                              |
| -------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral                                                                                                                                                                                                                                                                                     |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                                                                                                                                                                                                                                                                                    |
| amount         | uint256 | The underlying amount to be repaid, expressed in underlying asset decimals units.Use type(uint256).max to repay the entire debt, ONLY when the repayment is not executed on behalf of a 3rd party. In case of repayments on behalf of another user, it's recommended to send an amount slightly higher than the current borrowed amount. |

**Return Values**

| Parameter Name | Type    | Description                                                                 |
| -------------- | ------- | --------------------------------------------------------------------------- |
| repaidAmount   | uint256 | The underlying payback amount repaid                                        |
| isBurnLoan     | bool    | The loan is burned or not, return true if all borrowed debt has been repaid |

### auction

**function auction( address nftAsset, uint256 nftTokenId, uint256 bidPrice, address onBehalfOf )**

Function to auction a non-healthy position collateral-wise. The caller (liquidator) want to buy collateral asset of the user getting liquidated. Auction mechanism in Bend is English Auction, the highest bidder will be the winner.&#x20;

| Parameter Name | Type    | Description                                                                                                                                                                                          |
| -------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral                                                                                                                                                 |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                                                                                                                                                |
| bidPrice       | uint256 | The bid price of the liquidator want to buy the underlying NFT                                                                                                                                       |
| onBehalfOf     | address | Address of the user who will get the underlying NFT, same as msg.sender if the user wants to receive them on his own wallet, or a different address if the beneficiary of NFT is a different wallet. |

### redeem

function redeem(address nftAsset, uint256 nftTokenId, uint256 bidFine)

Function to redeem a non-healthy NFT loan which state is in Auction. The caller must be borrower of loan. The borrower can redeem his own things before the redemption time expires.

| Parameter Name | Type    | Description                                           |
| -------------- | ------- | ----------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral  |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral |
| amount         | uint256 | The amount to repay the debt                          |
| bidFine        | uint256 | The amount of bid fine                                |

**Return Values**

| Parameter Name | Type    | Description                          |
| -------------- | ------- | ------------------------------------ |
| repayAmount    | uint256 | The underlying payback amount repaid |

### liquidate

**function liquidate( address nftAsset, uint256 nftTokenId, address onBehalfOf )**

Function to liquidate a non-healthy NFT loan which state is in Auction. The caller (liquidator) buy collateral asset of the user getting liquidated, and receives the collateral asset.

| Parameter Name | Type    | Description                                                     |
| -------------- | ------- | --------------------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral            |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral           |
| amount         | uint256 | The extra amount to repay debt. It should be 0 in most of case. |

**Return Values**

| Parameter Name | Type    | Description                        |
| -------------- | ------- | ---------------------------------- |
| extraAmount    | uint256 | The underlying extra amount repaid |

## View Methods

### getReservesList

**function getReservesList()**

Returns the underlying address list of the initialized reserves.

### getReserveData

**function getReserveData(address asset)**

Returns the state and configuration of the reserve.

**Return Values**

| Parameter Name            | Type                    | Description                                        |
| ------------------------- | ----------------------- | -------------------------------------------------- |
| configuration             | ReserveConfigurationMap | the reserve configuration                          |
| liquidityIndex            | uint128                 | the liquidity index. Expressed in ray              |
| variableBorrowIndex       | uint128                 | variable borrow index. Expressed in ray            |
| currentLiquidityRate      | uint128                 | the current supply rate. Expressed in ray          |
| currentVariableBorrowRate | uint128                 | the current variable borrow rate. Expressed in ray |
| lastUpdateTimestamp       | uint40                  |                                                    |
| bTokenAddress             | address                 | bToken addresses of reserve                        |
| debtTokenAddress          | address                 | debtToken addresses of reserve                     |
| interestRateAddress       | address                 | address of the interest rate strategy              |

### getReserveConfiguration

**function getReserveConfiguration(address asset)**

Returns the configuration of the reserve.

### getReserveNormalizedIncome

_function getReserveNormalizedIncome(address asset)_

Returns the normalized income normalized income of the reserve.

### getReserveNormalizedVariableDebt

function getReserveNormalizedVariableDebt(address asset)

Returns the normalized variable debt per unit of asset**.**

### getNftsList

**function getNftsList()**

Returns the underlying address list of the initialized NFTs.

### getNftData

**function getNftData(address asset)**

Returns the state and configuration of the nft.

### getNftConfiguration

**function getNftConfiguration(address asset)**

Returns the configuration of the NFT.

### getNftLoanData

**function getNftLoanData(address nftAsset, uint256 nftTokenId)**

Returns the loan data of the NFT.

**Return Values**

| Parameter Name       | Type    | Description                                               |
| -------------------- | ------- | --------------------------------------------------------- |
| totalCollateralETH   | uint256 | the total collateral in ETH of the NFT                    |
| totalDebtETH         | uint256 | the total borrowed debt in ETH of the NFT                 |
| availableBorrowsETH  | uint256 | the borrowing power left of the NFT                       |
| ltv                  | uint256 | the loan to value of the user,  that is collateral ration |
| liquidationThreshold | uint256 | the liquidation threshold of the NFT                      |
| loanId               | uint256 | the loan id of the NFT related to                         |
| healthFactor         | uint256 | the current health factor of the NFT                      |
| reserveAsset         | address | the current borrowed reserve asset of the NFT             |

### getNftAuctionData

**function getNftAuctionData(address nftAsset, uint256 nftTokenId)**

Returns the auction data of the NFT.

**Return Values**

| Parameter Name  | Type    | Description                                  |
| --------------- | ------- | -------------------------------------------- |
| loanId          | uint256 | the loan id of the NFT                       |
| bidderAddres    | address | the highest bidder address of the loan       |
| bidPrice        | uint256 | the highest bid price in Reserve of the loan |
| bidBorrowAmount | uint256 | the borrow amount in Reserve of the loan     |
| bidFine         | uint256 | the penalty fine of the loan                 |

### getNftLiquidatePrice

Returns the liquidate price of the NFT which health factor is below 1.

### getNftCollateralData

**function getNftCollateralData(address nftAsset, address reserveAsset)**

Returns the collateral data of the NFT.

**Return Values**

| Parameter Name            | Type    | Description                                |
| ------------------------- | ------- | ------------------------------------------ |
| totalCollateralInETH      | uint256 | the total collateral in ETH of the NFT     |
| totalCollateralInReserve  | uint256 | the total collateral in Reserve of the NFT |
| availableBorrowsInETH     | uint256 | the borrowing power in ETH of the NFT      |
| availableBorrowsInReserve | uint256 | the borrowing power in Reserve of the NFT  |
| ltv                       | uint256 | the loan to value of the user              |
| liquidationThreshold      | uint256 | the liquidation threshold of the NFT       |
| liquidationBonus          | uint256 | the liquidation bonus of the NFT           |

###

### paused

Returns true if the LendPool is paused
