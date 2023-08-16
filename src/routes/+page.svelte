<script>
	import { onMount } from 'svelte';
	import Vivus from 'vivus';

	onMount(() => {
		new Vivus('box', { duration: 500, type: 'oneByOne' }, () => {});
	});

	let activeButton = '';

	/**
	 * @param {string} className
	 */
	function buttonPressed(className) {
		let theDogs = document.getElementsByClassName(className);
		for (let dog of theDogs) {
			dog.classList.add('active');
			dog.classList.remove('cube-shadow');
		}
		activeButton = className;
	}

	function buttonReleased() {
		let theDogs = document.getElementsByClassName(activeButton);
		for (let dog of theDogs) {
			dog.classList.remove('active');
			dog.classList.add('cube-shadow');
		}
	}
</script>

<svelte:body on:mouseup={() => buttonReleased()} on:keyup={() => buttonReleased()} />

<div id="container">
	<div class="boxContainer">
		<svg
			version="1.1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			width="427"
			height="683"
			id="cube"
			class="boxPart"
			><defs
				><clipPath id="MreExmZsqeoV"
					><path
						fill="none"
						stroke="rgb(10,10,20)"
						d=" M 0 0 L 427 0 L 427 683 L 0 683 L 0 0 Z"
					/></clipPath
				></defs
			><g transform="scale(1,1)" clip-path="url(#MreExmZsqeoV)"
				><g>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 226.80714375198227 552.7646461601528 L 397.12459072617037 454.43182230191655 L 397.12459072617037 257.7661745854442 L 226.80714375198227 356.0989984436804 Z"
						fill-opacity="0.09803921568627451"
						id="right-bg"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 226.80714375198227 552.7646461601528 L 56.48969677779411 454.43182230191655 L 56.48969677779414 257.7661745854442 L 226.80714375198227 356.0989984436804 Z"
						fill-opacity="0.09803921568627451"
						id="left-bg"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 56.48969677779414 257.7661745854442 L 226.80714375198227 356.0989984436804 L 397.12459072617037 257.7661745854442 L 226.80714375198224 159.43335072720805 Z"
						fill-opacity="0.09803921568627451"
						id="top-bg"
					/>
					<!--
						-				-
						-	Buttons		-
						-				-
					-->
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 73.52144147521295 376.9529220379645 L 151.19257551740878 421.7963721854893 L 151.24421726519193 332.1392872674238 L 209.77539905456345 365.932280829504 L 209.77539905456342 523.2647990026818 L 73.52144147521295 444.59853991609293 Z"
						fill-opacity="0.09803921568627451"
						id="left-button-br"
						on:mousedown={() => buttonPressed('left-shadow-br')}
						on:keydown={() => buttonPressed('left-shadow-br')}
					/>
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 73.52144147521298 287.2660217429151 L 132.263167849406 321.18057327771834 L 132.33714206942864 389.13780345485446 L 73.52144147521295 355.180542884208 Z"
						fill-opacity="0.09803921568627451"
						id="left-button-tl"
						on:mousedown={() => buttonPressed('left-shadow-tl')}
						on:keydown={() => buttonPressed('left-shadow-tl')}
					/>
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 243.83888844940108 365.932280829504 L 302.2579697448923 332.2040085177419 L 302.2579697448923 399.6605531412661 L 243.83888844940108 433.5430289256001 Z"
						fill-opacity="0.09803921568627451"
						id="right-button-tl"
						on:mousedown={() => buttonPressed('right-shadow-tl')}
						on:keydown={() => buttonPressed('right-shadow-tl')}
					/>
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 243.83888844940108 455.8765560832039 L 302.2579697448923 422.0799820673956 L 302.2579697448923 489.5365266909198 L 243.83888844940108 523.2647990026819 Z"
						fill-opacity="0.09803921568627451"
						id="right-button-bl"
						on:mousedown={() => buttonPressed('right-shadow-bl')}
						on:keydown={() => buttonPressed('right-shadow-bl')}
					/>
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 321.69524343156706 478.3144114956058 L 380.0928460287516 444.59853991609293 L 380.0928460287516 287.2660217429151 L 321.69524343156706 320.98189332242794 Z"
						fill-opacity="0.09803921568627451"
						id="right-button-r"
						on:mousedown={() => buttonPressed('right-shadow-r')}
						on:keydown={() => buttonPressed('right-shadow-r')}
					/>
					<!-- svelte-ignore a11y-no-static-element-interactions -->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 90.55318617263177 257.7661745854442 L 226.80714375198224 179.09991549885524 L 363.0611013313328 257.7661745854442 L 226.80714375198227 336.43243367203314 Z"
						fill-opacity="0.09803921568627451"
						id="top-button"
						on:mousedown={() => buttonPressed('top-shadow')}
						on:keydown={() => buttonPressed('top-shadow')}
					/>
					<!-- 
						-							-
						-	Button Pressed Paths	-
						-							-
					-->
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 90.55318617263191 434.7652575302692 L 209.77539905456342 503.59823423103444 L 209.77539905456342 523.2647990026818 L 73.52144147521295 444.59853991609293 Z"
						fill-opacity="0.09803921568627451"
						id="left-shadow-br-b"
						class="cube-shadow left-shadow-br"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 90.55318617263191 434.7652575302692 L 90.55318617263191 386.78620442378826 L 73.52144147521295 376.9529220379645 L 73.52144147521295 444.59853991609293 Z"
						fill-opacity="0.09803921568627451"
						id="left-shadow-br-bl"
						class="cube-shadow left-shadow-br"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 90.55318617263171 345.34726049838446 L 132.31572074796367 369.45887107749314 L 132.33714206942864 389.13780345485446 L 73.52144147521295 355.180542884208 Z"
						fill-opacity="0.09803921568627451"
						id="left-shadow-tl-b"
						class="cube-shadow left-shadow-tl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 90.55318617263171 345.34726049838446 L 90.55318617263174 297.09930412873865 L 73.52144147521298 287.2660217429151 L 73.52144147521295 355.180542884208 Z"
						fill-opacity="0.09803921568627451"
						id="left-shadow-tl-l"
						class="cube-shadow left-shadow-tl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 226.80714375198224 179.09991549885524 L 226.80714375198224 198.76648027050248 L 107.58493087005056 267.59945697126784 L 90.55318617263177 257.7661745854442 Z"
						fill-opacity="0.09803921568627451"
						id="top-shadow-l"
						class="cube-shadow top-shadow"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 226.80714375198224 179.09991549885524 L 226.80714375198224 198.76648027050248 L 346.029356633914 267.5994569712678 L 363.0611013313328 257.7661745854442 Z"
						fill-opacity="0.09803921568627451"
						id="top-shadow-r"
						class="cube-shadow top-shadow"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 380.0928460287516 444.59853991609293 L 380.0928460287516 287.2660217429151 L 363.0611013313328 297.09930412873865 L 363.0611013313329 434.7652575302694 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-r-r"
						class="cube-shadow right-shadow-r"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 380.0928460287516 444.59853991609293 L 321.69524343156706 478.3144114956058 L 321.69524343156706 458.64784672395854 L 363.0611013313329 434.7652575302694 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-r-b"
						class="cube-shadow right-shadow-r"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 302.2579697448923 332.2040085177419 L 285.22622504747346 342.0372909035655 L 285.22622504747346 389.8272707554425 L 302.2579697448923 399.6605531412661 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-tl-r"
						class="cube-shadow right-shadow-tl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 302.2579697448923 399.6605531412661 L 243.83888844940108 433.5430289256001 L 243.83888844940108 413.72226068138093 L 285.22622504747346 389.8272707554425 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-tl-b"
						class="cube-shadow right-shadow-tl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 302.2579697448923 422.0799820673956 L 285.22622504747346 431.9331774193241 L 285.2262250474735 479.7032443050961 L 302.2579697448923 489.5365266909198 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-bl-r"
						class="cube-shadow right-shadow-bl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 302.2579697448923 489.5365266909198 L 243.83888844940108 523.2647990026819 L 243.83888844940108 503.5982342310346 L 285.2262250474735 479.7032443050961 Z"
						fill-opacity="0.09803921568627451"
						id="right-shadow-bl-b"
						class="cube-shadow right-shadow-bl"
					/>
					<path
						fill="rgb(153,51,0)"
						stroke="rgb(10,10,20)"
						paint-order="stroke fill markers"
						fill-rule="evenodd"
						d=" M 151.19257551740878 421.7963721854893 L 168.2243202148276 411.9630897996657 L 168.26463794790675 341.9660317303098 L 151.24421726519193 332.1392872674238 Z"
						fill-opacity="0.09803921568627451"
						id="left-shadow-br-tl"
						class="cube-shadow left-shadow-br"
					/>
				</g></g
			></svg
		>
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

	.cube-shadow {
		opacity: 0;
	}

	.active {
		opacity: 1 !important;
	}
</style>
