# Gas Limits

The following table shows the recommended gas limit to set when calling the functions. Note that this is the _safe_ gas limit to set to ensure that the transaction completes, however the transaction may use significantly less than these gas limits.

| Contract | Function  | Recommended Gas Limit |
| -------- | --------- | --------------------- |
| LendPool | deposit   | 250000                |
| LendPool | withdraw  | 300000                |
| LendPool | borrow    | 800000                |
| LendPool | repay     | 350000                |
| LendPool | auction   | 500000                |
| LendPool | redeem    | 200000                |
| LendPool | liquidate | 200000                |
