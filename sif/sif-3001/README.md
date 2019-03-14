# 如何完成sif-3001测试网络中的激励任务？

## sif-3001的任务

| **编号** | **名称**                                       | **详情**                                                     | **证明**                                                     | **积分** |
| -------- | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------- |
| 1        | 运行一个全节点                                 | 运行一个全节点，[加入testnet帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN) | 提交节点的IP，并保证相应端口可访问，默认为26657端口，即 http://${your_ip}:26657/status | 100      |
| 2        | 成为验证人                                     | 在此之前，请确保您已经创建钱包，并领取了测试token。发送交易申请成为验证人，[成为验证人](https://github.com/hashgard/testnets/blob/master/docs_CN/%E5%BC%80%E5%A7%8B%E4%B8%80%E4%B8%AA%E9%AA%8C%E8%AF%81%E5%99%A8%E8%8A%82%E7%82%B9.md) | 提交验证器的地址                                             | 100      |
| 3        | 从水龙头获得一些gard，然后将它委托给某个验证人 | 从水龙头获得一定的gard代币，然后将执行delegate操作将这部分代币委托给某个验证人。[delegate帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/delegate.md) | 提交此次交易tx                                               | 50       |
| 4        | 取消委托                                       | 对于您委托过的验证人，您可以通过unbond操作，指定其取消一定的您委托的股份，[unbond帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/unbond.md) | 提交此次交易tx                                               | 50       |
| 5        | 重新委托                                       | 您可以通过redelegate操作，讲您委托的一部或者全部从一个验证人转移到另外一个验证人身上，[redelegate帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/redelegate.md) | 提交此次交易tx                                               | 50       |
| 6        | 发起提案                                       | 您可以通过submit-proposal操作，提交治理提案，[submit-proposal帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/gov/submit-proposal.md) | 提交此处交易tx                                               | 50       |
| 7        | 使用多签账户转账                               | 创建三个普通账户（分别为a1、a2、a3）用这三个账户创建一个a123的多签账户，用普通账户打币至多签账户a123，用a123转账 1gard 至 gard1d0s06rave0a6xzvuw7nhz782vcty99hgunc724（至少用a1、a2、a3中的两个账户进行签名），[multisign帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/bank/multisign.md) | 提交此次交易tx                                               | 50       |
| 8        | 对提案进行投票                                 | 使用有余额的账户对6号提案进行投票，[query-votes帮助](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/gov/vote.md) | 提交投票账户的地址                                           |          |



### 如何提交完成证明

请在以下 [issue](https://github.com/hashgard/testnets/issues/5)下提交完成证明，格式如下：

```
GitHub ID: XXXX
Task 1: Node URL
Task 2: validator address
Task 3: Tx Hash
Task 4: Tx Hash
Task 5: Tx Hash
Task 6: Tx Hash
Task 7: Tx Hash
Task 8: voter address
```
