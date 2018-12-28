# Hashgard Testnet
> 此次为sif-1000测试网络，请务必chain-id指定sif-1000
> ${}代表变量可替换

## 如何加入
### 步骤1：在您的服务器上安装Hashgard
请按照此说明在本地安装Hashgard,[hashgard安装文档](hashgard安装文档.md)。

### 步骤2：设置节点
这些说明适用于从头开始设置全新的完整节点。

首先，初始化节点并创建必要的配置文件：

```
hashgard init --moniker=${your_custom_name} --chain-id=${chain-id} --home=${HASHGARDHOME} 
```
> 注意：仅支持ASCII字符--name。使用Unicode字符将使您的节点无法访问。

### 获取配置文件
获取配置文件
如果您想成为genesis文件geneartion进程的一部分，请按照本指南来总结一个json文件。否则，您可以随后发送相关事务以成为验证器。

生成文件生成过程完成后，请下载genesis和默认配置文件。
```
cd $HASHGARDHOME/config/
rm genesis.json
rm config.toml
wget https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-1000/config/config.toml
wget https://raw.githubusercontent.com/hashgard/testnets/master/sif/sif-1000/config/genesis.json

```

默认的$ HASHGARDHOME是~/.hashgard，您节点的name可以稍后在~/.hashgard/config/config.toml文件中编辑：
```
# A custom human readable name for this node
moniker = "${your_custom_name}"
external_address = "${your-public-IP}"

```

可选：设置addr_book_strict为false更轻松地进行对等。
```
addr_book_strict = false
```


### 添加种子节点
您的节点需要知道如何查找对等点。您需要添加健康的种子节点$HASHGARD/config/config.toml。以下是您可以使用的一些种子节点：
```
e31e4242d8aac069193428d6bcb16b8c52f41c62@39.105.98.20:26656
```

同时，您可以添加一些已知的完整节点作为```Persistent Peer```。你的节点可以连接到```sentry node```的```persistent peers```。

将```external_address```改成你的```public IP:26656```。

### 运行完整节点
使用以下命令启动整个节点：
```hashgard start --home=$HASHGARDHOME > hashgard.log```

检查一切是否顺利进行：
```hashgardcli status```


您可以看到以下内容:
```
{"node_info":{"protocol_version":{"p2p":"5","block":"8","app":"0"},"id":"b783ac2b41da096ddc3a26c2a39e3b0c1ea49d9e","listen_addr":"127.0.0.190:26656","network":"hashgard","version":"0.27.0","channels":"4020212223303800","moniker":"hashgard_test","other":{"tx_index":"on","rpc_address":"tcp://0.0.0.0:26657"}},"sync_info":{"latest_block_hash":"AFB6261A76DCC6176FF5248B3B5BEDEEBD38B6DA3D18AD21ADD4054AEDEED016","latest_app_hash":"1DEAF3D71AD735F4E375439DAFD96C8934E944D8D32F6179F55C5470E219D132","latest_block_height":"77280","latest_block_time":"2018-12-24T07:13:53.787154732Z","catching_up":false},"validator_info":{"address":"5959DF3D28F601407A98D0B038174E288ED45BD7","pub_key":{"type":"tendermint/PubKeyEd25519","value":"wYrxKp7cw14eQiqzfGBggEV474ZA2lc35AieJM5SM6Y="},"voting_power":"950"}}
```


当您看到```catching_upis```时false，表示节点与testnet已经同步完成，否则表示它仍在同步。


### 升级到Validator节点
您现在拥有一个活动的完整节点。下一步是什么？

如果您参与了genesis文件生成过程，那么一旦完全同步，您就应该成为验证者。

如果您错过了genesis文件生成过程，您仍然可以升级整个节点以成为Hashgardnet验证程序。继续进入[验证器设置](开始一个验证器节点.md)。

您也可以[委托](委托代币.md)，[解绑](解绑委托.md)，[再委托](重新委托.md)


### 链式治理
去中心化的链式，您可以在链上发起提案，也可参与到投票过程中

如何发起提案？进入[发起治理提案](提交在线治理.md)

提案时需要进入激活状态才能发起投票，在此之前，您可以进行[抵押存款](抵押存款.md)

对于被正式被激活的提案，您可以对其进行[投票](提案投票.md)
