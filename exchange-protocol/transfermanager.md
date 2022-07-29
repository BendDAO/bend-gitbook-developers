# TransferManager

It selects the NFT transfer manager based on a collection address.

### view methods

#### INTERFACE\_ID\_ERC1155[​](broken-reference) <a href="#interface_id_erc1155" id="interface_id_erc1155"></a>

```
function INTERFACE_ID_ERC1155() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                   | Type   | Description |
| ---------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC1155 | bytes4 | -           |

#### INTERFACE\_ID\_ERC721[​](broken-reference) <a href="#interface_id_erc721" id="interface_id_erc721"></a>

```
function INTERFACE_ID_ERC721() external view returns (bytes4)
```

**Returns**[**​**](broken-reference)

| Name                  | Type   | Description |
| --------------------- | ------ | ----------- |
| INTERFACE\_ID\_ERC721 | bytes4 | -           |

#### TRANSFER\_MANAGER\_ERC1155[​](broken-reference) <a href="#transfer_manager_erc1155" id="transfer_manager_erc1155"></a>

```
function TRANSFER_MANAGER_ERC1155() external view returns (address)
```

**Returns**[**​**](broken-reference)

| Name                       | Type    | Description                           |
| -------------------------- | ------- | ------------------------------------- |
| TRANSFER\_MANAGER\_ERC1155 | address | address of the TransferManagerERC1155 |

#### TRANSFER\_MANAGER\_ERC721[​](broken-reference) <a href="#transfer_manager_erc721" id="transfer_manager_erc721"></a>

```
function TRANSFER_MANAGER_ERC721() external view returns (address)
```

**Returns**[**​**](broken-reference)

| Name                      | Type    | Description                          |
| ------------------------- | ------- | ------------------------------------ |
| TRANSFER\_MANAGER\_ERC721 | address | address of the TransferManagerERC721 |

#### addCollectionTransferManager[​](broken-reference) <a href="#addcollectiontransfermanager" id="addcollectiontransfermanager"></a>

```
function addCollectionTransferManager(address collection, address transferManager) external nonpayable
```

Add a transfer manager for a collection

_It is meant to be used for exceptions only (e.g., CryptoKitties)_

**Parameters**[**​**](broken-reference)

| Name            | Type    | Description                                      |
| --------------- | ------- | ------------------------------------------------ |
| collection      | address | collection address to add specific transfer rule |
| transferManager | address | address of the transfer manager                  |

#### checkTransferForToken[​](broken-reference) <a href="#checktransfermanagerfortoken" id="checktransfermanagerfortoken"></a>

```
function checkTransferForToken(address collection) external view returns (address transferManager)
```

Check the transfer manager for a token

_Support for ERC165 interface is checked AFTER custom implementation_

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description        |
| ---------- | ------- | ------------------ |
| collection | address | collection address |

**Returns**[**​**](broken-reference)

| Name            | Type    | Description                                         |
| --------------- | ------- | --------------------------------------------------- |
| transferManager | address | address of the transfer manager for this collection |

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

### Methods <a href="#removecollectiontransfermanager" id="removecollectiontransfermanager"></a>

#### removeCollectionTransferManager[​](broken-reference) <a href="#removecollectiontransfermanager" id="removecollectiontransfermanager"></a>

```
function removeCollectionTransferManager(address collection) external nonpayable
```

Remove a transfer manager for a collection

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                            |
| ---------- | ------- | -------------------------------------- |
| collection | address | collection address to remove exception |

#### renounceOwnership[​](broken-reference) <a href="#renounceownership" id="renounceownership"></a>

```
function renounceOwnership() external nonpayable
```

_Leaves the contract without owner. It will not be possible to call `onlyOwner` functions anymore. Can only be called by the current owner. NOTE: Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner._

#### transferManagerSelectorForCollection[​](broken-reference) <a href="#transfermanagerselectorforcollection" id="transfermanagerselectorforcollection"></a>

```
function transferManagerSelectorForCollection(address) external view returns (address)
```

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description               |
| ---------- | ------- | ------------------------- |
| collection | address | address of the collection |

**Returns**[**​**](broken-reference)

| Name | Type    | Description                                                        |
| ---- | ------- | ------------------------------------------------------------------ |
| -    | address | transfer selector address (if no exception, it returns address(0)) |

#### transferOwnership[​](broken-reference) <a href="#transferownership" id="transferownership"></a>

```
function transferOwnership(address newOwner) external nonpayable
```

_Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner._

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description              |
| -------- | ------- | ------------------------ |
| newOwner | address | address of the new owner |

### Events <a href="#collectiontransfermanageradded" id="collectiontransfermanageradded"></a>

#### CollectionTransferManagerAdded[​](broken-reference) <a href="#collectiontransfermanageradded" id="collectiontransfermanageradded"></a>

```
event CollectionTransferManagerAdded(address indexed collection, address indexed transferManager)
```

**Parameters**[**​**](broken-reference)

| Name                      | Type    | Description |
| ------------------------- | ------- | ----------- |
| collection `indexed`      | address | -           |
| transferManager `indexed` | address | -           |

#### CollectionTransferManagerRemoved[​](broken-reference) <a href="#collectiontransfermanagerremoved" id="collectiontransfermanagerremoved"></a>

```
event CollectionTransferManagerRemoved(address indexed collection)
```

**Parameters**[**​**](broken-reference)

| Name                 | Type    | Description |
| -------------------- | ------- | ----------- |
| collection `indexed` | address | -           |

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |
