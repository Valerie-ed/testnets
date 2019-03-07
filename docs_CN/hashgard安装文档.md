# Hashgard 安装文档 #
Hashgard 公链采用Go语言编写，它可以在任何能够编译并运行Go语言程序的平台上工作。我们建议采用方法二，即可执行文件安装的方式安装 Hashgard 公链

## 配置您的服务器
Hashgard 公链基于Cosmos-SDK 开发，Cosmos SDK 是使用 Go 语言开发的区块链应用程序的框架。建议在 Linux 服务器中运行验证程序节点。

**推荐配置：**

- CPU：2Core
- 内存：4GB
- 磁盘：60GB SSD
- 操作系统：Ubuntu 16.04 LTS
- 允许来自 TCP  26656-26657 端口的所有传入连接

## 方法1：源码编译安装 ##
需要保证 Go 的版本在 1.11.5 以上，下载 [Go 1.11.5+](https://golang.org/dl)

此外，你需要指定相关的 `$GOPATH`、`$GOBIN` 和 `$PATH` 变量, 例如:

```bash
mkdir -p $HOME/go/bin
echo "export GOPATH=$HOME/go" >> ~/.bash_profile
source ~/.bash_profile
echo "export GOBIN=$GOPATH/bin" >> ~/.bash_profile
source ~/.bash_profile
echo "export PATH=$PATH:$GOBIN" >> ~/.bash_profile
source ~/.bash_profile
```
参考链接：
1. https://golang.org/doc/install
2. https://github.com/golang/go/wiki/Ubuntu


请将 Hashgard 项目放在指定目录，切换至 master 分支，进行安装：

```bash
mkdir -p $GOPATH/src/github.com/hashgard
cd $GOPATH/src/github.com/hashgard
git clone https://github.com/hashgard/hashgard
cd hashgard && git checkout master
make get_tools && make get_vendor_deps && make install
```

当完成安装之后，最后检查是否安装成功

```bash
hashgard help
hashgardcli help
```



## 方法2: 下载可执行文件

从 github [下载](https://github.com/hashgard/hashgard/releases) 您的操作系统所对应的版本，并解压 hashgard、hashgardcli 到对应的目录下：

- Linux / MacOS ：/usr/local/bin
- Windows: C:\windows\system32\

当完成解压之后，可在 CMD 中检查是否安装成功

```bash
hashgard help
hashgardcli help
```
如果出现
```
Command line interface for interacting with hashgard
```
则表示安装成功
