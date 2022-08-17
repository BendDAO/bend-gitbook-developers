# Gas Limits

The following table shows the recommended gas limit to set when calling the functions. Note that this is the _safe_ gas limit to set to ensure that the transaction completes, however, the transaction may use significantly less than these gas limits.

| Contract    | Function       | Recommended Gas Limit                            |
| ----------- | -------------- | ------------------------------------------------ |
| LendPool    | deposit        | 300000                                           |
| LendPool    | withdraw       | 200000                                           |
| LendPool    | borrow         | 1000000                                          |
| LendPool    | repay          | 700000                                           |
| LendPool    | auction        | 500000                                           |
| LendPool    | redeem         | 500000                                           |
| LendPool    | liquidate      | 700000                                           |
| LendPool    | batchBorrow    | Token Item number multiply borrow's Gas Limit    |
| LendPool    | batchRepay     | Token Item number multiply repay's Gas Limit     |
| WETHGateway | depositETH     | 350000                                           |
| WETHGateway | withdrawETH    | 400000                                           |
| WETHGateway | borrowETH      | 1000000                                          |
| WETHGateway | repayETH       | 700000                                           |
| WETHGateway | auctionETH     | 550000                                           |
| WETHGateway | redeemETH      | 550000                                           |
| WETHGateway | liquidateETH   | 700000                                           |
| WETHGateway | batchBorrowETH | Token Item number multiply borrowETH's Gas Limit |
| WETHGateway | batchRepayETH  | Token Item number multiply repayETH's Gas Limit  |
| PunkGateway | borrowETH      | 1200000                                          |
| PunkGateway | repayETH       | 900000                                           |
| PunkGateway | auctionETH     | 650000                                           |
| PunkGateway | redeemETH      | 650000                                           |
| PunkGateway | liquidateETH   | 900000                                           |
| PunkGateway | batchBorrowETH | Punk Item number multiply borrowETH's Gas Limit  |
| PunkGateway | batchRepayETH  | Punk Item number multiply repayETH's Gas Limit   |
