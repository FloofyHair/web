<script>
</script>

<div id="container">
	<slot />
	<div id="duneContainer" />
</div>

<style>
	:global(html),
	:global(body) {
		border: 0;
		padding: 0;
		margin: 0;
		background-color: wheat;
	}


	#duneContainer {
		position: fixed;
		height: 33vh;
		width: 100vw;
		bottom: 0;
		margin: 0;
		background-image: url( dune.svg );
		background-size: cover;
	}

	#container {
		width: 100vw;
		height: 100vh;
	}
</style>
