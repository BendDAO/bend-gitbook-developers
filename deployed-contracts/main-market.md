# Main Market

The Bend protocol is an ecosystem of multiple markets, with the first market being the main Bend Market.

{% hint style="info" %}
For contract addresses of other markets, see the side bar under [Deployed Contracts](broken-reference)
{% endhint %}

## Main Contracts

{% tabs %}
{% tab title="Mainnet" %}
| Contract Name            | Address                                                                                                                    |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| LendPoolAddressProvider  | [0x24451F47CaF13B24f4b5034e1dF6c0E401ec0e46](https://etherscan.io/address/0x24451f47caf13b24f4b5034e1df6c0e401ec0e46#code) |
| LendPool                 | [0x70b97A0da65C15dfb0FFA02aEE6FA36e507C2762](https://etherscan.io/address/0x70b97a0da65c15dfb0ffa02aee6fa36e507c2762#code) |
| LendPoolLoan             | [0x5f6ac80CdB9E87f3Cfa6a90E5140B9a16A361d5C](https://etherscan.io/address/0x5f6ac80cdb9e87f3cfa6a90e5140b9a16a361d5c#code) |
| LendPoolConfigurator     | [0x4f694372ced64B8Cf389A04f13E67ac0035A6449](https://etherscan.io/address/0x4f694372ced64b8cf389a04f13e67ac0035a6449#code) |
| LendPoolLiquidator       | [0x154270A5Ec350a9a9c127fEd7787667A7B2cCbA0](https://etherscan.io/address/0x154270a5ec350a9a9c127fed7787667a7b2ccba0#code) |
| ReserveOracle            | [0x16ca3E500dA893cF2EEBb6b401247e68ca5BC072](https://etherscan.io/address/0x16ca3e500da893cf2eebb6b401247e68ca5bc072#code) |
| NFTOracle                | [0x7C2A19e54e48718f6C60908a9Cff3396E4Ea1eBA](https://etherscan.io/address/0x7c2a19e54e48718f6c60908a9cff3396e4ea1eba#code) |
| WETHGateway              | [0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88](https://etherscan.io/address/0x3B968D2D299B895A5Fcf3BBa7A64ad0F566e6F88#code) |
| PunkGateway              | [0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30](https://etherscan.io/address/0xeD01f8A737813F0bDA2D4340d191DBF8c2Cbcf30#code) |
| BendProtocolDataProvider | [0x0B54cDf07D5467012A2D5731c5F87f9c6945bEa9](https://etherscan.io/address/0x0b54cdf07d5467012a2d5731c5f87f9c6945bea9#code) |
| UiPoolDataProvider       | [0x5250cCE48E43AB930e45Cc8E71C87Ca4B51244cf](https://etherscan.io/address/0x5250cCE48E43AB930e45Cc8E71C87Ca4B51244cf)      |
{% endtab %}

{% tab title="Rinkeby" %}
| Contract Name            | Address                                                                                                                       |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| LendPoolAddressProvider  | [0xE55870eBB007a50B0dfAbAdB1a21e4bFcee5299b](https://rinkeby.etherscan.io/address/0xE55870eBB007a50B0dfAbAdB1a21e4bFcee5299b) |
| LendPool                 | [0xa8D0e90bCB533d70067EEc37601fa7D5C5b3F13E](https://rinkeby.etherscan.io/address/0xa8d0e90bcb533d70067eec37601fa7d5c5b3f13e) |
| LendPoolLoan             | [0xbc622a62bAC3B7de0659A0Dc7b50E4d59aF11377](https://rinkeby.etherscan.io/address/0xbc622a62bac3b7de0659a0dc7b50e4d59af11377) |
| LendPoolConfigurator     | [0x97987245f5Cb66c1EF4A1f750eb6865931486Fd6](https://rinkeby.etherscan.io/address/0x97987245f5cb66c1ef4a1f750eb6865931486fd6) |
| LendPoolLiquidator       | [0xC133Cd86FE48344B7ce86eC4368Cc37C3FEfe012](https://rinkeby.etherscan.io/address/0xc133cd86fe48344b7ce86ec4368cc37c3fefe012) |
| ReserveOracle            | [0xEEa5BC7BEB4DD341E8BBa230E22df9CA45f0AE19](https://rinkeby.etherscan.io/address/0xeea5bc7beb4dd341e8bba230e22df9ca45f0ae19) |
| NFTOracle                | [0x04af5eF6100E1025560Be50FF244CB31f60d08c2](https://rinkeby.etherscan.io/address/0x04af5ef6100e1025560be50ff244cb31f60d08c2) |
| WETHGateway              | [0x1aDF8093E66d8A48F97bCf1bA174845Ec013bBE3](https://rinkeby.etherscan.io/address/0x1adf8093e66d8a48f97bcf1ba174845ec013bbe3) |
| PunkGateway              | [0xdf52378727A5B924Cf0eebbA28eB644fc5E9775E](https://rinkeby.etherscan.io/address/0xdf52378727a5b924cf0eebba28eb644fc5e9775e) |
| BendProtocolDataProvider | [0x6fd2b12Ec4aB86d5e74A43F3C76E00f68Eb69cA7](https://rinkeby.etherscan.io/address/0x6fd2b12ec4ab86d5e74a43f3c76e00f68eb69ca7) |
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
| ETH   | Refer to WETH below or [WETH Gateway](../core-protocol/weth-gateway.md#methods)                                       | Refer to WETH below                                                                                                        | Refer to WETH below                                                                                                        |
| WETH  | [0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2](https://etherscan.io/address/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2) | [0xeD1840223484483C0cb050E6fC344d1eBF0778a9](https://etherscan.io/address/0xeD1840223484483C0cb050E6fC344d1eBF0778a9#code) | [0x87ddE3A3f4b629E389ce5894c9A1F34A7eeC5648](https://etherscan.io/address/0x87ddE3A3f4b629E389ce5894c9A1F34A7eeC5648#code) |
{% endtab %}

{% tab title="Rinkeby" %}
| Asset | Underlying Address                                                                                                            | bendToken Address                                                                                                             | debtToken Address                                                                                                             |
| ----- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ETH   | Refer to WETH below or [WETH Gateway](../core-protocol/weth-gateway.md#methods)                                               | Refer to WETH below                                                                                                           | Refer to WETH below                                                                                                           |
| WETH  | [0xaD1908f909B5C5D2B1032a215d611773F26f089F](https://rinkeby.etherscan.io/address/0xaD1908f909B5C5D2B1032a215d611773F26f089F) | [0x1BBcE5469B8BCc5078AE2398476350936d1393Af](https://rinkeby.etherscan.io/address/0x1bbce5469b8bcc5078ae2398476350936d1393af) | [0xe42f3a56F89546a2596b88cff08234c5EEa304b7](https://rinkeby.etherscan.io/address/0xe42f3a56f89546a2596b88cff08234c5eea304b7) |
{% endtab %}
{% endtabs %}

## boundNFT Contracts

The below information can also be programmatically fetched by calling getNftTokensAddresses().

{% tabs %}
{% tab title="Mainnet" %}
| Asset       | Original NFT Address                                                                                                        | boundNFT Address                                                                                                           |
| ----------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| CryptoPunks | Refer to WPUNKS below or [Punk Gateway](../core-protocol/punk-gateway.md#borroweth)                                         | Refer to WPUNKS below                                                                                                      |
| WPUNKS      |  [0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6](https://etherscan.io/address/0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6#code) | [0x6c415673C79b31aCA38669AD9fb5cdb7012C0e8e](https://etherscan.io/address/0x6c415673C79b31aCA38669AD9fb5cdb7012C0e8e#code) |
| BAYC        | [0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d](https://etherscan.io/address/0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d#code)  | [0xDBfD76AF2157Dc15eE4e57F3f942bB45Ba84aF24](https://etherscan.io/address/0xDBfD76AF2157Dc15eE4e57F3f942bB45Ba84aF24#code) |
| DOODLE      | [0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e](https://etherscan.io/address/0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e)       | [0xacD6AB55F6FbA36293a9a920fFcb2f0F3d34967a](https://etherscan.io/address/0xacD6AB55F6FbA36293a9a920fFcb2f0F3d34967a)      |
| COOL CATS   | [0x1A92f7381B9F03921564a437210bB9396471050C](https://etherscan.io/address/0x1A92f7381B9F03921564a437210bB9396471050C)       | [0x64C0841a7B3145b203001d79dAC3B27AE05d774F](https://etherscan.io/address/0x64C0841a7B3145b203001d79dAC3B27AE05d774F)      |
| MAYC        | [0x60E4d786628Fea6478F785A6d7e704777c86a7c6](https://etherscan.io/address/0x60E4d786628Fea6478F785A6d7e704777c86a7c6)       | [0x69f37e419bD1457d2a25ed3f5d418169caAe8D1F](https://etherscan.io/address/0x69f37e419bD1457d2a25ed3f5d418169caAe8D1F)      |
| WOW         | [0xe785E82358879F061BC3dcAC6f0444462D4b5330](https://etherscan.io/address/0xe785E82358879F061BC3dcAC6f0444462D4b5330)       | [0x6FFB3c6cd21E1C0e0Cb0B8D1EDE946d0f41EfaB4](https://etherscan.io/address/0x6FFB3c6cd21E1C0e0Cb0B8D1EDE946d0f41EfaB4)      |
| CloneX      | [0x49cF6f5d44E70224e2E23fDcdd2C053F30aDA28B](https://etherscan.io/address/0x49cF6f5d44E70224e2E23fDcdd2C053F30aDA28B)       | [0xB8bCAFefEBdD846Dc1F262ca4c5546d7D27092A2](https://etherscan.io/address/0xB8bCAFefEBdD846Dc1F262ca4c5546d7D27092A2)      |
| AZUKI       | [0xED5AF388653567Af2F388E6224dC7C4b3241C544](https://etherscan.io/address/0xED5AF388653567Af2F388E6224dC7C4b3241C544)       | [0xd46C8648F2ac4Ce1A1aace620460fbd24F640853](https://etherscan.io/address/0xd46C8648F2ac4Ce1A1aace620460fbd24F640853)      |
| KONGZ       | [0x57a204AA1042f6E66DD7730813f4024114d74f37](https://etherscan.io/address/0x57a204AA1042f6E66DD7730813f4024114d74f37)       | [0x5F2E3C13cF5b8C5EC7D6a7D14534A7a8e1518E92](https://etherscan.io/address/0x5F2E3C13cF5b8C5EC7D6a7D14534A7a8e1518E92)      |
| BAKC        | 0xba30E5F9Bb24caa003E9f2f0497Ad287FDF95623                                                                                  | 0xcF2CC4994Fe9E411A6aDC30d0A11f20CD4D8d2aB                                                                                 |
| TOADZ       | 0x1CB1A5e65610AEFF2551A50f76a87a7d3fB649C6                                                                                  | 0x2A24535c49567301Ec11BE325E3ee3f9BD06B183                                                                                 |
| MEEBITS     | 0x7Bd29408f11D2bFC23c34f18275bBf23bB716Bc7                                                                                  | 0x4DA03759d24CCf01b64a7750Be2905a6c84DDCd1                                                                                 |
| MFER        | 0x79FCDEF22feeD20eDDacbB2587640e45491b757f                                                                                  | 0x963256b76D87959f57763d1Ca4022e406b8d9f46                                                                                 |
{% endtab %}

{% tab title="Rinkeby" %}
| Asset       | Underlying Address                                                                                                                                                                                                                                          | boundNFT Address                                                                                                                   |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| CryptoPunks | <p><a href="https://rinkeby.etherscan.io/address/0x6389ea3cf6de815ba76d7cf4c6db6a7093471bcb#code">0x6389eA3Cf6dE815ba76d7Cf4C6Db6A7093471bcb</a>, </p><p>Refer to WPUNKS below or <a href="../core-protocol/punk-gateway.md#borroweth">Punk Gateway</a></p> | Refer to WPUNKS below                                                                                                              |
| WPUNKS      | [0x74e4418A41169Fb951Ca886976ccd8b36968c4Ab](https://rinkeby.etherscan.io/address/0x74e4418A41169Fb951Ca886976ccd8b36968c4Ab#code)                                                                                                                          | [0x8894215794f196018324d191a03ef987A617eb01](https://rinkeby.etherscan.io/address/0x8894215794f196018324d191a03ef987a617eb01#code) |
| BAYC        | [0x588D1a07ccdb224cB28dCd8E3dD46E16B3a72b5e](https://rinkeby.etherscan.io/address/0x588d1a07ccdb224cb28dcd8e3dd46e16b3a72b5e#code)                                                                                                                          | [0x7fE857748dc8e335E3E94cAFE27a63d1F573dF45](https://rinkeby.etherscan.io/address/0x7fe857748dc8e335e3e94cafe27a63d1f573df45#code) |
| DOODLE      | [0x10cACFfBf3Cdcfb365FDdC4795079417768BaA74](https://rinkeby.etherscan.io/address/0x10cacffbf3cdcfb365fddc4795079417768baa74)                                                                                                                               | [0xc305b869f94A4380AAa8682796074fd03526D809](https://rinkeby.etherscan.io/address/0xc305b869f94a4380aaa8682796074fd03526d809#code) |
| COOL        | [0x1F912E9b691858052196F11Aff9d8B6f89951AbD](https://rinkeby.etherscan.io/address/0x1f912e9b691858052196f11aff9d8b6f89951abd#code)                                                                                                                          | [0xaf9c744f59256Be4636Ce3e872fbEa861A0bE5B5](https://rinkeby.etherscan.io/address/0xaf9c744f59256be4636ce3e872fbea861a0be5b5#code) |
| MAYC        | [0x9C235dF4053a415f028b8386ed13ae8162843a6e](https://rinkeby.etherscan.io/address/0x9c235df4053a415f028b8386ed13ae8162843a6e#code)                                                                                                                          | [0x98919EAcC8C0d54269954EE04Bbe19cfDeEa780B](https://rinkeby.etherscan.io/address/0x98919eacc8c0d54269954ee04bbe19cfdeea780b#code) |
{% endtab %}
{% endtabs %}
