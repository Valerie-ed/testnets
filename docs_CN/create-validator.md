# 创建验证人节点

### 验证人是什么

验证人节点负责通过投票将新块提交给整个区块链网络。
验证人节点如果离线、双重签署交易或不投票，验证人将会受到惩罚，其抵押的股权将被削减。
如果您要成为验证人节点，请确保您节点的安全性，以避免资产损失。

### 创建验证人

> 在此之前，请确保您已经创建了一个本地钱包。
>
> 并且使用水龙头领取了测试币，[水龙头帮助文档](https://github.com/hashgard/hashgard/blob/develop/docs/translations/zh/cli/hashgardcli/faucet/send.md)

您可以通过运行以下命令找到验证人 pubkey：

```bash
hashgard tendermint show-validator
```

接下来，通过 hashgardcli stake create-validator 命令使节点升为验证人节点：

```bash
hashgardcli stake create-validator \
    --from=${your_wallet_name}  \
	  --pubkey=$(hashgard tendermint show-validator) \
	  --commission-max-change-rate=0.01 \
	  --commission-rate=0.1 \
	  --commission-max-rate=0.2 \
	  --amount=40gard \
	  --moniker=${your_node_name}  \
	  --min-self-delegation=10 \
	  --fees=2gard \
```

> commission 参数
>
> commission-max-change-rate 是 commission-rate 的变更百分比。
> 如：1% 到 2% commission-rate 有 100% 的变更, 但变更百分比 commission-max-change-rate 只有 1%。

> Min-self-delegation
>
> 最小自抵押数量必须为正整数。
> 如：min-self-delegation=10 表示您的验证人节点在任何时候的抵押数量不能小于 10gard。

### 查看验证人信息

使用以下命令查看验证人的信息：

```bash
hashgardcli stake validator ${validator-address} 
```

您也可以通过区块链浏览器查看验证人信息：
[http://www.gardplorer.io/validator](http://www.gardplorer.io/validator)
