# Punk Gateway

If you need to use CryptoPunks in the protocol, it must first be wrapped into WPUNKS. The WPUNKS Gateway contract is a helper contract to easily wrap and unwrap CryptoPunks as necessary when interacting with the protocol, since only ERC721 is used within protocol interactions.

## Methods

### borrow

**function borrow( address reserveAsset, uint256 amount, uint256 punkIndex, address onBehalfOf, uint16 referralCode )**

Allows users to borrow a specific `amount` of the ERC20 reserve underlying asset, provided that the borrower already own some CryptoPunks collaterals. E.g. User borrows 10000 USDC, receiving the 10000 USDC in his wallet and lock CryptoPunks collateral asset in contract.

| Parameter Name | Type    | Description                                                                                   |
| -------------- | ------- | --------------------------------------------------------------------------------------------- |
| reserveAsset   | address | The address of the underlying asset to borrow                                                 |
| amount         | uint256 | The amount to be borrowed.  Units should decimals of underlying reserve                       |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral                                               |
| OnBehalfOf     | address | The address of the user who will receive the debtTokens and NFT loans representing the borrow |
| referralCode   | uint16  | referral code for our referral program. Use 0 for no referral                                 |

### repay

**function repay(uint256 punkIndex, uint256 amount)**

Repays a borrowed `amount` on a specific punk, burning the equivalent loan owned. E.g. User repays 10000 USDC, burning loan and receives collateral asset.

| Parameter Name | Type    | Description                                     |
| -------------- | ------- | ----------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral |
| amount         | uint256 | The amount to repay                             |

### auction

**function auction(uint256 punkIndex, uint256 bidPrice, address onBehalfOf)**

Auction a un-health punk loan with ERC20 reserve.

| Parameter Name | Type    | Description                                              |
| -------------- | ------- | -------------------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral          |
| bidPrice       | uint256 | The bid price                                            |
| onBehalfOf     | address | The address of the user who will receive the CryptoPunks |

### redeem

**function redeem(uint256 punkIndex, uint256 amount, uint256 bidFine)**

Redeems a un-health CryptoPunks loan with ERC20 reserve.&#x20;

| Parameter Name | Type    | Description                                     |
| -------------- | ------- | ----------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral |
| amount         | uint256 | The amount of repaid debt                       |
| bidFine        | uint256 | The amount of bid fine                          |

### liquidate

**function liquidate(uint256 punkIndex, uint256 amount)**

Liquidates a un-health CryptoPunks loan with ERC20 reserve.

| Parameter Name | Type    | Description                                     |
| -------------- | ------- | ----------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral |
| amount         | uint256 | The extra amount of repaid debt                 |

### borrowETH

**function borrowETH( uint256 amount, uint256 punkIndex, address onBehalfOf, uint16 referralCode )**

Allows users to borrow a specific `amount` of the native ETH, provided that the borrower already own some CryptoPunks collaterals. E.g. User borrows 100 ETH, receiving the 100 ETH in his wallet and lock CryptoPunks collateral asset in contract.

| Parameter Name | Type | Description                                                                                   |
| -------------- | ---- | --------------------------------------------------------------------------------------------- |
| amount         |      | The amount to be borrowed. Units should be 18 decimals.                                       |
| punkIndex      |      | The index of the CryptoPunks used as collateral                                               |
| onBehalfOf     |      | The address of the user who will receive the debtTokens and NFT loans representing the borrow |
| referralCode   |      | referral code for our referral program. Use 0 for no referral                                 |

### repayETH

**function repayETH(uint256 punkIndex, uint256 amount)**

Repays a borrowed `amount` on a specific CryptoPunks with native ETH.

| Parameter Name | Type    | Description                                     |
| -------------- | ------- | ----------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral |
| amount         | uint256 | The amount to repay                             |

### auctionETH

**function auction(uint256 punkIndex, address onBehalfOf)**

Auctions a un-health punk loan with native ETH.

| Parameter Name | Type    | Description                                              |
| -------------- | ------- | -------------------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral          |
| onBehalfOf     | address | The address of the user who will receive the CryptoPunks |

### redeemETH

**function redeemETH(uint256 punkIndex, uint256 amount, uint256 bidFine)**

Redeems a un-health punk loan with native ETH.

| Parameter Name | Type    | Description                                     |
| -------------- | ------- | ----------------------------------------------- |
| punkIndex      | uint256 | The index of the CryptoPunks used as collateral |
| amount         | uint256 | The amount of repaid debt                       |
| bidFine        | uint256 | The amount of bid fine                          |

### liquidateETH

**function liquidateETH(uint256 punkIndex, uint256 amount)**

Liquidates a un-health punk loan with native ETH.

|           |         |                                                 |
| --------- | ------- | ----------------------------------------------- |
| punkIndex | uint256 | The index of the CryptoPunks used as collateral |
| amount    | uint256 | The extra amount of repaid debt                 |
