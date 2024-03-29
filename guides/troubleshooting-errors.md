# Troubleshooting Errors

## Error Codes

In order to reduce gas usage and code size, Bend contracts return numbered errors. If you are making calls to the protocol and receive numbered errors, you can use the reference below to know what is the error. Alternatively, you can also find what the numbers represent by checking the [Errors.sol](https://github.com/BendDAO/bend-protocol/blob/main/contracts/libraries/helpers/Errors.sol).

## Reference Guide

| Error Class               | Error Code(string) | Description                                          |
| ------------------------- | ------------------ | ---------------------------------------------------- |
| Common Errors             | 100                | Caller is not Pool Admin                             |
| Common Errors             | 101                | Caller is not Address Provider                       |
| Common Errors             | 102                | Invalid from balance after transfer                  |
| Common Errors             | 103                | Invalid to balance after transfer                    |
| Math Library Errors       | 200                | Multiplication overflow                              |
| Math Library Errors       | 201                | Addition overflow                                    |
| Math Library Errors       | 202                | Divided by zero                                      |
| Validation & check Errors | 301                | Amount must be greater than 0                        |
| Validation & check Errors | 308                | There is not enough collateral to cover a new borrow |
| Lend Pool Loan Errors     | 484                | Bid price is less than liquidation price             |
| Lend Pool Loan Errors     | 485                | Bid price is less than previous highest price        |
| Lend Pool Loan Errors     | 486                | Redeem duration has ended                            |
| Lend Pool Loan Errors     | 489                | Auction has ended                                    |
| Lend Pool Loan Errors     | 490                | Auction is not end                                   |

