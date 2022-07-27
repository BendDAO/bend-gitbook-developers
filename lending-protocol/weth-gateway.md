# WETH Gateway

If you need to use native ETH in the protocol, it must first be wrapped into WETH. The WETH Gateway contract is a helper contract to easily wrap and unwrap ETH as necessary when interacting with the protocol, since only ERC20 is used within protocol interactions.

The source code can be [found here](https://github.com/BendDAO/bend-protocol/blob/main/contracts/protocol/WETHGateway.sol), with the latest deployed address listed in the [Deployed Contracts](broken-reference).

## Methods

### depositETH

**function depositETH(address onBehalfOf, uint16 referralCode)**

Deposits WETH into the reserve, using native ETH. A corresponding amount of the overlying asset (bTokens) is minted.

| Parameter Name | Type    | Description                                                                   |
| -------------- | ------- | ----------------------------------------------------------------------------- |
| onBehalfOf     | address | The address of the user who will receive the bTokens representing the deposit |
| referralCode   | uint16  | referral code for our referral program. Use 0 for no referral                 |

### withdrawETH

**function withdrawETH(uint256 amount, address to)**

Withdraws the WETH \_reserves of msg.sender.

| Parameter Name | Type    | Description                                        |
| -------------- | ------- | -------------------------------------------------- |
| amount         | uint256 | amount of aWETH to withdraw and receive native ETH |
| to             | address | address of the user who will receive native ETH    |

### borrowETH

**function borrowETH( uint256 amount, address nftAsset, uint256 nftTokenId, address onBehalfOf, uint16 referralCode )**

Borrow WETH, unwraps to ETH and send both the ETH and DebtTokens to msg.sender, via  onBehalf argument in `LendPool.borrow`.

| Parameter Name | Type    | Description                                                                                                                                                                                                                                                |
| -------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| amount         | uint256 | the amount of ETH to borrow                                                                                                                                                                                                                                |
| nftAsset       | address | The address of the underlying NFT used as collateral                                                                                                                                                                                                       |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                                                                                                                                                                                                      |
| onBehalfOf     | address | Address of the user who will receive the loan. Should be the address of the borrower itself calling the function if he wants to borrow against his own collateral, or the address of the credit delegator if he has been given credit delegation allowance |
| referralCode   | uint16  | referral code for our referral program. Use 0 for no referral.                                                                                                                                                                                             |

## repayETH

**function repayETH( address nftAsset, uint256 nftTokenId, uint256 amount )**

Repays a borrow on the WETH reserve, for the specified amount (or for the whole amount, if type(uint256).max is specified).

| Parameter Name | Type    | Description                                                                     |
| -------------- | ------- | ------------------------------------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral                            |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                           |
| amount         | uint256 | the amount to repay, or type(uint256).max if the user wants to repay everything |

### auctionETH

**function auctionETH( address nftAsset, uint256 nftTokenId, address onBehalfOf )**

Auction a borrow on the WETH reserve.

| Parameter Name | Type    | Description                                                                                                                                                                                                                                                |
| -------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral                                                                                                                                                                                                       |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral                                                                                                                                                                                                      |
| onBehalfOf     | address | Address of the user who will receive the loan. Should be the address of the borrower itself calling the function if he wants to borrow against his own collateral, or the address of the credit delegator if he has been given credit delegation allowance |

### redeemETH

**function redeemETH( address nftAsset, uint256 nftTokenId, uint256 amount, uint256 bidFine)**

Redeems a borrow on the WETH reserve.

| Parameter Name | Type    | Description                                           |
| -------------- | ------- | ----------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral  |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral |
| amount         | uint256 | The amount to repay the debt                          |
| bidFine        | uint256 | The amount of bid fine                                |

### liquidateETH

**function liquidateETH( address nftAsset, uint256 nftTokenId, uint256 amount)**

Liquidates a borrow on the WETH reserve.

| Parameter Name | Type    | Description                                           |
| -------------- | ------- | ----------------------------------------------------- |
| nftAsset       | address | The address of the underlying NFT used as collateral  |
| nftTokenId     | uint256 | The token ID of the underlying NFT used as collateral |
| amount         | uint256 | The extra amount to repay the debt                    |
