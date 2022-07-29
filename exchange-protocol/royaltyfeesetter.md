# RoyaltyFeeSetter

It is used to allow creators to set royalty parameters in the `RoyaltyFeeRegistry`.

### View methods <a href="#interface_id_erc1155" id="interface_id_erc1155"></a>

#### INTERFACE\_ID\_ERC1155[​](broken-reference) <a href="#interface_id_erc1155" id="interface_id_erc1155"></a>

```
function INTERFACE_ID_ERC1155() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                   | Type   | Description |
| ---------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC1155 | bytes4 | -           |

#### INTERFACE\_ID\_ERC2981[​](broken-reference) <a href="#interface_id_erc2981" id="interface_id_erc2981"></a>

```
function INTERFACE_ID_ERC2981() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                   | Type   | Description |
| ---------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC2981 | bytes4 | -           |

#### INTERFACE\_ID\_ERC721[​](broken-reference) <a href="#interface_id_erc721" id="interface_id_erc721"></a>

```
function INTERFACE_ID_ERC721() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                  | Type   | Description |
| --------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC721 | bytes4 | -           |

#### checkForCollectionSetter[​](broken-reference) <a href="#checkforcollectionsetter" id="checkforcollectionsetter"></a>

```
function checkForCollectionSetter(address collection) external view returns (address, uint8)
```

Check royalty info for collection

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description        |
| ---------- | ------- | ------------------ |
| collection | address | collection address |

**Returns**[**​**](broken-reference)

| Name | Type    | Description                                                                                                                                                                                                 |
| ---- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| -    | address | whether there is a setter (address(0) if not)                                                                                                                                                               |
| -    | uint8   | <p>0: Royalty setter is set in the registry<br>1: ERC2981 and no setter<br>2: setter can be set using owner()<br>3: setter can be set using admin()<br>4: setter cannot be set, nor support for ERC2981</p> |

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
function royaltyFeeRegistry() external view returns (address)
```

**Returns**[**​**](broken-reference)

| Name               | Type    | Description                                |
| ------------------ | ------- | ------------------------------------------ |
| royaltyFeeRegistry | address | address of the RoyaltyFeeRegistry contract |

### Methods <a href="#renounceownership" id="renounceownership"></a>

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

#### updateOwnerOfRoyaltyFeeRegistry[​](broken-reference) <a href="#updateownerofroyaltyfeeregistry" id="updateownerofroyaltyfeeregistry"></a>

```
function updateOwnerOfRoyaltyFeeRegistry(address _owner) external nonpayable
```

Update owner of royalty fee registry

_Can be used for migration of this royalty fee setter contract_

**Parameters**[**​**](broken-reference)

| Name    | Type    | Description              |
| ------- | ------- | ------------------------ |
| \_owner | address | address of the new owner |

#### updateRoyaltyFeeLimit[​](broken-reference) <a href="#updateroyaltyfeelimit" id="updateroyaltyfeelimit"></a>

```
function updateRoyaltyFeeLimit(uint256 _royaltyFeeLimit) external nonpayable
```

Update royalty info for collection

**Parameters**[**​**](broken-reference)

| Name              | Type    | Description                                   |
| ----------------- | ------- | --------------------------------------------- |
| \_royaltyFeeLimit | uint256 | new royalty fee limit (500 = 5%, 1,000 = 10%) |

#### updateRoyaltyInfoForCollection[​](broken-reference) <a href="#updateroyaltyinfoforcollection" id="updateroyaltyinfoforcollection"></a>

```
function updateRoyaltyInfoForCollection(address collection, address setter, address receiver, uint256 fee) external nonpayable
```

Update royalty info for collection

_Can only be called by contract owner (of this)_

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                    |
| ---------- | ------- | ------------------------------ |
| collection | address | address of the NFT contract    |
| setter     | address | address that sets the receiver |
| receiver   | address | receiver for the royalty fee   |
| fee        | uint256 | fee (500 = 5%, 1,000 = 10%)    |

#### updateRoyaltyInfoForCollectionIfAdmin[​](broken-reference) <a href="#updateroyaltyinfoforcollectionifadmin" id="updateroyaltyinfoforcollectionifadmin"></a>

```
function updateRoyaltyInfoForCollectionIfAdmin(address collection, address setter, address receiver, uint256 fee) external nonpayable
```

Update royalty info for collection if admin

_Only to be called if there is no setter address_

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                    |
| ---------- | ------- | ------------------------------ |
| collection | address | address of the NFT contract    |
| setter     | address | address that sets the receiver |
| receiver   | address | receiver for the royalty fee   |
| fee        | uint256 | fee (500 = 5%, 1,000 = 10%)    |

#### updateRoyaltyInfoForCollectionIfOwner[​](broken-reference) <a href="#updateroyaltyinfoforcollectionifowner" id="updateroyaltyinfoforcollectionifowner"></a>

```
function updateRoyaltyInfoForCollectionIfOwner(address collection, address setter, address receiver, uint256 fee) external nonpayable
```

Update royalty info for collection if owner

_Only to be called if there is no setter address_

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                    |
| ---------- | ------- | ------------------------------ |
| collection | address | address of the NFT contract    |
| setter     | address | address that sets the receiver |
| receiver   | address | receiver for the royalty fee   |
| fee        | uint256 | fee (500 = 5%, 1,000 = 10%)    |

#### updateRoyaltyInfoForCollectionIfSetter[​](broken-reference) <a href="#updateroyaltyinfoforcollectionifsetter" id="updateroyaltyinfoforcollectionifsetter"></a>

```
function updateRoyaltyInfoForCollectionIfSetter(address collection, address setter, address receiver, uint256 fee) external nonpayable
```

Update royalty info for collection

_Only to be called if there msg.sender is the setter_

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                    |
| ---------- | ------- | ------------------------------ |
| collection | address | address of the NFT contract    |
| setter     | address | address that sets the receiver |
| receiver   | address | receiver for the royalty fee   |
| fee        | uint256 | fee (500 = 5%, 1,000 = 10%)    |

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
