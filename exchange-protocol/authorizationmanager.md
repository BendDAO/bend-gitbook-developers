# AuthorizationManager

Used to register authorized proxy, each user has their own independent proxy.

### Methods

#### revoke

```
function revoke() external nopayable
```

#### registerProxy

```
function registerProxy() external returns (address) nopayable
```

**Returns**

| Name  | Type    | Description                 |
| ----- | ------- | --------------------------- |
| proxy | address | address of registered proxy |

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

### View methods <a href="#viewcountwhitelistedcurrencies" id="viewcountwhitelistedcurrencies"></a>

#### proxies

```
function proxies(address owner) external view returns (address)
```

**Parameters**

| Name  | Type    | Description            |
| ----- | ------- | ---------------------- |
| owner | address | address of proxy owner |

**Returns**

| Name  | Type    | Description      |
| ----- | ------- | ---------------- |
| proxy | address | address of proxy |

#### authorizedAddress

```
function authorizedAddress() external view returns (address)
```

**Returns**

| Name              | Type    | Description                    |
| ----------------- | ------- | ------------------------------ |
| authorizedAddress | address | address of authorized contract |

#### WETH[​](https://docs.looksrare.org/developers/exchange/LooksRareExchange#weth) <a href="#weth" id="weth"></a>

```
function WETH() external view returns (address)
```

**Returns**[**​**](https://docs.looksrare.org/developers/exchange/LooksRareExchange#returns-1)

| Name | Type    | Description                                    |
| ---- | ------- | ---------------------------------------------- |
| WETH | address | address of the WETH ("Wrapped Ether") contract |

#### revoked[​](https://docs.looksrare.org/developers/exchange/LooksRareExchange#weth)

```
function revoked() external view returns (bool)
```

**Returns**[**​**](https://docs.looksrare.org/developers/exchange/LooksRareExchange#returns-1)

| Name    | Type | Description                             |
| ------- | ---- | --------------------------------------- |
| revoked | bool | whether AuthorizationManager is revoked |

#### proxyImplemention[​](https://docs.looksrare.org/developers/exchange/LooksRareExchange#weth)

```
function proxyImplemention() external view returns (address)
```

**Returns**[**​**](https://docs.looksrare.org/developers/exchange/LooksRareExchange#returns-1)

| Name              | Type    | Description                   |
| ----------------- | ------- | ----------------------------- |
| proxyImplemention | address | address of proxy implemention |

### Events

#### Revoked

```
event Revoked()
```

