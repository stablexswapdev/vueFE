<template>
	<div class="window white">
        <h2>
            Risks of using 
            <img :src="publicPath + 'logo.png'" class='icon'> {{ currentPool }} pool
        </h2>
        
        <ul class='poolrisks' v-show="['compound', 'pax', 'iearn', 'y', 'busd'].includes(currentPool)">
        	<li>Smart contract issues with lending protocols</li>
			<li>Smart contract issues with StableXswap</li>
			<li>Systemic issues with the stable coins in those pools</li>
        </ul>
        <ul class='poolrisks' v-show="['ren'].includes(currentPool)">
			<li>Smart contract issues with Curve</li>
			<li>Systemic issues with renBTC or wBTC</li>
        </ul>
        <risks></risks>

    </div>
</template>

<script>
	import { getters } from '../contract'

    import Risks from './Risks'

    export default {
        components: {
            Risks,
        },
        computed: {
          publicPath() {
            return process.env.BASE_URL
          },
          currentPool() {
          	return getters.currentPool()
          },
        },
    }
</script>

<style scoped>
    h2 {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
    }

    h2 img {
        margin-left: 0.7em;
        margin-right: 0.3em;
    }

    @media only screen and (max-device-width: 470px) {
        h2 img {
            margin-left: 0;
        }
    }
    .window.white a {
        border-bottom: 1px dashed gray;
    }
    .window.white a:hover {
        border-bottom: none;
    }
    .poolrisks li {
    	margin-top: 0.4em;
    }
</style>