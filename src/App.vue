<template>
  <div id="app">
    <router-view></router-view>
  </div>
  
</template>

<script>
    import { getters, contract as currentContract } from './contract'
    import { capitalizeFirstLetter } from './utils/helpers'

    const descriptions = {
    	compound: 'A stablexswap.com portal for swapping cDAI/cUSDC',
    	usdt: 'A stablexswap.com Tethered portal for swapping cDAI/cUSDC/USDT',
    	iearn: 'A stablexswap.com yTokens portal for swapping DAI/USDC/USDT/TUSD',
    	busd: 'A stablexswap.com portal for swapping BUSD and other stablecoins',
    }

    const titles = {
    	compound: 'Compounded',
    	usdt: 'Tethered',
    	iearn: 'Yield',
    	busd: 'bUSD',
    	susd: 'sUSD-yCurve old',
    	susdv2: 'sUSD',
        pax: 'PAX',
        ren: 'renBTC',
    }

	export default {
		metaInfo() {
			return {
                title: "stablexswap.com",
				meta: [
					{'property': 'og:title', 'content': 'stablexswap.com/' + this.currentPool},
					{'property': 'og:url', 'content': 'https://stablexswap.com/' + this.currentPool},
					{'property': 'og:type', 'content': 'website'},
					{'property': 'og:description', 'content': descriptions[this.currentPool]},
					{'property': 'og:image', 'content':  '/stablexswap' + this.currentPool + '_preview.png'},
					{'name': 'twitter:card', 'content': 'summary_large_image'},
					{'name': 'twitter:title', 'content': 'stablexswap.com/' + this.currentPool},
					{'name': 'twitter:site', 'content': '@stablexswap'},
					{'name': 'twitter:creator', 'content': '@stablexswap'},
					{'name': 'twitter:description', 'content': descriptions[this.currentPool]},
					{'name': 'twitter:url', 'content': 'https://stablexswap.com/' + this.currentPool},
					{'name': 'twitter:image', 'content': this.currentPool + '/_preview.png'},
				]
			}
		},
        computed: {
          ...getters,
        },
	}
</script>


