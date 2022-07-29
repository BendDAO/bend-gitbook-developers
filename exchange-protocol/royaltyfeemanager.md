# RoyaltyFeeManager

It handles the logic to check and transfer royalty fees (if any).

### View methods <a href="#interface_id_erc2981" id="interface_id_erc2981"></a>

#### INTERFACE\_ID\_ERC2981[​](broken-reference) <a href="#interface_id_erc2981" id="interface_id_erc2981"></a>

```
function INTERFACE_ID_ERC2981() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                   | Type   | Description |
| ---------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC2981 | bytes4 | -           |

#### calculateRoyaltyFeeAndGetRecipient[​](broken-reference) <a href="#calculateroyaltyfeeandgetrecipient" id="calculateroyaltyfeeandgetrecipient"></a>

```
function calculateRoyaltyFeeAndGetRecipient(address collection, uint256 tokenId, uint256 amount) external view returns (address, uint256)
```

Calculate royalty fee and get recipient

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                 |
| ---------- | ------- | --------------------------- |
| collection | address | address of the NFT contract |
| tokenId    | uint256 | tokenId                     |
| amount     | uint256 | amount (price of sale)      |

**Returns**[**​**](broken-reference)

| Name      | Type    | Description                                   |
| --------- | ------- | --------------------------------------------- |
| recipient | address | royalty recipient address                     |
| amount    | uint256 | amount of tokens to transfer to the recipient |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### royaltyFeeRegistry[​](broken-reference) <a href="#royaltyfeeregistry" id="royaltyfeeregistry"></a>

```
function royaltyFeeRegistry() external view returns (contract IRoyaltyFeeRegistry)
```

**Returns**[**​**](broken-reference)

| Name               | Type                         | Description                       |
| ------------------ | ---------------------------- | --------------------------------- |
| royaltyFeeRegistry | contract IRoyaltyFeeRegistry | address of the RoyaltyFeeRegistry |

### Methods <a href="#ownershiptransferred" id="ownershiptransferred"></a>

#### renounceOwnership[​](broken-reference) <a href="#renounceownership" id="renounceownership"></a>

```
function renounceOwnership() external nonpayable
```

_Leaves the contract without owner. It will not be possible to call `onlyOwner` functions anymore. Can only be called by the current owner. NOTE: Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner._

#### transferOwnership[​](broken-reference) <a href="#transferownership" id="transferownership"></a>

```
function transferOwnership(address newOwner) external nonpayable
```

_Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner._

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description              |
| -------- | ------- | ------------------------ |
| newOwner | address | address of the new owner |



### Events <a href="#ownershiptransferred" id="ownershiptransferred"></a>

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |
