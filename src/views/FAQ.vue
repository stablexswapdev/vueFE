<template>
	<div class="window white">
        <h2>StableXSwap FAQ</h2>
        <h3>What is StableXSwap?</h3>


        <h3>Has StableXswap been audited?</h3>
        <p>StableXswap is a fork of Curve. Curve smart contracts were <router-link to="/audits">Audited</router-link> by
        Trail of Bits.</p>
        <p>However, security audits don't eliminate risks completely.
        Please don’t supply your life savings, or assets you
        can’t afford to lose, to Curve, especially as a liquidity
        provider.</p>

        <p>Using StableXswap as an exchange user should be significantly less
        risky, but this is not advice.</p>

        <h3>
            <router-link to="/bugbounty">Bug bounty</router-link>
        </h3>

        <h3>Source code git</h3>
        <p>
            <a href="https://github.com/stablexlabs">Smart contracts</a>
        </p>
   

        <h3>How do I trade on StableXswap?</h3>
        <p>Before trading, you’ll have to approve StableXswap to interact with
        your stablecoin balances, similar to most DeFi applications.</p>

        <p>On the <a href="/">exchange</a>, select the asset you would like to convert (e.g.
        BUSD), and the quantity (e.g. 1,000) - the exchange rate, and
        quantity that you will receive (including and all slippage and fees)
        will be displayed. The exchange rate might surprise you - that’s the
        power of StableXswap.</p>

        <h3>Fees</h3>
        <p>
            Currently the fee on all pools is 0.035%, of which 0.025% goes to buy back STAX and give to STAX stakers, 
            and 0.01% which goes to liquidity providers. There is no admin fee.
        </p>
     

        <h3>How do I provide liquidity to StableXswap?</h3>

    
        <p>Before providing liquidity, you’ll have to approve StableXswap to
        interact with your cDAI or cUSDC balances.</p>

        <p>Visit the <router-link to="deposit">StableXswap deposit page</router-link>, and your available balances should
        appear. If you <b>add all coins in a balanced proportion</b>, you will
        provide coins at the current exchange StableXswap rate; this requires
        you to have all assets in your wallet. You can uncheck this feature
        to supply one side of the market, or a different ratio of assets,
        and Curve will automatically exchange them into the proper quantity
        (with the same low slippage & fees of the StableXswap exchange) -
        magic!</p>

        <p>
            You can deposit plain stablecoins DAI/USDC/USDT/BUSD/QUSD or their interest-bearing Tokens by clicking "Deposit wrapped"
        </p>

        <h3>What's "Use maximum amount of coins available"?</h3>
        <p>This means using all USDC and DAI in your wallet. This way is
        recommended only if you have much less coins than currently in
        liquidity pool.</p>

        <h3>What's "Infinite approval - trust this contract forever"?</h3>
        <p>This means that you preapprove the contract to to be able to spend any amount of your coins when you interact with it.
        This means that you won't be asked every time to appove the amount of coins you want to transfer to the contract.
        </p>

        <h3>How to withdraw liquidity I provided?</h3>
        <p>Go to <router-link to="withdraw">the withdraw page</router-link>. If you want
        to withdraw some percentage of your liquidity (the preferred way),
        type that percentage in the top field.
        You can, however, withdraw in a form of individual coins (BUSD, USDC,
        DAI), having the exchange happening for you, if you type amounts in
        lower fields. You'll get charged with the exchange fee in the latter
        case.</p>
    </div>
</template>

<style scoped>
    .window.white a {
        border-bottom: 1px dashed gray;
    }
    .window.white a:hover {
        border-bottom: none;
    }
</style>