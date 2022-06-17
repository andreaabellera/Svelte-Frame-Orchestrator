<script>
    import Bison from "casually-css/@svelte/bison.svelte"
    import { bounceOut } from 'svelte/easing'
    import { fly } from 'svelte/transition'

    // Pop out
    function zoom({ duration }) {
		return {
			duration,
			css: t => {
				const eased = bounceOut(t);
				return `transform: translate(-50%, -50%) scale(${eased});`
			}
		}
	}

    // Box transition
    let boxText="create( thisBox, 'bison' )"
    $: currText = ""
    let visCode = true
    let totalTime = 1200
    let tick = totalTime / boxText.length / 2
    let i = 0
    let id1 = setInterval(next, totalTime)
    setInterval(() => {
        if (i < boxText.length) {
            currText += boxText[i]
            i++
        }
    }, tick)
    function next() {
        visCode = false
        clearInterval(id1)
    }
</script>

<link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@200;300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<div id="reelCtr">
    {#if visCode}
    <div id="codeCtr" class="box" out:zoom="{{duration: 800}}">
        <div id="code"><span>{currText}</span></div>
    </div>
    {:else}
    <div id="bisonCtr" class="box" in:fly="{{ y: -2000, duration: 600 }}">
        <Bison />
    </div>
    {/if}
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
    }
    #codeCtr{
        background-image: linear-gradient(204deg, #E6E6EE 0%, #f0f9fa 60%, #F0FFF1 75%, #FFFFFF 100%);
        box-shadow: 0.05em 0.15em 0.5em rgba(0,0,0,0.3);
    }
    .box{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: 50vh;
        width: 40vw;
        display: grid;
        justify-items: center;
        align-items: center;
        border-radius: 0.08em;
    }
    #code{
        position: absolute;
        height: 39vh;
        width: 35vw;
        font-size: 56px;
        display: grid;
        justify-items: center;
        align-items: center;
        padding: 0.5em;
        color: #3e3e3e;
        font-family: 'Work Sans', sans-serif;
    }
</style>


