<script>
	import Orchestrator from './compo/Orchestrator.svelte'

	let empty = []
	let myIntervals = [
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
	]

	$: reel = empty

	let sound = false
	let hideInfo = false
	let start = false

	function handleKeydown(event) {
		if(event.keyCode == 32)
			start = true
		if(event.keyCode == 83)
			sound = !sound
	}

	function begin(){ 
		hideInfo = true
		
		let intermissionDelay = setInterval(go, 1000)
		function go(){
			start = true
			reel = myIntervals
			clearInterval(intermissionDelay)
		}

		let totalLength = myIntervals.reduce((a, b) => a + b, 0)

		let endReel = setInterval(resetReel, totalLength)
		function resetReel(){
			reset()
			clearInterval(endReel)
		}
	}

	function reset(){
		start = false
		hideInfo = false
		reel = empty
	}

</script>

<svelte:window on:keydown={handleKeydown}/>

<div class="texturize"></div>

{#if !hideInfo}
	<button id="info" on:click={begin}> 
		Press SPACE or click here to start <br>
		Press s to toggle sound on/off
	</button>
{/if}

<div id="octr">
	{#if start}
		<Orchestrator intervals={reel} />
		
		<span id="secretSound">
			<audio controls autoplay muted={!sound}>
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
	margin: 1.8em;
	background-color: #547570;
	box-shadow: 0.06em 0.06em 0.2em 0.1em rgba(0,0,0,0.2);
	text-align: left;
}

#secretSound{
	display: none;
}

</style>