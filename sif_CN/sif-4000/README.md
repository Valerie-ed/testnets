# sif-4000 任务

## sif-4000 的任务列表

### 基础任务

| #    | 任务名称                 | 详情                                                         | 证明                                                         | 积分 |
| ---- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | 运行一个全节点           | 运行一个全节点，加入 testnet，并创建两个普通地址钱包(命名为钱包 A 和钱包 B ,[帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN) | 提交节点的 IP，并保证相应端口可访问，默认为 26657 端口，即 http://${your_ip}:26657/status | 200  |
| 2    | 从水龙头地址获取测试代币 | 从水龙头领取一次的 gard 和 apple 到钱包 A 和钱包 B,[帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/faucet/send.md>) | 提交两次交易 tx                                              | 100  |
| 总计 |                          |                                                              |                                                              | 300  |



### 交易任务

| #    | 任务名称     | 详情                                                         | 证明            | 积分 |
| ---- | ------------ | ------------------------------------------------------------ | --------------- | ---- |
| 3    | 普通地址转账 | 用钱包 A 发送 10 gard 至钱包 B ,[帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/bank/send.md>) | 提交此次交易 tx | 100  |
| 4    | 多签地址转账 | 创建三个普通账户（分别命名为钱包 C、D、E）用这三个账户创建一个钱包 CDE 的多签账户，用钱包 A 转账 10 gard 至多签账户 CDE，用钱包 CDE 转账 1gard 至 gard18p4mtd2vq297rc0dc8pkhrrjfa25p69x9gqfvx，至少用到钱包 C、D、E 中的两个账户进行签名 ,[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/bank/multisign.md) | 提交此次交易 tx | 300  |
| 5    | 查询交易记录 | 查询该笔多签的交易,[帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/tendermint/tx.md>) |                 |      |
| 总计 |              |                                                              |                 | 400  |



### 委托任务

| #    | 任务名称   | 详情                                                         | 证明            | 积分 |
| ---- | ---------- | ------------------------------------------------------------ | --------------- | ---- |
| 6    | 成为验证人 | 使用钱包 A 发送交易申请成为验证人, (在此之前，请确保您已经创建钱包，并领取了测试 token) [帮助文档](https://github.com/hashgard/testnets/blob/master/docs_CN/%E5%88%9B%E5%BB%BA%E9%AA%8C%E8%AF%81%E4%BA%BA%E8%8A%82%E7%82%B9.md) | 提交验证人地址  | 200  |
| 7    | 委托       | 将钱包 B 执行 delegate 操作，将 10 gard 委托给自己创建的验证人,[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/delegate.md) | 提交此次交易 tx | 100  |
| 8    | 重新委托   | 钱包 B 通过 redelegate 操作，将委托的 10 gard 从自己创建的验证人转移至官方验证人(gardvaloper17dvu8yt47mq0k0tj50rr46ke6yh4g8dzvvld6l),[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/stake/redelegate.md) | 提交此次交易 tx | 100  |
| 9    | 取消委托   | 钱包 B 通过 unbond 操作，取消委托，取回委托在官方验证人的 10 gard,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/stake/unbond.md) | 提交此次交易 tx | 100  |
| 总计 |            |                                                              |                 | 500  |



### 提案任务

| #    | 任务名称 | 详情                                                         | 证明            | 积分 |
| ---- | -------- | ------------------------------------------------------------ | --------------- | ---- |
| 10   | 发起提案 | 使用钱包 A 发起一个文本类型的提案并抵押 10 gard,[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/gov/submit-proposal.md) | 提交此次提案 id | 100  |
| 11   | 投票     | 使用钱包 A 对**自己创建的提案**投赞同票，钱包 B 投反对票,[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/gov/vote.md) | 提交此次交易 tx | 100  |
| 总计 |          |                                                              |                 | 200  |



### 发行 Token 任务

| #    | 任务名称      | 详情                                                         | 证明            | 积分 |
| ---- | ------------- | ------------------------------------------------------------ | --------------- | ---- |
| 12   | 创建 token     | 使用钱包 A 发行一个 token A(自由取名),[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/issue/create.md) | 提交此次交易 tx | 100  |
| 13   | 添加 token 描述 | 使用钱包 A 将 logo(可使用任意图片的 url)补充进 toekn A 的 description ,[帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/issue/describe.md>) | 提交此次交易 tx | 100  |
| 14   | 转账 token     | 使用钱包 A 将钱包 A 中的 token A 转账至钱包 B,[帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/bank/send.md>) | 提交此次交易 tx | 100  |
| 15   | 增发          | 使用钱包 A 对 token A 进行增发，[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/issue/mint.md) | 提交此次交易 tx | 100  |
| 16   | 销毁          | 使用钱包 A 将 token A 进行部分销毁, [帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/issue/burn.md) | 提交此次交易 tx | 100  |
| 17   | 转移 owner     | 将 token A 的 owner 即钱包 A 转移到钱包 B,[帮助文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/issue/transfer-ownership.md) | 提交此次交易 tx | 100  |
| 总计 |               |                                                              |                 | 600  |

`备注：下一个网络任务将公布增发和销毁的进一步任务`



### 原子交换任务

| #    | 任务名称 | 详情                                                         | 证明            | 积分 |
| ---- | -------- | ------------------------------------------------------------ | --------------- | ---- |
| 18   | 创建订单 | 使用钱包 A 创建一笔「用 10 gard 换取 10 apple」的订单, [帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/exchange/create-order.md>) | 提交此次交易 tx | 100  |
| 19   | 成交订单 | 使用钱包 B 花费 5 apple 部分成交该订单, [帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/exchange/take-order.md>) | 提交此次交易 tx | 100  |
| 20   | 撤销订单 | 使用钱包 A 撤销该笔订单, [帮助文档](<https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/exchange/withdrawal-order.md>) | 提交此次交易 tx | 100  |
| 总计 |          |                                                              |                 | 300  |

### 总计积分 2300

## 如何提交完成证明

请在以下 [issue](https://github.com/hashgard/testnets/issues/11)下提交完成证明，格式如下：

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
