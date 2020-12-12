# StableXSwap Part 2: Smooth

<p align="center">
  <!-- <img src="" /> Add Logo Here -->
</p>

# Smooth FAQ

## What is Smooth?
Smooth is an exchange liquidity pool on Binance Smart Chain designed for (1) extremely efficient stablecoin trading (2) low risk, supplemental fee income for liquidity providers, without an opportunity cost. As a fork of Curve, deployed on BSC, the project aims to provide even more efficiency for swaps with lower fees, shorter blocktimes, and less frontrunning.

Smooth allows users (and smart contract aggregators) to trade between stablecoins at lower slippages. Behind the scenes, the liquidity pools' underlying stablecoins can earn interest from lending products 

## Has Smooth been audited?
Smooth has not yet been audited. Our v1 swap,  a Sushiswap/Uniswap based fork, has been audited. Please don’t supply your life savings, or assets you can’t afford to lose, to Smooth, especially as a liquidity provider.

Using Smooth as an exchange user should be significantly less risky, as you are not depositing into the pools, but please proceed at your own caution.

## How do I trade on Smooth?
Before trading, you’ll have to approve Smooth to interact with your BUSD or USDT balance, similar to most DeFi applications.

On the exchange, select the asset you would like to convert (e.g. BUSD), and the quantity (e.g. 1,000) - the exchange rate, and quantity that you will receive (including and all slippage and fees) will be displayed. The exchange rate might surprise you - that’s the power of Smooth.

## How do I provide liquidity to Smooth?
Smooth will work on integrating interest-bearing tokens in the future.

Before providing liquidity, you’ll have to approve Smooth to interact with your interest-bearing tokens.

Visit the Smooth deposit page, and your available balances should appear. If you add all coins in a balanced proportion, you will provide tokens at the current exchange Smooth rate; this requires you to have both assets in your wallet. You can uncheck this feature to supply one side of the market, or a different ratio of assets, and Smooth will automatically exchange them into the proper quantity (with the same low slippage & fees of the Smooth exchange) - magic!

## What's "Use maximum amount of coins available"?
This means using all USDC and DAI in your wallet. This way is recommended only if you have much less coins than currently in liquidity pool. Please be wary of depositing too much leading to too high slippage.

## How to withdraw liquidity I provided?
Go to the withdraw page. If you want to withdraw some percentage of your liquidity (the preferred way), type that percentage in the top field. You can, however, withdraw in a form of individual coins (USDC, DAI), having the exchange happening for you, if you type amounts in lower fields. You'll get charge with the exchange fee in the latter case.



# smooth-vue

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).