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

The below information can also be programmatically fetched by calling getNftTokensAddresses().

{% tabs %}
{% tab title="Mainnet" %}
| Asset       | Original NFT Address                                                                                                        | boundNFT Address                                                                                                           |
| ----------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| CryptoPunks | Refer to WPUNKS below or [Punk Gateway](../lending-protocol/punk-gateway.md#borroweth)                                      | Refer to WPUNKS below                                                                                                      |
| WPUNKS      |  [0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6](https://etherscan.io/address/0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6#code) | [0x6c415673C79b31aCA38669AD9fb5cdb7012C0e8e](https://etherscan.io/address/0x6c415673C79b31aCA38669AD9fb5cdb7012C0e8e#code) |
| BAYC        | [0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d](https://etherscan.io/address/0xbc4ca0eda7647a8ab7c2061c2e118a18a936f13d#code)  | [0xDBfD76AF2157Dc15eE4e57F3f942bB45Ba84aF24](https://etherscan.io/address/0xDBfD76AF2157Dc15eE4e57F3f942bB45Ba84aF24#code) |
| DOODLE      | [0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e](https://etherscan.io/address/0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e)       | [0xacD6AB55F6FbA36293a9a920fFcb2f0F3d34967a](https://etherscan.io/address/0xacD6AB55F6FbA36293a9a920fFcb2f0F3d34967a)      |
| SDOODLE     | 0x620b70123fb810f6c653da7644b5dd0b6312e4d8                                                                                  | 0x8D395BeC6573a0B0D556639B38Ed8C87f18E6fE0                                                                                 |
| MAYC        | [0x60E4d786628Fea6478F785A6d7e704777c86a7c6](https://etherscan.io/address/0x60E4d786628Fea6478F785A6d7e704777c86a7c6)       | [0x69f37e419bD1457d2a25ed3f5d418169caAe8D1F](https://etherscan.io/address/0x69f37e419bD1457d2a25ed3f5d418169caAe8D1F)      |
| CloneX      | [0x49cF6f5d44E70224e2E23fDcdd2C053F30aDA28B](https://etherscan.io/address/0x49cF6f5d44E70224e2E23fDcdd2C053F30aDA28B)       | [0xB8bCAFefEBdD846Dc1F262ca4c5546d7D27092A2](https://etherscan.io/address/0xB8bCAFefEBdD846Dc1F262ca4c5546d7D27092A2)      |
| AZUKI       | [0xED5AF388653567Af2F388E6224dC7C4b3241C544](https://etherscan.io/address/0xED5AF388653567Af2F388E6224dC7C4b3241C544)       | [0xd46C8648F2ac4Ce1A1aace620460fbd24F640853](https://etherscan.io/address/0xd46C8648F2ac4Ce1A1aace620460fbd24F640853)      |
| Moonbirds   | 0x23581767a106ae21c074b2276d25e5c3e136a68b                                                                                  | 0x4117417a2EbA58766501A1968e2cc1321d50f698                                                                                 |
| COOL CATS   | [0x1A92f7381B9F03921564a437210bB9396471050C](https://etherscan.io/address/0x1A92f7381B9F03921564a437210bB9396471050C)       | [0x64C0841a7B3145b203001d79dAC3B27AE05d774F](https://etherscan.io/address/0x64C0841a7B3145b203001d79dAC3B27AE05d774F)      |
| WOW         | [0xe785E82358879F061BC3dcAC6f0444462D4b5330](https://etherscan.io/address/0xe785E82358879F061BC3dcAC6f0444462D4b5330)       | [0x6FFB3c6cd21E1C0e0Cb0B8D1EDE946d0f41EfaB4](https://etherscan.io/address/0x6FFB3c6cd21E1C0e0Cb0B8D1EDE946d0f41EfaB4)      |
| KONGZ       | [0x57a204AA1042f6E66DD7730813f4024114d74f37](https://etherscan.io/address/0x57a204AA1042f6E66DD7730813f4024114d74f37)       | [0x5F2E3C13cF5b8C5EC7D6a7D14534A7a8e1518E92](https://etherscan.io/address/0x5F2E3C13cF5b8C5EC7D6a7D14534A7a8e1518E92)      |
| BAKC        | 0xba30E5F9Bb24caa003E9f2f0497Ad287FDF95623                                                                                  | 0xcF2CC4994Fe9E411A6aDC30d0A11f20CD4D8d2aB                                                                                 |
| Otherdeed   | 0x34d85c9CDeB23FA97cb08333b511ac86E1C4E258                                                                                  | 0x59BF54AfB69260189Fe954263229617317141053                                                                                 |
| TOADZ       | 0x1CB1A5e65610AEFF2551A50f76a87a7d3fB649C6                                                                                  | 0x2A24535c49567301Ec11BE325E3ee3f9BD06B183                                                                                 |
| MEEBITS     | 0x7Bd29408f11D2bFC23c34f18275bBf23bB716Bc7                                                                                  | 0x4DA03759d24CCf01b64a7750Be2905a6c84DDCd1                                                                                 |
| MFER        | 0x79FCDEF22feeD20eDDacbB2587640e45491b757f                                                                                  | 0x963256b76D87959f57763d1Ca4022e406b8d9f46                                                                                 |
{% endtab %}

{% tab title="Goerli" %}
| Asset       | Underlying Address                         | boundNFT Address                           |
| ----------- | ------------------------------------------ | ------------------------------------------ |
| CryptoPunks | 0xbeD1e8B430FD512b82A18cb121a8442F3889E505 | Refer to WPUNKS below                      |
| WPUNKS      | 0xbeD1e8B430FD512b82A18cb121a8442F3889E505 | 0x83f90CF9c281636a0128614EA043b5d8Ccd380fa |
| BAYC        | 0x30d190032A34d6151073a7DB8793c01Aa05987ec | 0x529710d1e2ab61bDea707039bB841583A983b228 |
| DOODLE      | 0x317e19Fe3DB508f1A45421379FBbd7564d0259c0 | 0xF0CB11A532ff2401B783a14Cf50344a0E04D25B4 |
| SDOODLE     | 0x82C348Ef21629f5aaeE5280ef3f4389Ad82F8799 | 0x7Dc59D9395b6Fa436CE49d643BcF517A376E0A1C |
| MAYC        | 0x15596C27900e12A9cfC301248E21888751f61c19 | 0xe7BD47E781e8758420Df9992ADD1f5ab31555fF7 |
| CloneX      | 0x578bc56a145A3464Adc44635C23501653138c946 | 0x27F9996c228eE3A85AC898d49A3eFaAaDC44D1e6 |
| Azuki       | 0x708c48AaA4Ea8B9E46Bd8DEb6470986842b9a16d | 0x302cE2Ddf378CaAabB990662aFdA1488b13Fc1B0 |
| Moonbirds   | 0x784E3FcfC86F7806f52a24571d8534c916C8c609 | 0x8A291a0e671EDAcb76224A1fD933e332BCc981D8 |
{% endtab %}
{% endtabs %}
