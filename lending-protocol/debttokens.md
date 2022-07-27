# debtTokens

Debt tokens are interest-accruing tokens that are minted and burned on borrow and repay, representing the debt owed by the token holder.

## ERC20 Methods

Although debt tokens are modeled on the ERC20 standard, they are non-transferrable. Therefore they do not implement any of the standard ERC20 functions relating to transfer() and allowance().

{% hint style="info" %}
balanceOf() will always return the most up to date accumulated debt of the user.
{% endhint %}

{% hint style="info" %}
totalSupply() will always return the most up to date total debt accrued by all protocol users for debt token.
{% endhint %}

## Methods

### UNDERLYING\_ASSET\_ADDRESS

Returns the address of the underlying asset of this debtToken.

### POOL

Returns the address of the lend pool where this debtToken is used.

### scaledBalanceOf

Returns the principal debt balance of user.

### scaledTotalSupply

Returns the scaled total supply of the debt token.

### getScaledUserBalanceAndSupply

Returns the principal balance of the user and principal total supply.
