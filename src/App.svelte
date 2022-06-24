<script>
	import Orchestrator from './compo/Orchestrator.svelte'

	let start = false
	function handleKeydown(event) {
		if(event.keyCode == 32)
			start = true
	}
</script>

<svelte:window on:keydown={handleKeydown}/>

<div class="texturize"></div>
{#if !start}
<div id="info"> Press SPACE to start orchestrator </div>
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
		8000   // CasuallyRoadshow
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
	bottom: 2.5ex;
	left: 2ex;
	position: relative;
	display: grid;
	font-size: 2em;
}

#secretSound{
	display: none;
}

</style>