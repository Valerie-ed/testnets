### 基础任务

| 序号    | 任务名称                 | 详情                                                         | 证明                                                         | 积分 |
| ---- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---- |
| 1    | 创建钱包，运行全节点           | 下载最新版本的软件并安装[帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN/installation.md)，创建 A、B、C、D、E、F 钱包地址[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/keys/add.md)。 运行一个全节点，加入 testnet[帮助文档](https://github.com/hashgard/testnets/blob/master/docs_CN/README.md) | 提交节点的 IP，并保证相应端口可访问，默认为 26657 端口，即 http://${your_ip}:26657/status | 200  |
| 2    | 从水龙头地址获取测试代币 | 从水龙头领取一次的 gard 和 apple 到钱包 A 和钱包 B,[帮助文档](https://github.com/hashgard/hashgard/tree/develop/docs/translations/zh/cli/hashgardcli/faucet/send.md) | 提交两次交易 tx                                              | 100  |




### 委托任务

| 序号    | 任务名称   | 详情                                                         | 证明            | 积分 |
| ---- | ---------- | ------------------------------------------------------------ | --------------- | ---- |
| 3    | 成为验证人 | 使用钱包 A 发送交易申请成为验证人, (在此之前，请确保您已经创建钱包，并领取了测试 token) [帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN/GreatValidator.md) | 提交验证人地址  | 200  |
| 4    | 委托       | 将钱包 B 执行 delegate 操作，将 10 gard 委托给自己创建的验证人,[帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN/Delegate.md) | 提交此次交易 tx | 100  |
| 5    | 重新委托   | 钱包 B 通过 redelegate 操作，将委托的 10 gard 从自己创建的验证人转移至官方验证人(gardvaloper13fn2v2rstszureanek9aqvev6z8hzx0hty77wj),[帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN/Redelegate.md) | 提交此次交易 tx | 100  |
| 6    | 取消委托   | 钱包 B 通过 unbond 操作，取消委托，取回委托在官方验证人的 10 gard,[帮助文档](https://github.com/hashgard/testnets/tree/master/docs_CN/unbond.md) | 提交此次交易 tx | 100  |


###  存款协议（HRC12）任务

| 序号    | 任务名称                   | 详情                                                         | 证明            | 积分 |
| ---- | -------------------------- | ------------------------------------------------------------ | --------------- | ---- |
|   7   | 创建存款盒子               | **用钱包 A 创建一笔存款目标 100 token A ，利息为 10 token B 的存款盒子 A**,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/create.md) | 提交此次交易 tx | 100  |
|   8   | 存款盒子发行期）利息注入   | 用钱包 B 注入 10 token B 至存款盒子 A,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/interest-inject.md) | 提交此次交易 tx | 100  |
|   8   | （存款盒子发行期）利息取回 | 用钱包 B 取回利息，并再此注入,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/interest-cancel.md) | 提交此次交易 tx | 100  |
|   9   | (在存款吸纳期)存款         | 用钱包 C (请事先往钱包 C 打入余额）往存款盒子 A 存入 100 token A ,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/deposit/inject.md) | 提交此次交易 tx | 100  |
|   10   | （在存款吸纳期）取回存款   | 用钱包 C 取回存入的 100 token A，再注入回去                    |      提交此次交易 tx          |  100    |



### 远期支付协议（HRC13）

| 序号    | 任务名称                   | 详情                                                         | 证明            | 积分 |
| ---- | -------------------------- | ------------------------------------------------------------ | --------------- | ---- |
| 11   | 创建（多账户）远期支付盒子 | 用钱包 A 创建一个总量为 90 GARD ，对钱包 C / D / E 钱包，分三期（每期每账户 10 GARD）进行远期支付的远期支付盒子 A ,[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/future/create.md) | 提交此次交易 tx | 100  |
| 12   | 存款           | 用钱包 B 存入 90 GARD 至盒子 A，[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/future/inject.md) | 提交此次交易 tx | 100  |
| 13    | 用户提取收款  |C/D/E 任意钱包在支付到期后提取支付盒子中的 GARD[帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/bank/withdraw.md)   |  提交此次交易 tx |  100 |

### 在线升级任务

| 序号 |任务名称 |详情 | 证明|积分|
|--|-- |-- |--| -- |
| 12 |  进行 | 使用客户端进行查询名叫   |  提交此次交易 tx |   |
