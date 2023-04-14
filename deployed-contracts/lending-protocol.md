# Lending Protocol

The BendDAO lending protocol is an ecosystem of multiple markets, with the first market being the main BendDAO Market on Ethereum.

## Main Contracts

{% tabs %}
{% tab title="Mainnet" %}
| Contract Name           | Address                                                                                                                    |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| LendPoolAddressProvider | [0x24451F47CaF13B24f4b5034e1dF6c0E401ec0e46](https://etherscan.io/address/0x24451f47caf13b24f4b5034e1df6c0e401ec0e46#code) |
| WETHGateway             | [0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88](https://etherscan.io/address/0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88)      |
| PunkGateway             | [0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30](https://etherscan.io/address/0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30)      |
| Other Contracts         | Using Methods in LendPoolAddressProvider to query them                                                                     |
{% endtab %}

{% tab title="Goerli" %}
| Contract Name           | Address                                                                                                                      |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| LendPoolAddressProvider | [0x1cba0A3e18be7f210713c9AC9FE17955359cC99B](https://goerli.etherscan.io/address/0x1cba0A3e18be7f210713c9AC9FE17955359cC99B) |
| WETHGateway             | [0xB926DD4A16c264F02986B575b546123D5D0bC607](https://goerli.etherscan.io/address/0xB926DD4A16c264F02986B575b546123D5D0bC607) |
| PunkGateway             | [0xa7076550Ee79DB0320BE98f89D775797D859140c](https://goerli.etherscan.io/address/0xa7076550Ee79DB0320BE98f89D775797D859140c) |
| Other Contracts         | Using Methods in LendPoolAddressProvider to query them                                                                       |
{% endtab %}
{% endtabs %}

{% hint style="info" %}
For governance related contracts, see the [Voting & Governance](../protocol-governance/voting-and-governance.md) section.
{% endhint %}

## bendToken Contracts

The below information can also be programmatically fetched by calling getReserveTokensAddresses(). All tokens use 18 decimals, unless indicated otherwise.

{% tabs %}
{% tab title="Mainnet" %}
| Asset | Original Reserve Address                                                                                              | bendToken Address                                                                                                          | debtToken Address                                                                                                          |
| ----- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| ETH   | Refer to WETH below or [WETH Gateway](../lending-protocol/weth-gateway.md#methods)                                    | Refer to WETH below                                                                                                        | Refer to WETH below                                                                                                        |
| WETH  | [0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2](https://etherscan.io/address/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2) | [0xeD1840223484483C0cb050E6fC344d1eBF0778a9](https://etherscan.io/address/0xeD1840223484483C0cb050E6fC344d1eBF0778a9#code) | [0x87ddE3A3f4b629E389ce5894c9A1F34A7eeC5648](https://etherscan.io/address/0x87ddE3A3f4b629E389ce5894c9A1F34A7eeC5648#code) |
{% endtab %}

{% tab title="Goerli" %}
| Asset | Underlying Address                                                                                                    | bendToken Address                          | debtToken Address                          |
| ----- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------ |
| ETH   | Refer to WETH below                                                                                                   | Refer to WETH below                        | Refer to WETH below                        |
| WETH  | [0xB4FBF271143F4FBf7B91A5ded31805e42b2208d6](https://etherscan.io/address/0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88) | 0x57FEbd640424C85b72b4361fE557a781C8d2a509 | 0x9aB83A4886dCE3C0c1011f9D248249DD3eF64784 |
{% endtab %}
{% endtabs %}

## boundNFT Contracts

The below information can also be programmatically fetched by calling getNftTokensAddresses(). Please refer to it [here](boundnft-protocol.md#boundnft-contracts).
