# sif-7000 任务

## sif-7000 的任务列表

### 基础任务

| #    | 任务名称                 | 详情                                                         | 证明                                                         | 积分 |
| ---- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | 运行一个全节点           | 运行一个全节点，加入 testnet，并创建 6 个普通地址钱包(命名为钱包 A / B / C / D / E / F ,[帮助文档](https://github.com/hashgard/testnets/tree/develop/docs_CN/README.md) | 提交节点的 IP，并保证相应端口可访问，默认为 26657 端口，即 http://${your_ip}:26657/status | 200  |
| 2    | 从水龙头地址获取测试代币 | 从水龙头领取一次的 gard 和 apple 到钱包 A 和钱包 B,[帮助文档](https://github.com/hashgard/hashgard/tree/develop/docs/translations/zh/cli/hashgardcli/faucet/send.md) | 提交两次交易 tx                                              | 100  |
| 总计 |                          |                                                              |                                                              | 300  |


### 委托任务

| #    | 任务名称   | 详情                                                         | 证明            | 积分 |
| ---- | ---------- | ------------------------------------------------------------ | --------------- | ---- |
| 3    | 成为验证人 | 使用钱包 A 发送交易申请成为验证人, (在此之前，请确保您已经创建钱包，并领取了测试 token) [帮助文档](https://github.com/hashgard/testnets/tree/develop/docs_CN/create-validator.md) | 提交验证人地址  | 200  |
| 4    | 委托       | 将钱包 B 执行 delegate 操作，将 10 gard 委托给自己创建的验证人,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/stake/delegate.md) | 提交此次交易 tx | 100  |
| 5    | 重新委托   | 钱包 B 通过 redelegate 操作，将委托的 10 gard 从自己创建的验证人转移至其他验证人[地址查询](https://www.gardplorer.io/validator),[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/stake/redelegate.md) | 提交此次交易 tx | 100  |
| 6    | 取消委托   | 钱包 B 通过 unbond 操作，取消委托，取回委托在官方验证人的 10 gard,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/stake/unbond.md) | 提交此次交易 tx | 100  |
| 总计 |            |                                                              |                 | 500  |


### 发行 Token 任务

| #    | 任务名称            | 详情                                                         | 证明            | 积分 |
| ---- | ------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 7    | 创建 token           | 使用钱包 A 发行一个 token A 和 token B (自由取名)，数量为 1000,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/create.md) | 提交此次交易 tx | 100  |
| 8    | 添加 token 描述       | 使用钱包 A 将 logo(可使用任意图片的 url)补充进 toekn A 的 description ,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/describe.md) | 提交此次交易 tx | 100  |
| 9    | 转账 token           | 将钱包 A 中的 1000 token B 转账至钱包 B,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/send.md) | 提交此次交易 tx | 100  |
| 10   | 增发到指定地址      | 使用钱包 A ，增发 10000 token A 到钱包 B,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/mint.md) | 提交此次交易 tx | 100  |
| 11   | 关闭增发            | 使用钱包 A ，关闭 token A 的增发开关,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/disable.md) | 提交此次交易 tx | 100  |
| 12   | 冻结指定地址        | 使用钱包 A，冻结钱包 B 里的 token A 的转入转出功能,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/freeze.md) | 提交此次交易 tx | 100  |
| 13   | 解冻指定地址        | 使用钱包 A，解冻钱包 B 里的 token A 的转入转出功能,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/unfreeze.md) | 提交此次交易 tx | 100  |
| 14   | 销毁自身 token       | 使用钱包 A 销毁数量为 10 的 token A, [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/burn.md) | 提交此次交易 tx | 100  |
| 15   | owner 销毁他人 token | 使用钱包 A 销毁钱包 B 数量为 10 的 token A，[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/burn-from.md) | 提交此次交易 tx | 100  |
| 16   | 关闭销毁开关        | 使用钱包 A（owner 账户）<br />1. 将钱包 A（owner 账户）销毁其他账户的功能关闭,<br />2. 将非 owner 账户销毁功能关闭, <br />3. 将 token A 的销毁功能关闭，[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/disable.md) | 提交 3 次交易 tx   | 150  |
| 17   | 转移 owner           | 将 token A 的 owner 即钱包 A 转移到钱包 B,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/issue/transfer-ownership.md) | 提交此次交易 tx | 100  |
| 总计 |                     |                                                              |                 | 1150 |


### 存款盒子任务

| #    | 任务名称                   | 详情                                                         | 证明            | 积分 |
| ---- | -------------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 18   | 创建存款盒子               | **用钱包 A 创建一笔存款目标 100 token A ，利息为 10 token B 的存款盒子 A**,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/create.md) | 提交此次交易 tx | 100  |
| 19   | （存款盒子发行期）利息注入 | 用钱包 B 注入 10 token B 至存款盒子 A,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/interest-inject.md) | 提交次次交易 tx | 100  |
| 20   | （存款盒子发行期）利息取回 | 用钱包 B 取回利息，并再此注入,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/interest-cancel.md) | 提交两次交易 tx | 100  |
| 21   | (在存款吸纳期)存款         | 用钱包 C (请事先往钱包 C 打入余额）往存款盒子 A 存入 100 token A ,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/inject.md) | 提交此次交易 tx | 100  |
| 22  | (存款结束期后)取款      | 用钱包 C 提取存款盒子 A 中存储的代币,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/withdraw.md) | 提交此次交易 tx | 100  |
| 总计 |                            |                                                              |                 | 500  |



### 远期支付盒子任务


| #    | 任务名称                   | 详情                                                         | 证明            | 积分 |
| ---- | -------------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 23   | 创建（多账户）远期支付盒子 | 用钱包 A 创建一个总量为 90 GARD ，对钱包 C / D / E 钱包，分三期（每期每账户 10 GARD）进行远期支付的远期支付盒子 A ,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/future/create.md) | 提交此次交易 tx | 100  |
| 24   | 存款                       | 用钱包 B 存入 90 GARD 至盒子 A，[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/inject.md) | 提交此次交易 tx | 100  |
| 25  | (在支付到期)取款      | 用钱包 C 提取存款盒子 A 中存储的代币,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/withdraw.md) | 提交此次交易 tx | 100  |
| 总计 |                            |                                                              |                 | 300  |
远期支付的盒子因为有多期，请事先使用 hashgardcli bank account 查询账户的实际持有的盒子
### 锁定盒子任务

| #    | 任务名称 | 详情                                                         | 证明            | 积分 |
| ---- | -------- | ------------------------------------------------------------ | --------------- | ---- |
| 26   | 锁定盒子 | 用钱包 A 创建一个包含 100 token A 的锁定盒子,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/lock/create.md) | 提交此次交易 tx | 100  |
| 总计 |          |                                                              |                 | 100  |

### 在线投票升级任务

| 序号 |任务名称 |详情 | 证明|积分|
|--|-- |-- |--| -- |
| 27 |  进行投票 | 查询可以投票的提案进行投票 [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/gov/README.md)   |  提交此次交易 tx | 100  |
| 总计 |          |                                                              |                 | 100  |

### 存证功能
| 序号 |任务名称 |详情 | 证明|积分|
|--|-- |-- |--| -- |
| 28|  进行存证 | 进行存证 [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/record/create.md)   |  提交此次交易 tx | 100  |
| 29   |  进行查询 | 对已经存证的 hash 进行查询[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/record/query.md)     |   | |
| 总计 |          |                                                              |                 | 100  |

### 强制地址转入备注
| 序号 |任务名称 |详情 | 证明|积分|
|--|-- |-- |--| -- |
| 30 |  设置备注 | 设置 A 地址转入备注为 true [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/keys/flag-required.md)   |  提交此次交易 tx | 100  |
| 31   | 查询   | 对 A 地址进行交易备注查询  [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/keys/flag-required-query.md)  |    |   |
| 32   | 转账  | 使用 B 地址对 A 进行转账并填写memo信息   [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/send.md)  | 提交此次交易 tx | 100 |
| 33 |  设置备注 | 设置 A 地址转入备注为 false [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/keys/flag-required.md)   |  提交此次交易 tx | 100  |
| 34   | 转账  | 使用 B 地址对 A 进行转账 [帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/send.md)  | 提交交易hash | 100 |
| 总计 |          |                                                              |                 | 400 |


### 在线任务
| #    | 任务名称 | 详情                                                         | 证明 | 积分 |
| ---- | -------- | ------------------------------------------------------------ | ---- | ---- |
| 35   | 节点在线 | 自提交任务后的至 sif-7000 下线期间一直保持在线（要求至少三周），采取随机快照的方式进行 |      | 300  |
| 总计 |          |                                                              |      | 300  |




### 总计积分 3750

## 如何提交完成证明

请在以下 [issue](https://github.com/hashgard/testnets/issues/32)下提交完成证明，格式如下：

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
Task26Tx Hash
Task27Tx Hash
Task28Tx Hash
Task29
Task30Tx Hash
Task31
Task32Tx Hash
Task33Tx Hash
Task34Tx Hash
Task35Tx Hash

```
