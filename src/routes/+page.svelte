<script>
	import { onMount } from 'svelte';
	import Vivus from 'vivus';

	onMount(() => {
		new Vivus('box', { duration: 500, type: 'oneByOne' }, () => {});
	});
</script>

<div id="container">
	<div class="boxContainer">
		<svg
			viewBox="0 0 22 25"
			version="1.1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			stroke-linecap="round"
			stroke-linejoin="round"
			fill-rule="evenodd"
			xml:space="preserve"
			id="box"
			class="boxPart"
		>
			<g id="cube" class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					fill="transparent"
					points="1.1805,6.83071 1.1805,18.1693 11,23.8386 20.8195,18.1693 20.8195,6.83071 11,1.16142 "
				/><!-- Cube outline -->
				<polyline points="1.1805,6.83071 11,12.5 20.8195,6.83071 " /><!-- Top Connector -->
				<polyline points="11,12.5 11,23.8386 " /><!-- Bottom Connector -->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeTop0"
					fill="transparent"
					points="11,2.15476 2.81708,6.83071 11,11.3661 18.937,6.83071 "
				/><!-- Top -->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeRight0"
					fill="transparent"
					points="15.5006,15.0984 11.8183,17.2244 11.8183,12.9724 15.5006,10.8465 "
				/><!-- Right / Top Left -->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeRight1"
					fill="transparent"
					points="15.5006,20.2953 11.8183,22.4213 11.8183,18.1693 15.5006,16.0433 "
				/><!-- Right / Bottom Left-->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeRight2"
					fill="transparent"
					points="20.0012,8.24803 16.3189,10.374 16.3189,14.626 16.3189,19.8228 20.0012,17.6969 "
				/><!-- Right / Right -->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeLeft0"
					fill="transparent"
					points="1.99879,12.5 1.99879,8.24803 5.6811,10.374 5.6811,14.626 "
				/><!-- Left / Top Left -->
			</g>
			<g class="cubePart" fill="none" stroke="rgb(10,10,20)" stroke-width="0.07">
				<polygon
					id="cubeLeft1"
					fill="transparent"
					points="1.99879,17.6969 1.99879,13.4449 6.4994,16.0433 6.4994,10.8465 10.1817,12.9724 10.1817,22.4213 "
				/><!-- Left / Left -->
			</g>
		</svg>
	</div>
	<div class="boxContainer">
		<svg
			viewBox="0 0 22 26"
			version="1.1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			stroke-linecap="round"
			stroke-linejoin="round"
			fill-rule="evenodd"
			xml:space="preserve"
			id="boxPressed"
			class="boxPart"
			style="opacity: 0;"
		>
			<g fill="red" stroke="rgb(0,0,0)" stroke-width="0.07">
				<g
					><polyline
						points="14.846,16.9707 14.846,20.4668 15.5006,20.8448 11.8183,22.9707 11.8183,18.7188 15.5006,16.5928 15.5006,20.8448 "
					/> <polyline points="14.846,20.4668 11.8183,22.2148 " />
					<!-- Right / Bottom Left --></g
				>
				<g
					><polygon
						points="20.0012,8.79752 16.3189,10.9235 16.3189,15.1755 16.3189,20.3723 20.0012,18.2463 "
					/><polyline
						points="16.3189,19.6164 19.3466,17.8684 20.0012,18.2463 19.3466,17.8684 19.3466,9.17547 "
					/><!-- Right / Right --></g
				>
				<g
					><polygon points="2.81708,7.3802 11,2.55504 19.1781,7.27946 10.9952,12.1046 " />
					<polyline points="11,2.55504 11,3.31095 18.5306,7.66129 " />
					<polyline points="11,3.31095 3.46462,7.75427 " />
					<!-- Top --></g
				>
				<g
					><polygon
						points="1.99879,13.0495 1.99879,8.79752 5.6811,10.9235 5.6811,15.1755 "
					/><polyline points="2.67921,9.19036 2.67921,12.7202 5.6811,14.4534 " />
					<polyline points="1.99879,13.0495 2.67921,12.7202 " />
					<!-- Left / Top Left --></g
				>
				<g fill="green" style="opacity: 1;">
					<polyline
						points="14.846,11.7739 14.846,15.27 15.5006,15.6479 11.8183,17.7739 11.8183,13.5219 15.5006,11.3959 15.5006,15.6479 14.846,15.27 11.8183,17.018 "
					/><!--Right / Top Left--></g
				>
				<g
					><polyline
						points="6.4994,16.5928 6.4994,11.3959 10.1817,13.5219 10.1817,22.9707 1.99879,18.2463 1.99879,13.9944 6.4994,16.5928 7.17982,16.2635 7.17982,11.7888 "
					/><polyline points="1.99879,18.2463 2.67921,17.9171 10.1817,22.2486 " />
					<polyline points="2.67921,17.9171 2.67921,14.3872 " />

					<!-- Left / L --></g
				>
			</g>
			<g fill="none" stroke="rgb(0,0,0)" stroke-width="0.07">
				<polyline
					points="11,24.3881 1.1805,18.7188 1.1805,7.3802 11,13.0495 11,24.3881 20.8195,18.7188 20.8195,7.3802 11,13.0495 "
				/><!-- Left & Right Fill -->
				<polyline points="20.8195,7.3802 10.9422,1.61193 1.1805,7.3802 " /><!-- Top Fill-->
			</g>
		</svg>
	</div>
</div>

<style>
	:global(html),
	:global(body) {
		overflow: hidden;
		border: 0;
		padding: 0;
		margin: 0;
	}
	#container {
		width: 100vw;
		height: 100vh;
		background-color: wheat;
	}
	.boxContainer {
		position: fixed;
		width: 100%;
		height: 100%;
	}
	.boxPart {
		width: 50rem;
		height: 50rem;
		fill: transparent;
		display: block;
		margin: auto;
	}
	#box {
		margin-top: 1rem;
	}
	#boxPressed {
		width: 52rem;
		height: 52rem;
	}

	#cubeTop0:hover {
		fill: cyan;
	}
	#cubeLeft0:hover {
		fill: red;
	}
	#cubeLeft1:hover {
		fill: green;
	}
	#cubeRight0:hover {
		fill: yellow;
	}
	#cubeRight1:hover {
		fill: blue;
	}
	#cubeRight2:hover {
		fill: orange;
	}
</style>
