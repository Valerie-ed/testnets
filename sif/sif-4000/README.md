# sif-4000 task

## sif-4000 Task List

### Basic Tasks

| #     | Tasks                              | Details                                                      | Proof                                                        | Score |
| ----- | ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- |
| 1     | Run a full node                    | Run a full node, join testnet, and create two wallets (named Wallet A and Wallet B), [Help](https://github.com/hashgard/testnets/tree/master/docs) | submit nodes IP, and ensure that the corresponding port is accessible, the default is 26657 port, ie http://${your_ip}:26657/status | 200   |
| 2     | Get the test token from the faucet | Get GARD and apple from faucet to wallet A and wallet B,<br />See `hashgardcli keys --help` | Submit two transaction tx                                    | 100   |
| Total |                                    |                                                              |                                                              | 300   |



### Transaction Tasks

| #     | Tasks                         | Details                                                      | Proof                 | Score |
| ----- | ----------------------------- | ------------------------------------------------------------ | --------------------- | ----- |
| 3     | Transfer to normal address    | Transfer 10 GARD from Wallet A to Wallet B <br />See `hashgardcli bank send --help` | Submit transaction tx | 100   |
| 4     | Transfer to Multi-sig address | Open three normal address (named Wallet C, D and E). Open a multi-sig account CDE with Wallet C, D and E. Transfer 10 GARD to multi-sig account CDE from Wallet A. Transfer 1 GARD to  gard18p4mtd2vq297rc0dc8pkhrrjfa25p69x9gqfvx from Wallet CDE, use at least two accounts for signature among Wallet C, D and E, [Help](https://github.com/hashgard/hashgard/blob/master/docs/cli/hashgardcli/bank/multisign.md) | Submit transaction tx | 300   |
| 5     | Check transaction history     | Check multi-sig transaction history<br />See `hashgardcli tendermint tx --help` |                       |       |
| Total |                               |                                                              |                       | 400   |



### Delegation Tasks

| #     | Tasks              | Details                                                      | Proof                    | Score |
| ----- | ------------------ | ------------------------------------------------------------ | ------------------------ | ----- |
| 6     | Become a validator | Use Wallet A send a transaction to be a validator ( make sure you have created a wallet and got test tokens), [Help](https://github.com/hashgard/testnets/blob/master/docs/create-validator.md) | Submit validator address | 200   |
| 7     | Delegate           | Delegate Wallet B and transfer 10 GARD to the validator you created,[Help](<https://github.com/hashgard/testnets/blob/master/docs/delegate.md>) | Submit transaction tx    | 100   |
| 8     | Re-delegate        | Wallet B transfer delegated 10 GARD to official validator from validator created (gardvaloper17dvu8yt47mq0k0tj50rr46ke6yh4g8dzvvld6l),[Help](<https://github.com/hashgard/testnets/blob/master/docs/redelegate.md>) | Submit transaction tx    | 100   |
| 9     | Cancel delegation  | Wallet B cancel delegation by unbond function to get 10 GARD back from official validator ,[Help](<https://github.com/hashgard/testnets/blob/master/docs/unbond.md>) | Submit transaction tx    | 100   |
| Total |                    |                                                              |                          | 500   |



### Submit a proposal tasks

| #     | Tasks             | Details                                                      | Proof                 | Score |
| ----- | ----------------- | ------------------------------------------------------------ | --------------------- | ----- |
| 10    | Submit a proposal | Use Wallet A to submit a proposal and deposit 10 gard ,[Help](https://github.com/hashgard/testnets/blob/master/docs/submit-proposal.md) | Submit proposal id    | 100   |
| 11    | Vote              | Vote positive on proposals created by yourself by Wallet A, and vote negative with Wallet B ,~~[Help](<https://github.com/hashgard/testnets/blob/master/docs/vote.md>) | Submit transaction tx | 100   |
| Total |                   |                                                              |                       | 200   |



### Token Issuance Tasks

| #     | Tasks                 | Details                                                      | Proof                 | Score |
| ----- | --------------------- | ------------------------------------------------------------ | --------------------- | ----- |
| 12    | Creat a token         | Use Wallet A to create a Token <br />See `hashgardcli issue create --help` | Submit transaction tx | 100   |
| 13    | Add Token description | Use wallet A to add a logo (can be url of any pictures) to the description of token A <br />See `hashgardcli describe --help` | Submit transaction tx | 100   |
| 14    | transfer token        | Transfer token A from Wallet A to Wallet B <br />See `hashgardcli bank send --help` | Submit transaction tx | 100   |
| 15    | Mint addtional token  | Mint addtional token A with wallet A<br />See `hashgardcli issue mint --help` | Submit transaction tx | 100   |
| 16    | Burn token            | Burn part of token A with wallet A <br />See `hashgardcli issue burn --help` | Submit transaction tx | 100   |
| 17    | Transfer owner        | transfer the owner of token A which is Wallet A to Wallet B<br />See `hashgardcli issue transfer-ownership --help` | Submit transaction tx | 100   |
| Total |                       |                                                              |                       | 600   |

>Note： we will have more tasks on minting additional tokens and burning tokens in the next phase.

### Atomic swap tasks

| #     | Tasks         | Details                                                      | Proof                 | Score |
| ----- | ------------- | ------------------------------------------------------------ | --------------------- | ----- |
| 18    | Open an order | Use wallet A to open an order to exchange 10 apple by 10 GARD<br />See `hashgardcli exchange create-order --help` | Submit transaction tx | 100   |
| 19    | Match order   | Use Wallet B to partially match the order for 5 apple  <br />See `hashgardcli exchange take-order --help` | Submit transaction tx | 100   |
| 20    | Cancel order  | Use Wallet A to cancel this order  <br />See `hashgardcli withdrawal-order --help` | Submit transaction tx | 100   |
| Total |               |                                                              |                       | 300   |

### Total score 2300

## How to submit proof of completing tasks

Please submit proof of completion under the following [issue](https://github.com/hashgard/testnets/issues/11) in the following format:

```plain
GitHub ID: XXXX
Task 1: Node URL
Task 2: Tx Hash / Tx Hash
Task 3: Tx Hash
Task 4: Tx Hash
Task 5: 
Task 6: validator address
Task 7: Tx Hash
Task 8: Tx Hash
Task 9: Tx Hash
Task 10: proposal id
Task 11: Tx Hash / Tx Hash
Task 12: Tx Hash
Task 13：Tx Hash
Task 14: Tx Hash
Task 15: Tx Hash
Task 16: Tx Hash
Task 17: Tx Hash
Task 18: Tx Hash
Task 19: Tx Hash
Task 20: Tx Hash
```
