<template>
	<div class='window white'>
		<fieldset class='devdialog donations'>
			<legend>Developer Docs</legend>
			<a href = "https://github.com/stablexlabs">
							</a>
		
		</fieldset>
		</div>
</template>

<script>
	export default {
		data: () => ({

		}),

		computed: {
			publicPath() {
				return process.env.BASE_URL
			},
		},
	}
</script>

<style scoped>
	legend {
		text-align: center;
	}
	.devdialog a {
		display: flex;
		align-items: center;
		padding: 0.1em;
	}
	.devdialog a img {
		margin-right: 10px;
	}
	.devdialog div {
		display: block;
		margin-top: 10px;
	}
	.devdialog a:hover {
	    background-color: blue;
    	color: white;
	}
</style>