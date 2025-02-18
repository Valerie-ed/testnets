# 如何完成 sif-2000 测试网络中的激励任务

## sif-2000 的任务

| **编号** | **名称**                                       | **详情**                                                     | **证明**                                                     | **积分** |
| -------- | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------- |
| 1        | 运行一个全节点                                 | 运行一个全节点，[加入 testnet 帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN) | 提供节点的 IP，并保证相应端口可访问，默认为 26657 端口，即 http://${your_ip}:26657/status | 100      |
| 2        | 成为验证人                                     | 在此之前，请确保您已经创建钱包，并领取了测试 token。发送交易申请成为验证人，[成为验证人](https://github.com/hashgard/testnets/blob/master/docs_CN/%E5%BC%80%E5%A7%8B%E4%B8%80%E4%B8%AA%E9%AA%8C%E8%AF%81%E5%99%A8%E8%8A%82%E7%82%B9.md) | 提供验证器的地址                                             | 100      |
| 3        | 从水龙头获得一些 gard，然后将它委托给某个验证人 | 从水龙头获得一定的 gard 代币，然后将执行 delegate 操作将这部分代币委托给某个验证人。[delegate 帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/delegate.md) | 提供此次交易 tx                                               | 50       |
| 4        | 取消委托                                       | 对于您委托过的验证人，您可以通过 unbond 操作，指定其取消一定的您委托的股份。[unbond 帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/stake/unbond.md) | 提供此次交易 tx                                               | 50       |
| 5        | 重新委托                                       | 您可以通过 redelegate 操作，讲您委托的一部或者全部从一个验证人转移到另外一个验证人身上。[redelegate 帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/redelegate.md) | 提供此次交易 tx                                               | 50       |
| 6        | 发起提案                                       | 您可以通过 submit-proposal 操作，提交治理提案，[submit-proposal 帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/gov/submit-proposal.md) | 提交此处交易 tx                                               | 50       |



### 如何提交完成证明

请在以下 [issue](https://github.com/hashgard/testnets/issues/3)下提交完成证明，格式如下：

```plain
GitHub ID: XXXX
Task 1: Node URL
Task 2: validator address
Task 3: Tx Hash
Task 4: Tx Hash
Task 5: Tx Hash
Task 6: Tx Hash
```
