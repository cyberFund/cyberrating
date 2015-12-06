# Scoring Coefficients

Scoring coefficients depend on a stage of development and associated chaingear type:
![scoring_table](scoring.png)

## Chaingear

Scoring coefficients depend on a stage of development and associated chaingear type:
![chaingear_scoring](chaingear_scoring.png)

## Blockchain Reporting

In development

## Automation

Ease of integration is evaluated. At this point of time we evaluate only integration with library that allow crosschain update of balances (trusted). In a future we are going to extend it with emerging libs.

Scoring:
- 0.5 score. If integration with [Quantum library](https://github.com/cyberFund/quantum) is `true`

## Weighted Liquidity

Daily turnover grade is evaluated against market cap grade.

Turnover scoring:
- `0` score. `Illiquid` grade if daily turnover is 0%
- `0.1` score. `Very Low` grade if daily turnover is <= 0.01%
- `0.2` score. `Low` grade if daily turnover is >0.01% and <= 0.1%
- `0.3` score. `Normal` grade if daily turnover is >0.1% and <= 0.5%
- `0.4` score. `High` grade if daily turnover is >0.5% and <= 2%
- `0.5` score. `Very High` grade if daily turnover is >2%

Cap scoring:
- `0` score. `Pico` grade if cap is <= $10k
- `0.1` score. `Nano` grade if cap is <= $100k
- `0.2` score. `Micro` grade if cap is <= $1M
- `0.3` score. `Kilo` grade if cap is <= $10M
- `0.4` score. `Mega` grade if cap is <= $1B
- `0.5` score. `Giga` grade if cap is > $1B

Calculation example:
```
Daily trade volume of bitcoins is `100000`

USD/BTC price is `$300`

Total Supply is `15000000`

Cap is `300 * 15000000` = `$4.5B`

Cap Grade is `Giga` and score is `0.5`
Daily turnover is `100000 * 300 / 4.5B` = `~0.67%`
Turnover grade is `High` and score is `0.4`
```

## People's Love

At this point of time we use simple centralized metrics to calculate people's love. cyber•Fund have a mechanism of starring systems that allow simplified evaluation. Eventually we want to develop rating system that don't rely on centralized third parties, but now there is no better alternative exist.

Scoring:
To calculate a score we use a ratio between quantity of stars of system we evaluate and quantity of stars of the most starred system. For the most starred system a score is always max.

Calculation example:
We want to calculate a rating of Ethereum. Bitcoin is the most starred system with 50 stars. Ethereum has 40 stars. Ethereum is in `Public` stage thus max score for Love is 2.
`40 / 50 * 2` = `1.6`
So Ethereum will have a love score of 1.6
