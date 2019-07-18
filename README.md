#GTB Chain Document

The GTB public chain provides API services in the form of JSON RPC, supporting any Ethereum library to connect to the GTB public chain.

```
RPC Address: http://api.gttdollar.com:8545
Chain ID:1234
```
This article is shown at [web3js](https://web3js.readthedocs.io/en/1.0/#)

### Use web3 to connect the public chain

```
var Web3 = require(“web3”);
var web3 = new Web3(new Web3.providers.HttpProvider("http://api.gttdollar.com:8545"));
```

### Create a wallet using web3

```
var Web3 = require(“web3”);
var web3 = new Web3(new Web3.providers.HttpProvider(“http://api.gttdollar.com:8545”));
var accounts = web3.eth.accounts.create();
console.log(accounts);
```

### Send a transaction using web3

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

### Check balance using web3

```
web3.eth.getBalance(currentAccount).then(console.log)
```

### Web socket listener using web3

GTB public chain web socket is not open to public access, need to use web socket Please provide public ip add whitelist

```
var web3 = new Web3(new Web3.providers.WebsocketProvider("ws://api.gttdollar.com:8546"));
```
##gtb 公链 api

### Get account balance

```
http://api.gttdollar.com/data/balance/get?address=0xeAF9D0b79Ba340d96aE17D4D728374Fe526d8784
```

### Get account transaction history
```
http://api.gttdollar.com//transaction/history?tokenName=GTB&addr=GTB
```



