# RoyaltyFeeRegistry

A royalty fee registry for the LooksRare exchange. Any marketplace can use this to implement royalty fees for collections that [do not implement ERC-2981](https://eips.ethereum.org/EIPS/eip-2981).

### View Methods <a href="#owner" id="owner"></a>

#### owner[​](broken-reference) <a href="#owner" id="owner"></a>

```
function owner() external view returns (address)
```

_Returns the address of the current owner._

**Returns**[**​**](broken-reference)

| Name  | Type    | Description                  |
| ----- | ------- | ---------------------------- |
| owner | address | address of the current owner |

#### royaltyFeeInfoCollection[​](broken-reference) <a href="#royaltyfeeinfocollection" id="royaltyfeeinfocollection"></a>

```
function royaltyFeeInfoCollection(address collection) external view returns (address, address, uint256)
```

View royalty info for a collection address

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description        |
| ---------- | ------- | ------------------ |
| collection | address | collection address |

**Returns**[**​**](broken-reference)

| Name      | Type    | Description                                                             |
| --------- | ------- | ----------------------------------------------------------------------- |
| setter    | address | address of the setter (can update the royalty fee info in the registry) |
| recipient | address | address of the recipient (collect the royalty fee)                      |
| fee       | uint256 | fee (e.g., 200 = 2%)                                                    |

#### royaltyFeeLimit[​](broken-reference) <a href="#royaltyfeelimit" id="royaltyfeelimit"></a>

```
function royaltyFeeLimit() external view returns (uint256)
```

**Returns**[**​**](broken-reference)

| Name            | Type    | Description                               |
| --------------- | ------- | ----------------------------------------- |
| royaltyFeeLimit | uint256 | royalty fee limit (500 = 5%, 1,000 = 10%) |

#### royaltyInfo[​](broken-reference) <a href="#royaltyinfo" id="royaltyinfo"></a>

```
function royaltyInfo(address collection, uint256 amount) external view returns (address, uint256)
```

Calculate royalty info for a collection address and a sale gross amount

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description        |
| ---------- | ------- | ------------------ |
| collection | address | collection address |
| amount     | uint256 | amount             |

**Returns**[**​**](broken-reference)

| Name      | Type    | Description                                |
| --------- | ------- | ------------------------------------------ |
| recipient | address | address of the recipient                   |
| amount    | uint256 | amount to be received by royalty recipient |

### Methods <a href="#royaltyfeeinfocollection" id="royaltyfeeinfocollection"></a>

#### renounceOwnership[​](broken-reference) <a href="#royaltyfeeinfocollection" id="royaltyfeeinfocollection"></a>

```
function renounceOwnership() external nonpayable
```

_Leaves the contract without owner. It will not be possible to call `onlyOwner` functions anymore. Can only be called by the current owner. NOTE: Renouncing ownership will leave the contract without an owner, thereby removing any functionality that is only available to the owner._

#### transferOwnership[​](broken-reference) <a href="#royaltyfeeinfocollection" id="royaltyfeeinfocollection"></a>

```
function transferOwnership(address newOwner) external nonpayable
```

_Transfers ownership of the contract to a new account (`newOwner`). Can only be called by the current owner._

**Parameters**[**​**](broken-reference)

| Name     | Type    | Description              |
| -------- | ------- | ------------------------ |
| newOwner | address | address of the new owner |

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

**Parameters**[**​**](broken-reference)

| Name       | Type    | Description                    |
| ---------- | ------- | ------------------------------ |
| collection | address | address of the NFT contract    |
| setter     | address | address that sets the receiver |
| receiver   | address | receiver for the royalty fee   |
| fee        | uint256 | fee (500 = 5%, 1,000 = 10%)    |

#### NewRoyaltyFeeLimit[​](broken-reference) <a href="#newroyaltyfeelimit" id="newroyaltyfeelimit"></a>

```
event NewRoyaltyFeeLimit(uint256 royaltyFeeLimit)
```

**Parameters**[**​**](broken-reference)

| Name            | Type    | Description                                                                         |
| --------------- | ------- | ----------------------------------------------------------------------------------- |
| royaltyFeeLimit | uint256 | upper limit for future updates in the royaltyFee of a collection (e.g., 5000 = 50%) |

#### OwnershipTransferred[​](broken-reference) <a href="#ownershiptransferred" id="ownershiptransferred"></a>

```
event OwnershipTransferred(address indexed previousOwner, address indexed newOwner)
```

**Parameters**[**​**](broken-reference)

| Name                    | Type    | Description                   |
| ----------------------- | ------- | ----------------------------- |
| previousOwner `indexed` | address | address of the previous owner |
| newOwner `indexed`      | address | address of the new owner      |

#### RoyaltyFeeUpdate[​](broken-reference) <a href="#royaltyfeeupdate" id="royaltyfeeupdate"></a>

```
event RoyaltyFeeUpdate(address indexed collection, address indexed setter, address indexed receiver, uint256 fee)
```

**Parameters**[**​**](broken-reference)

| Name                 | Type    | Description          |
| -------------------- | ------- | -------------------- |
| collection `indexed` | address | collection address   |
| setter `indexed`     | address | setter address       |
| receiver `indexed`   | address | receiver address     |
| fee                  | uint256 | fee (e.g., 200 = 2%) |
