<script>
	import Orchestrator from './compo/Orchestrator.svelte';
</script>

<div class="texturize"></div>
<div id="info"> Press [some key] to do [something] </div>
<div id="octr">
	<Orchestrator intervals = {[
		4000,
		4000,
		2000,
		1000,
		1000,
		4000,
		1000,
		1000,
		2000,
		1000,
		3000,
		1000,
		3000,
		3000,
		3000,
		8000
	]} />
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

</style>