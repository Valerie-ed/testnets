# 如何在sif-1000激励的测试网络中完成任务？

## sif-1000的任任务

| **编号** | **名称**                                           | **详情**                                                     | **证明**                                                     | **积分** |
| -------- | -------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------- |
| 1        | 参与到Genesis文件的生成中                         | 提交gen-tx.json文件,[参与genesis帮助文档](https://github.com/hashgard/testnets/blob/master/docs_CN/%E5%8F%82%E4%B8%8Egenesis.md)| 提供提交PR的链接                                             | 100      |
| 2        | 运行一个全节点                               | 运行一个全节点 | 提供节点的IP，并保证相应端口可访问，默认为26657端口，即 http://${your_ip}:26657/status                          | 100      |
|3|成为验证人|发送交易申请成为验证人，[成为验证人](https://github.com/hashgard/hashgard/blob/master/docs/zh/stake/create-validator.md)|提供验证器的地址|100|
| 4        | 从水龙头获得一些apple，然后将它委托给某个验证人     | 从水龙头获得一定的iris代币，然后将执行delegate操作将这部分代币委托给某个验证人。[delegate帮助文档](https://github.com/hashgard/hashgard/tree/master/docs/zh/stake) | 提供此次tx | 50       |
| 5    | 完成一笔send交易 | 创建一个钱包账号并从水龙头获得一定的apple代币，发送给另外一个地址。[send帮助文档](https://github.com/hashgard/hashgard/tree/master/docs/zh/bank)                                | 提供此次交易tx | 50     |
| 6        | 对某个提案投票                                     | 完成vote交易，[vote帮助文档](https://github.com/hashgard/hashgard/tree/master/docs/zh/gov)                                                 | 提交此处交易tx | 20       |



### 如何提交完成证明

请在以下 [issue](https://github.com/hashgard/testnets/issues/1)下提交完成证明，格式如下：

```
GitHub ID: XXXX
Task 1: Link to your PR
Task 2: Node URL
Task 3: validator address
Task 4: Tx Hash
Task 5: Tx Hash
Task 6: Tx Hash
```
