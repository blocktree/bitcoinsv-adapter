# bitcoinsv-adapter

bitcoinsv-adapter继承了bitcoin-adapter，主要修改了如下内容：

- 重写了Symbol = "BSV"。
- 重写了addressDecoder，实现了BSV地址编码。
- 交易启用ForkID

## 如何测试

openwtester包下的测试用例已经集成了openwallet钱包体系，创建conf文件，新建BSV.ini文件，编辑如下内容：

```ini

# RPC Server Type，0: CoreWallet RPC; 1: Explorer API
rpcServerType = 0
# node api url, if RPC Server Type = 0, use bitcoin core full node
serverAPI = "http://ip:port/"
# RPC Authentication Username
rpcUser = "user"
# RPC Authentication Password
rpcPassword = "password"
# Is network test?
isTestNet = false
# support segWit
supportSegWit = false
# minimum transaction fees
minFees = "0.001"
# Cache data file directory, default = "", current directory: ./data
dataDir = ""

```

## 资料介绍

### 区块浏览器

https://explorer.viabtc.com/bsv
