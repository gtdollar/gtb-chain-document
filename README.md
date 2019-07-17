#GTB 公链文档

GTB 公链以JSON RPC的方式提供API service，支持任意Ethereum Library连接到 GTB公链

```
公链RPC 地址: http://api.gttdollar.com:8545
Chain ID:1234
```
本文以 https://web3js.readthedocs.io/en/1.0/#来做展示

### 使用web3连接公链

```
var Web3 = require(“web3”);
var web3 = new Web3(new Web3.providers.HttpProvider("http://api.gttdollar.com:8545"));
```

### 使用web3创建钱包

```
var Web3 = require(“web3”);
var web3 = new Web3(new Web3.providers.HttpProvider(“http://api.gttdollar.com:8545”));
var accounts = web3.eth.accounts.create();
console.log(accounts);
```

### 使用web3发送交易

```

web3.eth.accounts.wallet.add(‘<privateKey>’);
web3.eth.sendTransaction({
    from: ‘0x75CEb30d2D61c2d8039f3282d3b4f0395670b765’,
    to: ‘0xb0dfc9aa515d935058da8fc44631ac055a3b7fb5’,
    value: ‘1’,
    gas: 2000000
}).then(function (receipt) {
    console.log(receipt);
});

```

### 使用 web3 查询余额

```
web3.eth.getBalance(currentAccount).then(console.log)
```
### Web socket 监听


GTB公链 web socket 没有开放给public access，需要使用 web socket 请提供 public ip 添加白名单
var web3 = new Web3(new Web3.providers.WebsocketProvider(“ws://api.gttdollar.com:8546”));
### gtb 公链 api

### 获得账户余额

http://api.gttdollar.com/data/balance/get?address=0xeAF9D0b79Ba340d96aE17D4D728374Fe526d8784

### 获得账户余额
http://api.gttdollar.com//transaction/history?tokenName=GTB&addr=GTB



