<script>
	import Orchestrator from './compo/Orchestrator.svelte'

	let start = false
	function handleKeydown(event) {
		if(event.keyCode == 32)
			start = true
	}
	function begin(){ start=true }
</script>

<svelte:window on:keydown={handleKeydown}/>

<div class="texturize"></div>
{#if !start}
<button id="info" on:click={begin}> Click here or press SPACE to start roadshow </button>
{/if}
<div id="octr">
	{#if start}
	<Orchestrator intervals = {[
		4000,  // SummonBison
		4000,  // SummonHippo
		2000,  // BisonHippo
		1000,  // FourGrid
		1000,  // TwelveGrid
		3000,  // Descent
		1000,  // Collide
		1000,  // Splash
		2000,  // SweetCirc
		2000,  // HippoSnap
		3000,  // BelugaSwim
		2000,  // HippoSnap
		5000,  // SwissMatchaRoll
		2000,  // BikeBlossom
		3000,  // DugongCalendar
		11000   // CasuallyRoadshow
	]} />
	<span id="secretSound">
		<audio controls autoplay>
			<source src="./jingle.mp3" type="audio/mpeg">
		</audio>
	</span>
	{:else}
	<Orchestrator />
	{/if}
</div>

<style>

#octr {
	position: absolute;
	z-index: 2;
	height: inherit;
	width: inherit;
	position: relative;
	display: grid;
}

#info{
	position: absolute !important;
	z-index: 20;
	bottom: 0;
	left: 0;
	position: relative;
	display: grid;
	font-size: 1.5em;
	margin: 1.5em;
	background-color: #547570;
	box-shadow: 0.06em 0.06em 0.2em 0.1em rgba(0,0,0,0.2);
}

#secretSound{
	display: none;
}

</style>