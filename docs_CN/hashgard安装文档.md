# hashgard安装文档 #
采用Go语言编写，它可以在任何能够编译并运行Go语言程序的平台上工作

## 方法1：源码编译安装 ##
需要保证Go的版本在1.10以上，下载[Go 1.10+](https://golang.org/dl)

此外，你需要指定相关的 $GOPATH, $GOBIN, 和 $PATH 变量, 例如:

```
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

```
mkdir -p $GOPATH/src/github.com/hashgard
cd $GOPATH/src/github.com/hashgard
git clone https://github.com/hashgard/hashgard
cd hashgard && git checkout master
make get_tools && make get_vendor_deps && make install

```
如果无法正常下载依赖包，请设置合适的代理，配置代理的方法如下：
**CentOS：**
```
sudo yum install python-setuptools && easy_install pip
sudo pip install shadowsocks
```

配置shadowsocks的配置文件，一般放到``` /etc```下面
```
sudo vi /etc/shadowsocks.json
```
然后在shadowsocks.json里面添加配置信息:
```
{
  "server":"my_server_ip",
  "local_address": "127.0.0.1",
  "local_port":1080,
  "server_port":my_server_port,
  "password":"my_password",
  "timeout":300,
  "method":"aes-256-cfb"
}
```
- my_server_ip改为自己的服务器IP
- my_server_port改为自己的服务器端口
- my_server_password改为自己的密码
- method的值改为自己的加密方式，一般是aes-256-cfb或者rc4-md5
- local_address为本地地址
- local_port为本地端口，一般1080，可任意


接下来需要配置SOCKS5 代理设置：
```
export HTTP_PROXY="socks5://127.0.0.1:1080"
export HTTPS_PROXY="socks5://127.0.0.1:1080"
```
>socks5://127.0.0.1:1080对应的ip和端口就是在shadowsocks.json中设置的ip和端口

检查是否配置成功：
```
echo $HTTP_PROXY
```
启动shadowsocks客户端：
```
sslocal -c /etc/shadowsocks.json 
```

>-c 后对应的是shadowsocks.json配置信息的路径

当完成安装之后，最后检查是否安装成功

```
$hashgard help
$hashgardcli help
```

## 方法2:下载可执行文件
[点击前往下载](https://github.com/hashgard/hashgard/releases)




