# Reserves Oracle

Throughout the Bend Protocol, we require reliable, up to date, and secure price feeds for reserves. Our proxy price provider contract provides this capability and works by:

1. First checking for a price from a Chainlink aggregator.
2. If the price is below or equal to zero, we call our fallback price oracle.​The fallback price oracle is currently maintained by the Bend team.
3. In the future, Bend governance mechanisms will manage the selection of sources and the fallback price oracle.

## View Methods

### getAssetPrice

Returns the price of the supported reserve asset in ETH wei units (18 decimals).
