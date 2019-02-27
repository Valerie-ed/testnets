# 如何参与Genesis过程
## 第1步：创建自己的帐户
首先，如果您没有帐户或忘记密码，则需要为自己创建一个帐户作为相应的验证程序操作员。
```bash
hashgardcli keys add root
```

您可以获取帐户信息，包括帐户地址，公钥地址和助记符
```bash
Enter a passphrase to encrypt your key to disk:
Repeat the passphrase:

NAME:	TYPE:	ADDRESS:						PUBKEY:
root	local	gard10w7duyzwtqmfya6avl2txl2hnjf7mdfl5lsv4q	gardpub1addwnpepqt4x0pc744uzuhzd4qnl89urs2ff7wxjlv6pw4c47qs3fxx5pjfwy5g0k6r

**Important** write this mnemonic phrase in a safe place.
It is the only way to recover your account if you ever forget your password.

shock prize color tenant raccoon country aunt palm column expose ship fame present miracle spatial slow acoustic trumpet bus shock educate private fly recipe
```

## 第2步：初始化您的节点
```bash
hashgard init --chain-id=hashgard-0.3.1 --moniker=${your-name}
```

## 第3步：向 genesis.json 中添加账户信息

```bash
hashgard add-genesis-account root 100000000gard
```

## 第4步：向 genesis.json 中添加账户信息

```bash
hashgard gentx --name=root --amount=100000000gard --ip=${validator_ip}
```
将在以下目录中生成事务：~/.hashgard/config/gentx 创建 CreateValidator 事务并通过刚刚创建的验证器操作员帐户对事务进行签名默认佣金数据为：
- delegation amount: 100000000 gard
- commission rate: 0.1
- commission max rate: 0.2
- commission max change rate: 0.01

```
注：${validator_ip} 是您的公网 IP 地址，不使用内部IP。
```


## 第5步：提交你的 gentx.json
通过创建拉取请求提交您的 gentx-node-ID.json 。
在团队收集了所有 gen-tx 事务后，我们将发布```genesis```文件。
然后，您可以下载最终的```genesis```文件并启动一个节点。