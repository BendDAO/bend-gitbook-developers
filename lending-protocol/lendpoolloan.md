# LendPoolLoan

The NFT loan manager of the protocol, generate unique loan when NFTs are used as collateral in the borrowing, and maintain relationship between NFT and loan.

## View Methods

### borrowerOf

**function borrowerOf(uint256 loanId)**

Returns borrower address of the loan.

### getCollateralLoanId

function getCollateralLoanId(address nftAsset, uint256 nftTokenId)

Returns loan id of the NFT specified.

### getLoanCollateralAndReserve

function getLoanCollateralAndReserve(uint256 loanId)

Returns collateral asset and reserve parameters of the loan.

### getLoanReserveBorrowScaledAmount

function getLoanReserveBorrowScaledAmount(uint256 loanId)

### getLoanReserveBorrowAmount

function getLoanReserveBorrowAmount(uint256 loanId)

### getNftCollateralAmount

function getNftCollateralAmount(address nftAsset)

### getUserNftCollateralAmount

function getUserNftCollateralAmount(address user, address nftAsset)
