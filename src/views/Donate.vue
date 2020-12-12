<template>
	<div class="window white">
	        <fieldset class='poolsdialog donations'>
	            <legend>Donations</legend>
	        
	            <div :class="{selected: activeLink == 1}">
	                <a href='https://bscscan.com/address/0x7323B13669028780c6450A620064E30654a5Be2c'>1.<img class='icon ethicon' :src="publicPath + 'ethereum-brands_optimized.svg?rev=8160e2e87988f42e44fd33495dead52c'" /><span class='text'>0x28b88cfD875C883cDb61938C97B8d1baabf31c88</span></a>
	            </div>
	        
	        </fieldset>
	    </div>
</template>


<script>
//  Update to add the correct BSC links and create a gitcoin grants page

	export default {
		metaInfo: {
	      title: 'stablexswap.com :: Donate',
	      meta: [
	        {'property': 'og:title', 'content': 'stablexswap.com/donate'},
	        {'property': 'og:url', 'content': 'https://stablexswap.com/donate'},
	        {'property': 'og:type', 'content': 'website'},
	        {'property': 'og:description', 'content': 'StableXwap Smooth is an exchange liquidity pool on BSC designed for extremely efficient stablecoin trading'},
	        {'property': 'og:image', 'content': '/stablexswap.png'},
	        {'name': 'twitter:card', 'content': 'summary_large_image'},
	        {'name': 'twitter:title', 'content': 'stablexswap.com/donate'},
	        {'name': 'twitter:site', 'content': '@stablexswap'},
	        {'name': 'twitter:creator', 'content': '@stablexswap'},
	        {'name': 'twitter:description', 'content': 'StableXswap Smooth is an exchange liquidity pool on BSC designed for extremely efficient stablecoin trading'},
	        {'name': 'twitter:url', 'content': 'https://stablexswap.com/donate'},
	        {'name': 'twitter:image', 'content': '/stablexswap.png/donate'},
	      ]
	    },

	    data: () => ({
	    	activeLink: -1,
	    	keydownListener: null,
	    }),

	    computed: {
	    	publicPath() {
	    		return process.env.BASE_URL
	    	},
	    },

	    mounted() {
	    	this.keydownListener = document.addEventListener('keydown', this.handle_navigating)
	    },

	    beforeDestroy() {
			document.removeEventListener('keydown', this.handle_navigating);
	    },

	    methods: {
	    	handle_navigating(e) {
				if(this.activeLink == -1) return this.activeLink = 0
	            if(e.code == 'ArrowUp' && this.activeLink != 0) {
	                e.preventDefault();
	                this.activeLink--;
	            }
	            if(e.code == 'ArrowDown' && this.activeLink < 2) {
	                e.preventDefault();
	                this.activeLink++;
	            }
	            if(e.code.includes('Digit')) {
	                e.preventDefault();
	                var digit = e.code.slice(-1);
	                if(digit > 5) return;
	                this.activeLink = digit
	            }
	            if(e.code == 'Enter') {
	                e.preventDefault();
	                window.open(document.querySelector('.poolsdialog .selected a').href, '_blank', 'noopener,noreferrer')
	            }
			},
	    },

	}
</script>