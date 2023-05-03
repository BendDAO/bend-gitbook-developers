# AuthenticatedProxy

Proxy contract to hold access to assets on behalf of a user (e.g. ERC20 ERC721 approve) and execute calls under particular conditions.

### Methods

#### initialize

```
function initialize(address _owner,address _authorizationManager,address _WETH) external;
```

**Parameters**

| Name                 | Type     | Description                                    |
| -------------------- | -------- | ---------------------------------------------- |
| owner                | address  | address of proxy owner                         |
| authorizationManager | address  | address of AuthorizationManager                |
| WETH                 | address  | address of the WETH ("Wrapped Ether") contract |

#### setRevoke

```
function setRevoke(bool revoke) external
```

**Parameters**

| Name   | Type | Description              |
| ------ | ---- | ------------------------ |
| revoke | bool | whether proxy is revoked |

#### safeTransfer

```
function safeTransfer(address token,address to,uint256 amount) external;
```

**Parameters**

| Name   | Type    | Description                |
| ------ | ------- | -------------------------- |
| token  | address | address of  token          |
| to     | address | address of token recipient |
| amount | uint256 | amount of  token           |

#### delegatecall

```
function delegatecall(address dest, bytes memory data) external returns (bool, bytes memory)
```

**Parameters**

| Name | Type    | Description                      |
| ---- | ------- | -------------------------------- |
| dest | address | address of  delegate call target |
| data | bytes   | data bytes of delegate call      |

**Returns**

| Name | Type  | Description             |
| ---- | ----- | ----------------------- |
| -    | bool  | status of delegate call |
| -    | bytes | result of delegate call |

#### withdrawETH

```
function withdrawETH() external
```

#### withdrawToken

```
function withdrawToken(address token) external
```

**Parameters**

| Name  | Type    | Description      |
| ----- | ------- | ---------------- |
| token | address | address of token |

####

