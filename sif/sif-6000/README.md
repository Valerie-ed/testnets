# sif-6000 task

## sif-6000 Task List

### Basic Tasks

| #    | Tasks                  | Details                                                        |Proof                                                           | Score |
| ---- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | Run a full node          | Run a full node, join testnet, and create six wallets (named Wallet A / B / C / D / E / F ,[doc](https://github.com/hashgard/testnets/blob/develop/docs/README.md) | submit nodes IP, and ensure that the corresponding port is accessible, the default is 26657 port, http://${your_ip}:26657/status | 200  |
| 2    | Get the test token from the faucet | Get GARD and apple from faucet to wallet A and wallet B ,see```hashgardcli keys --help``` | Submit two transaction tx                                              | 100  |
| Total |                          |                                                              |                                                              | 300  |





### Delegation Tasks

| #    | Tasks   | Details                                                         | Proof            | Score |
| ---- | ---------- | ------------------------------------------------------------ | --------------- | ---- |
| 3    | Become a validator | Send a transaction to apply to be a validator with Wallet A (make sure you have created a wallet and got test tokens before this step) [doc](https://github.com/hashgard/testnets/blob/develop/docs/create-validator.md) | Submit validator address | 200  |
| 4    | Delegation       | Delegate 10 GARD to the validator you created with Wallet B ,[doc](https://github.com/hashgard/testnets/blob/develop/docs/delegate.md) | Submit transaction tx | 100  |
| 5    | Redelegate   | With Wallet B, tranfer the 10 GARD you delegated to your own validator to the official validator(gardvaloper13fn2v2rstszureanek9aqvev6z8hzx0hty77wj) with redelegate function,[doc](https://github.com/hashgard/testnets/blob/develop/docs/redelegate.md) | Submit transaction tx | 100  |
| 6    | Cancel delegation  | With Wallet B, get the 10 GARD back from official validator by canceling delegation through unbond function,[doc](https://github.com/hashgard/testnets/blob/develop/docs/unbond.md) | Submit transaction tx | 100  |
| Total |            |                                                              |                 | 500  |





### Token Issuance Tasks

| #    | Tasks             | Details                                                      | Proof                 | Score |
| ---- | ------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 7    | token issuance      | Issue a Token A and a Token B (can be named by yourself) with Wallet A, total amount is 10000,  see`hashgardcli issue create --help` | Submit transaction tx | 100  |
| 8    | Add token description  | Add token logo (url of any picture) of token A to its description with Wallet A, see`hashgardcli issue describe --help` | Submit transaction tx | 100  |
| 9    | transfer token        | Transfer token B from Wallet A to Wallet B,see `hashgardcli bank send --help`  | Submit transaction tx | 100  |
| 10   | Mint addtional token to designated address | Mint addtional 10000 token A with wallet A to Wallet B, see`hashgardcli issue mint --help` | Submit transaction tx | 100  |
| 11   | Disable mint function | Disable the mint function of Token A with Wallet A, see`hashgardcli issue disable --help` | Submit transaction tx | 100 |
| 12   | Free designated account      | Freeze Transfer in/out function of Token A in Wallet B with Wallet A,see`hashgardcli issue freeze --help`  | Submit transaction tx | 100  |
| 13   | Unfreeze designated address        | Unfreeze the transfer in/out function of Token A in Wallet B with Wallet A,see`hashgardcli issue unfreeze --help`  | Submit transaction tx | 100  |
| 14   | Burn your own token       | Burn 10 Token A with Wallet A,  see`hashgardcli issue burn --help` | Submit transaction tx | 100  |
| 15   | owner token in other's wallet | Burn 10 Token A in Wallet B with Wallet A,see`hashgardcli issue burn-from --help`  | Submit transaction tx | 100  |
| 16   | Disable burn function       | With Wallet A（owner Account）<br />1, disable the function of burn other's token in Wallet A（owner Account）<br />2. Disable the function of burn token of your own, <br />3. disable the function of burn your own token in all accounts excep owner account , see`hashgardcli issue diasble --help` | Submit 3 transaction tx   | 150  |
| 17   | transfer owner           | Transfer the ownership of Token A which is Wallet A to Wallet B, see`hashgardcli issue transfer-ownership --hlep` | Submit transaction tx | 100  |
| Total |                     |                                                              |                 | 1150 |

Please refer to the documentation.[link](https://github.com/hashgard/hashgard/tree/develop/docs/cli/hashgardcli/issue)



### Deposit Box Tasks

| #    | Tasks                   | Details                                                         | Proof              | Score |
| ---- | -------------------------- | ------------------------------------------------------------ | ----------------- | ---- |
| 18   | Create Deposit box               | **Create a Deposit box A with targeted deposit of 100 Token A with Wallet A, and interest is 100 token B**,see`hashgardcli box create-deposit --help` | Submit transaction tx   | 100  |
| 19   | （Deposit box during releasing period）interest deposit | Deposit 10 token B to Deposit box A with wallet B, see`hashgardcli  deposit interest-injection --help`| Submit transaction tx   | 100  |
| 20   | Withdraw interest (during releasing period) | Withdraw the interest with Wallet B and then deposit it back again,see`hashgardcli box interest-fetch --help` | Submit two transaction tx   | 100  |
| 21   | make deposit (during deposit period)       | Deposit 100 token A to deposit box A with wallet C (make sure enough balance of token A in Wallet C) ,see`hashgardcli box deposit-to --help`| Submit transaction tx   | 100  |
| 22  | (After the deposit period)withdraw     | Use Wallet C to withdraw tokens from Deposit Box A,`hashgardcli bank withdraw --help`  | Submit transaction tx | 100  |
| Total |                            |                                                              |                   | 500  |

Please refer to the documentation.[link](https://github.com/hashgard/hashgard/tree/develop/docs/cli/hashgardcli/deposit)


### Future Payment Box Tasks

| #    | Tasks                   | Details                                                         | Proof            | Score |
| ---- | -------------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 22  | Create future payment box(with multiple accounts) | Create a future payment box A with 90 GARD with Wallet A，and pay 10 GARD/Wallet/period to Wallet C, Wallet D and Wallet E with 3 period, see`hashgardcli future create  --help`| Submit transaction tx | 100  |
| 23  | deposit                    | Deposit 90 GARD to Box A with Wallet B，see`hashgardcli  future  inject  --help`| Submit transaction tx | 100  |
| 22  | (After payment time)withdraw     | Use Wallet C to withdraw tokens from Deposit Box A,see`hashgardcli bank withdraw --help`  | Submit transaction tx | 100  |
| Total |                            |                                                              |                 | 200  |

Please refer to the documentation.[link](https://github.com/hashgard/hashgard/tree/develop/docs/cli/hashgardcli/future)

### Lock Box Tasks

| #    | Tasks | Details                  | Proof            | Score |
| ---- | -------- | ---------------------- | --------------- | ---- |
|  24  | Lock Boc | Create a Lock box that has 100 Token A with Wallet A ,see`hashgardcli lock create --help` | Submit transaction tx | 100  |
|  Total |          |            |                 | 100  |

Please refer to the documentation.[link](https://github.com/hashgard/hashgard/tree/develop/docs/cli/hashgardcli/lock)
### Online voting tasks

| #    | Tasks                   | Details                                                         | Proof            | Score |
| ---- | -------------------------- | --------------------------------------- | --------------- | ---- |
| 25 |  Voting | Proposal for a vote with proposal-id 1  |  Submit transaction tx | 100  |
Please refer to the documentation.[link](https://github.com/hashgard/hashgard/tree/develop/docs/cli/hashgardcli/gov)

### Online Status Task

| #    | Tasks | Details                                                         | Proof | Score |
| ---- | -------- | ------------------------------------------------------------ | ---- | ---- |
| 26  | Validator online | Keep being online since the task started till sif-6000 expired for at least 3 weeks with random snapshot |      | 300  |
| Total |          |                                                              |      | 300  |



### TotalScore 3150

## How to Submit Proof

Submit yout proof under [issue](https://github.com/hashgard/testnets/issues/32) with format below：

```plain
GitHub ID: XXXX
Task 1: Node URL
Task 2: Tx Hash / Tx Hash
Task 3: Validator address
Task 4: Tx Hash
Task 5: Tx Hash
Task 6: Tx Hash
Task 7: Tx Hash
Task 8: Tx Hash
Task 9: Tx Hash
Task 10:Tx Hash
Task 11: Tx Hash
Task 12: Tx Hash
Task 13：Tx Hash
Task 14: Tx Hash
Task 15: Tx Hash
Task 16: Tx Hash/Tx Hash/Tx Hash
Task 17: Tx Hash
Task 18: Tx Hash
Task 19: Tx Hash
Task 20: Tx Hash/Tx Hash
Task 21: Tx Hash
Task22:Tx Hash
Task23:Tx Hash
Task24Tx Hash
Task25Tx Hash
```

