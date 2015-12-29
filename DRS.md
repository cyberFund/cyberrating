# Decentralized Reporting Specification Draft

A work in progress. Feedback appriciated.

## Market Report
Is used to report on last observed price for one market.

```json
v: 1
// Version of DRS

timestamp: 1247592834
// Unix timestamp

sourse: “http://poloniex.com”
// If third party provider - full domain name. If a blockchain - name from Chaingear

base: “Bitcoin” 
// Should match with name from Chaingear

quote: “US”
// Should match with name from Chaingear

last: 240.677453
// Ratio between base and quote

volume: 2900 // Volume in quote tokens for last 24 hours
```

## Block Report
Is used to report on a state of particular chain.
```
v: 1
timestamp: 1247592834
system: Bitcoin
source: “blockchain.info”
height: 284634
hash: 84139b817…..
previous: 
root: 4fc12b6d36fa
supply: 15004588
budget: 0
investments: 25
revenue: 2 {
  txs: 1000;
  value: 2500;
  }
costs: 27 {
  mining: 27 {
  	consensus: “proof-of-work”
    algorithm: “SHA-256”
    difficulty: 365123800
    miner: 21.co;
    }
  }
```

## Chain Report
Is used to report on a valuated state of a particular chain.
```
v: 1
timestamp: 1247592834
system: Bitcoin
height: 284634
hash: 84139b817…..
previous: 
root: 4fc12b6d36fa
supply: 15004588
wvap: {
  btc: 0.2,
  usd: 100
}
cap: {
  btc: 1000,
  usd: 500000
}
budget: {
  btc: 10,
  usd: 500
}
investments: {
  btc: 500,
  usd: 1
}
revenue: 2 {
  txs: 1000;
  value: { 
    btc: 500,
    usd: 12500
  },
  avarage: { 
    btc: 500,
    usd: 12500
  },
  margin: { 
    btc: 500,
    usd: 12500
  },
costs: 27 {
  mining: { 
    btc: 500,
    usd: 12500
    },
  }
```
