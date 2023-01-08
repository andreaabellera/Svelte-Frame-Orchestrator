<script>
	/*=============================================
		Import Orchestrator component
	===============================================*/
	import Orchestrator from './Orchestrator.svelte'
	
	/*=============================================
		Import individual frame components to load
	===============================================*/
	import Empty from './frames/_Empty.svelte'  // Default unstarted frame
    import SummonBison from './frames/SummonBison.svelte'
    import SummonHippo from './frames/SummonHippo.svelte'
    import BisonHippo from './frames/BisonHippo.svelte'
    import FourGrid from './frames/FourGrid.svelte'
    import TwelveGrid from './frames/TwelveGrid.svelte'
    import Descent from './frames/Descent.svelte'
    import Collide from './frames/Collide.svelte'
    import Splash from './frames/Splash.svelte'
    import SweetCirc from './frames/SweetCirc.svelte'
    import HippoSnap from './frames/HippoSnap.svelte'
	import HippoSnapReverse from './frames/HippoSnapReverse.svelte'
    import BelugaSwim from './frames/BelugaSwim.svelte'
    import SwissMatchaRoll from './frames/SwissMatchaRoll.svelte'
    import BikeBlossom from './frames/BikeBlossom.svelte'
    import DugongCalendar from './frames/DugongCalendar.svelte'
    import CasuallyRoadshow from './frames/CasuallyRoadshow.svelte'

	/*=======================
		Import reel audio
	=========================*/
	let audioPath = '/jingle.mp3'

	/*=============================================
		reel
		  Defines the sequence of frames and duration they stay on screen
		  Frame attributes:
			. component: .svelte component - component name to load into window  
			. duration: integer - time to display component in milliseconds 
	===============================================*/
	let reel = [
		// Every row below is a 'frame', a single entry played on the resulting video reel
		{ component: SummonBison, duration: 4000 },
		{ component: SummonHippo, duration: 4000 },
		{ component: BisonHippo, duration: 2000 },
		{ component: FourGrid, duration: 1000 },
		{ component: TwelveGrid, duration: 1000 },
		{ component: Descent, duration: 3000 },
		{ component: Collide, duration: 1000 },
		{ component: Splash, duration: 1000 },
		{ component: SweetCirc, duration: 2000 },
		{ component: HippoSnap, duration: 2000 },
		{ component: BelugaSwim, duration: 3000 },
		{ component: HippoSnapReverse, duration: 2000 },
		{ component: SwissMatchaRoll, duration: 5000 },
		{ component: BikeBlossom, duration: 2000 },
		{ component: DugongCalendar, duration: 3000 },
		{ component: CasuallyRoadshow, duration: 11000 }
	]
    
	// Display Empty while reel is either empty or unstarted
	let currFrame = -1

	// Other states
	let sound = false
	let hideInfo = false
	let frameStarts = []
	let endReel

	// Play frames sequentially as defined under 'reel' 
	function begin(){ 
		hideInfo = true
		setTimeout(play, 1000)  // Intermission delay before showing first frame; Defaults to 1 second
		
		function play(){
			currFrame++
			let startTime = 0
			for (let frame of reel) {
				startTime += frame.duration
				let fs = setInterval(() => { 
					currFrame++
					clearInterval(fs)
				}, startTime)
				frameStarts.push(fs)
			}
		}

		// Compute total reel time
		let totalLength = 0
		for (let frame of reel){ totalLength += frame.duration }

		// When last frame finishes playing, reset reel to unstarted state
		endReel = setInterval(reset, totalLength)
	}

	// Reset all intervals and interface components to unstarted state
	function reset(){
		clearInterval(endReel)
		for(let fs of frameStarts)
			clearInterval(fs)
		hideInfo = false
		currFrame = -1
	}

	/*==========================
		User keyboard controls
	============================*/
	function handleKeydown(event) {
		
		// SPACE will trigger reel start/restart
		if(event.keyCode == 32){
			if(currFrame >= 0)
				reset()
			else
				begin()
		}

		// Mute/unmute music reel audio
		if(event.keyCode == 83)
			sound = !sound
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
	<Orchestrator>

		{#if currFrame >= 0 && reel.length > 0}
			<svelte:component this={ reel[currFrame].component }/>
			<span id="secretSound">
				<audio controls autoplay muted={!sound}>
					<source src={audioPath} type="audio/mpeg">
				</audio>
			</span>
		
		{:else}
			<Empty />
		{/if}

	</Orchestrator>
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