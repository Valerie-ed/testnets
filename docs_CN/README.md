# Hashgard Testnet
> 此次为sif-3001测试网络，请务必chain-id指定sif-3001

> ${}代表变量可替换

## 如何加入

### 步骤1：在您的服务器上安装Hashgard
请按照此说明在本地安装Hashgard，[hashgard安装文档](hashgard安装文档.md)。

### 步骤2 创建钱包

如果尚未创建钱包，请按照[钱包创建文档](https://github.com/hashgard/hashgard/blob/master/docs/zh/hashgardcli/keys/add.md)创建钱包

设置默认参数

```
# 设置默认连接节点
hashgardcli config chain-id sif-3001
hashgardcli config trust-node ture
# 输出格式化
hashgardcli config indent ture
hashgardcli config output json
```

### 步骤3：初始化节点并获取配置文件

初始化节点

`hashgard init --chain-id=sif-3001 --moniker=${your_node_name}`

如果您想成为 geneartion 进程的一部分，请按照本[指南](参与genesis.md)来生成一个json文件。或者，您可以随后发送相关事务以成为验证人节点。

生成文件生成过程完成后，请下载genesis和默认配置文件。
```bash
cd $HASHGARDHOME/config/
rm genesis.json
rm config.toml
wget https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-3001/config/config.toml
wget https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-3001/config/genesis.json
```

默认的$ HASHGARDHOME是  `~/.hashgard`，您节点的name可以稍后在`~/.hashgard/config/config.toml`文件中编辑：

```toml
# A custom human readable name for this node
moniker = "${your_node_name}"
external_address = "${your_public_ip}:26656"
```



### 步骤4：运行完整节点

使用以下命令启动整个节点：

```bash
hashgard start > hashgard.log &
```

检查一切是否顺利进行：

```bash
hashgardcli status --indent
```


您可以看到以下内容:
```json
{
  "node_info": {
    "protocol_version": {
      "p2p": "5",
      "block": "8",
      "app": "0"
    },
    "id": "b783ac2b41da096ddc3a26c2a39e3b0c1ea49d9e",
    "listen_addr": "127.0.0.190:26656",
    "network": "hashgard",
    "version": "0.27.0",
    "channels": "4020212223303800",
    "moniker": "hashgard_test",
    "other": {
      "tx_index": "on",
      "rpc_address": "tcp://0.0.0.0:26657"
    }
  },
  "sync_info": {
    "latest_block_hash": "AFB6261A76DCC6176FF5248B3B5BEDEEBD38B6DA3D18AD21ADD4054AEDEED016",
    "latest_app_hash": "1DEAF3D71AD735F4E375439DAFD96C8934E944D8D32F6179F55C5470E219D132",
    "latest_block_height": "77280",
    "latest_block_time": "2018-12-24T07:13:53.787154732Z",
    "catching_up": false
  },
  "validator_info": {
    "address": "5959DF3D28F601407A98D0B038174E288ED45BD7",
    "pub_key": {
      "type": "tendermint/PubKeyEd25519",
      "value": "wYrxKp7cw14eQiqzfGBggEV474ZA2lc35AieJM5SM6Y="
    },
    "voting_power": "950"
  }
}
```


当您看到 `catching_up` 是 `false`，表示节点与testnet已经同步完成，否则表示它仍在同步。

### 步骤5：升级到验证人( Validator )节点

您现在拥有一个活动的完整节点。下一步是什么？

如果您参与了genesis文件生成过程，那么一旦完全同步，您就会成为验证人中的一员。

如果您错过了genesis文件生成过程，您仍然可以升级整个节点以成为Hashgardnet验证人，继续进入[创建验证人节点](创建验证人节点.md)。

您也可以[委托](委托代币.md)，[解绑](解绑委托.md)，[再委托](重新委托.md)

### 步骤6：链式治理

去中心化的链式，您可以在链上发起提案，也可参与到投票过程中

如何发起提案？进入[发起治理提案](提交在线治理.md)

提案时需要进入激活状态才能发起投票，在此之前，您可以进行[抵押存款](抵押存款.md)

对于被正式被激活的提案，您可以对其进行[投票](提案投票.md)
