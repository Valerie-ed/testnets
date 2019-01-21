# 如何参与Genesis过程
## 第1步：创建自己的帐户
首先，如果您没有帐户或忘记密码，则需要为自己创建一个帐户作为相应的验证程序操作员。
```bash
hashgardcli keys add ${account_name}
```

您可以获取帐户信息，包括帐户地址，公钥地址和助记符
```bash
hashgard	local	gard1feq6ec4whhvpzrn6ax0yrzw9nvd9mv4sh8ezv8	gardpub1addwnpepqvs5nzd57sym6jhc4m836nq05sx63g5ge5qcq0g997sk2auvxf3zg2f7nx4

**Important** write this seed phrase in a safe place.
It is the only way to recover your account if you ever forget your password.

witness exotic fantasy gaze brass zebra adapt guess drip quote space payment farm argue pear actress garage smile hawk bid bag screen wonder person
```

## 第2步：初始化您的节点
```bash
hashgard init --home=${path_to_your_home} --chain-id=${chain-id} --moniker=${your-name}
```

### 第3步：执行```gentx```命令
```bash
hashgard gentx --name=${account_name} --home=${path_to_your_home} --ip=${your--ip}
```
将在以下目录中生成事务：${HASHGARDHOME}/config/gentx 创建 CreateValidator 事务并通过刚刚创建的验证器操作员帐户对事务进行签名默认佣金数据为：
- delegation amount: 10 GARD
- commission rate: 0.1
- commission max rate: 0.2
- commission max change rate: 0.01

```
IP是您的公共IP，不使用内部IP
```


## 第4步：提交你的gentx.json
通过创建拉取请求提交您的 gentx-node-ID.json 。
在团队收集了所有 gen-tx 事务后，我们将发布```genesis```文件。
然后，您可以下载最终的```genesis```文件并启动一个节点。