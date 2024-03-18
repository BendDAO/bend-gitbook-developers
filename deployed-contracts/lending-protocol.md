# Lending Protocol

The BendDAO lending protocol is an ecosystem of multiple markets, with the first market being the main BendDAO Market on Ethereum.

## Main Contracts

{% tabs %}
{% tab title="Mainnet" %}
<table><thead><tr><th width="309.65499028268664">Contract Name</th><th>Address</th></tr></thead><tbody><tr><td>LendPoolAddressProvider</td><td><a href="https://etherscan.io/address/0x24451f47caf13b24f4b5034e1df6c0e401ec0e46#code">0x24451F47CaF13B24f4b5034e1dF6c0E401ec0e46</a></td></tr><tr><td>WETHGateway</td><td><a href="https://etherscan.io/address/0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88">0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88</a></td></tr><tr><td>PunkGateway</td><td><a href="https://etherscan.io/address/0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30">0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30</a></td></tr><tr><td>BendProtocolDataProvider</td><td>0x3811DA50f55CCF75376C5535562F5b4797822480</td></tr><tr><td>UIPoolDataProvider</td><td>0x132E3E3eC6652299B235A26D601aa9C68806e3FE</td></tr><tr><td>BendProtocolIncentivesController</td><td>0x26FC1f11E612366d3367fc0cbFfF9e819da91C8d</td></tr><tr><td>StakedBUNI</td><td>0x647C509AF2A2b2294bB79fCE12DaEc8e7cf938f7</td></tr><tr><td>Other Contracts</td><td>Using Methods in LendPoolAddressProvider to query them</td></tr></tbody></table>
{% endtab %}

{% tab title="Goerli" %}
| Contract Name                    | Address                                                                                                                      |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| LendPoolAddressProvider          | [0x1cba0A3e18be7f210713c9AC9FE17955359cC99B](https://goerli.etherscan.io/address/0x1cba0A3e18be7f210713c9AC9FE17955359cC99B) |
| WETHGateway                      | [0xB926DD4A16c264F02986B575b546123D5D0bC607](https://goerli.etherscan.io/address/0xB926DD4A16c264F02986B575b546123D5D0bC607) |
| PunkGateway                      | [0xa7076550Ee79DB0320BE98f89D775797D859140c](https://goerli.etherscan.io/address/0xa7076550Ee79DB0320BE98f89D775797D859140c) |
| BendProtocolDataProvider         | 0xeFC513D24D2AC6dA4fF3C6429642DD6C497B0845                                                                                   |
| UIPoolDataProvider               | 0x15073180CA8b933C7a8099e811FFAD0568eAb861                                                                                   |
| BendProtocolIncentivesController | 0x292F693048208184320C01e0C223D624268e5EE7                                                                                   |
| StakedBUNI                       | 0x1f9b18D502d8A406564b0cF4e4B7ad9d4eEb2a52                                                                                   |
| Other Contracts                  | Using Methods in LendPoolAddressProvider to query them                                                                       |
{% endtab %}

{% tab title="Sepolia" %}
[https://github.com/BendDAO/bend-lending-protocol/blob/main/deployments/deployed-contracts-sepolia.json](https://github.com/BendDAO/bend-lending-protocol/blob/main/deployments/deployed-contracts-sepolia.json)
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
| USDT  | 0xdAC17F958D2ee523a2206206994597C13D831ec7                                                                            | [0x9631c79bfd6123a5b53307b6cdfb35f97606f954](https://etherscan.io/address/0x9631c79bfd6123a5b53307b6cdfb35f97606f954)      | 0x02716c55f49a9107467507b82f9889480949afe4                                                                                 |


{% endtab %}

{% tab title="Goerli" %}
<table><thead><tr><th width="150">Asset</th><th width="272">Underlying Address</th><th>bendToken Address</th><th>debtToken Address</th></tr></thead><tbody><tr><td>ETH</td><td>Refer to WETH below</td><td>Refer to WETH below</td><td>Refer to WETH below</td></tr><tr><td>WETH</td><td><a href="https://etherscan.io/address/0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88">0xB4FBF271143F4FBf7B91A5ded31805e42b2208d6</a></td><td>0x57FEbd640424C85b72b4361fE557a781C8d2a509</td><td>0x9aB83A4886dCE3C0c1011f9D248249DD3eF64784</td></tr></tbody></table>
{% endtab %}

{% tab title="Sepolia" %}
<table><thead><tr><th width="150">Asset</th><th width="272">Underlying Address</th><th>bendToken Address</th><th>debtToken Address</th></tr></thead><tbody><tr><td>ETH</td><td>Refer to WETH below</td><td>Refer to WETH below</td><td>Refer to WETH below</td></tr><tr><td>WETH</td><td>0xfFf9976782d46CC05630D1f6eBAb18b2324d6B14</td><td>0xD1E6d2B2D2205Ca77632c831bb8b5e468a270975</td><td>0x9ca8943Fb310d2c06DFB4D27Ea3d566B4bdC0971</td></tr><tr><td>USDT</td><td>0x53cEd787Ba91B4f872b961914faE013ccF8b0236</td><td>0xb8e0FBce4BeCC7f28aAaa074D90d6050f32F0830</td><td>0x6a813E393614dDA1086f6d743739186eA92B3f42</td></tr></tbody></table>
{% endtab %}
{% endtabs %}

## boundNFT Contracts

The below information can also be programmatically fetched by calling getNftTokensAddresses(). Please refer to it [here](boundnft-protocol.md#boundnft-contracts).
