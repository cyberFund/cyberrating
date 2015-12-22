# Decentralized Reporting specification v1

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
v: 1
timestamp: 1247592834
system: Bitcoin
height: 284634
hash: a469bb242…..
previous: 84139b817…..
root: 6d36fa4fc12b
supply: 15004588

## Chain Report
v: 1
timestamp: 1247592834
system: Bitcoin
calculated data
