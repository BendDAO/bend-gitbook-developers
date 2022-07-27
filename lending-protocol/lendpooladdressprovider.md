# LendPoolAddressProvider

Addresses register of the lending market. This contract is immutable and the address will never change. Also see [Deployed Contracts](broken-reference) section.

{% hint style="info" %}
Whenever the LendPool contract is needed, we recommended you fetch the correct address from the LendPoolAddressesProvider smart contract.
{% endhint %}

## Methods

### getMarketId

Returns the id of the lending market to which this contracts points to.

### getLendPool

Returns the address of the LendPool proxy.

### getLendPoolConfigurator

Returns the address of the LendPoolConfigurator proxy.

### getLendPoolLoan

Returns the address of the LendPooLoan proxy.

### getReserveOracle

Returns the address of the ReserveOracle proxy.

### getNFTOracle

Returns the address of the NFTOracle proxy.

### getBNFTRegistry

Returns the address of the BNFTRegistry proxy.

### getIncentivesController

Returns the address of the BEND token incentives controller proxy.

### getUIDataProvider

Returns the address of the UI pool data provider.

### getBendDataProvider

Returns the address of the Bend Protocol data provider.

### getWalletBalanceProvider

Returns the address of the wallet balance provider.

### getPoolAdmin

Returns the address of the pool administrator.

### getEmergencyAdmin()

Returns the address of the emergency pool administrator.
