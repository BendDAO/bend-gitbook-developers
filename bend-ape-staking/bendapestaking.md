# BendApeStaking

Contract used for pairing the ape & ape coin holder

### Methods <a href="#addcurrency" id="addcurrency"></a>

#### matchWithBakcAndCoin[​](broken-reference)

```
function matchWithBakcAndCoin(
   DataTypes.ApeOffer calldata apeOffer,
   DataTypes.BakcOffer calldata bakcOffer,
   DataTypes.CoinOffer calldata coinOffer
) external
```

Match ape & bakc & coin offers and stake

Parameters[**​**](broken-reference)

| Name      | Type                | Description              |
| --------- | ------------------- | ------------------------ |
| apeOffer  | DataTypes.ApeOffer  | the offer of ape holder  |
| bakcOffer | DataTypes.BakcOffer | the offer of bakc holder |
| coinOffer | DataTypes.CoinOffer | the offer of coin holder |

#### matchWithBakc

```
function matchWithBakc(
    DataTypes.ApeOffer calldata apeOffer, 
    DataTypes.BakcOffer calldata bakcOffer
) external
```

Match ape & bakc offers and stake

Parameters

| Name      | Type                | Description              |
| --------- | ------------------- | ------------------------ |
| apeOffer  | DataTypes.ApeOffer  | the offer of ape holder  |
| bakcOffer | DataTypes.BakcOffer | the offer of bakc holder |

#### matchWithCoin

```
function matchWithCoin(
        DataTypes.ApeOffer calldata apeOffer, 
        DataTypes.CoinOffer calldata coinOffer
) external
```

Match ape & coin offers and stake

Parameters

| Name      | Type                | Description              |
| --------- | ------------------- | ------------------------ |
| apeOffer  | DataTypes.ApeOffer  | the offer of ape holder  |
| coinOffer | DataTypes.CoinOffer | the offer of coin holder |

#### stakeSelf[​](broken-reference) <a href="#renounceownership" id="renounceownership"></a>

```
function stakeSelf(
    address apeCollection,
    uint256 apeTokenId,
    uint256 bakcTokenId,
    uint256 apeCoinAmount
) external 
```

_Stake with own_ assets

Parameters

| Name          | Type    | Description                                                              |
| ------------- | ------- | ------------------------------------------------------------------------ |
| apeCollection | address | the address of ape collection                                            |
| apeTokenId    | uint256 | the token id of ape collection                                           |
| bakcTokenId   | uint256 | the token id of bakc, and should be type(uint256).max if no bakc offered |
| apeCoinAmount | uint256 | the amount of ape coin                                                   |



#### cancelOffers[​](broken-reference) <a href="#transferownership" id="transferownership"></a>

```
function cancelOffers(uint256[] calldata offerNonces) external
```

_Cancel offers on chain_

Parameters[**​**](broken-reference)

| Name        | Type       | Description                              |
| ----------- | ---------- | ---------------------------------------- |
| offerNonces | uint256\[] | the nonce array of offers to be canceled |

### View methods

#### isCancelled

```
function isCancelled(address user, uint256 offerNonce) external view returns (bool)
```

Returns

| Name        | Type | Description                        |
| ----------- | ---- | ---------------------------------- |
| isCancelled | bool | whether the offer cancelled of not |



### &#x20;<a href="#currencyremoved" id="currencyremoved"></a>
