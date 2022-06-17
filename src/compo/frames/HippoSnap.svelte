<script>
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import { fade } from 'svelte/transition';

    export let flip = false
    let isFlip = "notFlip"
    let shads = [true,false,false,false,false,false]

    let id1 = setInterval(next, 100)
    let tick = 1
    let untick = 0
    function next() {
        shads[tick] = true
        if(tick > 10){
            shads[untick] = false
            untick++
            if(untick == 4){
                clearInterval(id1)
                tick = 1
                untick = 0
            }
        }
        tick++
    }

    if (flip)
        isFlip = "flip"


</script>

<div id="reelCtr" class={isFlip}>
    {#if shads[0]}
    <div id="hippoCtr" out:fade>
        <Hippo 
            snap={{iterationCount:"1",delay:"0.2s","duration":"2s"}}
            bouncing={{iterationCount:"0"}}
            whip={{iterationCount:"0"}}
        />
    </div>
    {/if}
    {#if shads[1]}
    <div id="shad1" class="shad" out:fade>
        <Hippo 
            snap={{iterationCount:"1",delay:"0.2s","duration":"2s"}}
            bouncing={{iterationCount:"0"}}
            whip={{iterationCount:"0"}}
        />
    </div>
    {/if}
    {#if shads[2]}
    <div id="shad2" class="shad" out:fade>
        <Hippo 
            snap={{iterationCount:"1",delay:"0.2s","duration":"2s"}}
            bouncing={{iterationCount:"0"}}
            whip={{iterationCount:"0"}}
        />
    </div>
    {/if}
    {#if shads[3]}
    <div id="shad3" class="shad" out:fade>
        <Hippo 
            snap={{iterationCount:"1",delay:"0.2s","duration":"2s"}}
            bouncing={{iterationCount:"0"}}
            whip={{iterationCount:"0"}}
        />
    </div>
    {/if}
    {#if shads[4]}
    <div id="shad4" class="shad">
        <Hippo 
            snap={{iterationCount:"1",delay:"0.2s","duration":"2s"}}
            bouncing={{iterationCount:"0"}}
            whip={{iterationCount:"0"}}
        />
    </div>
    {/if}
</div>

<style>
    #reelCtr{
        position: relative;
        height: 100%;
        width: 100%;
    }
    .flip{
        transform: rotateY(180deg);
    }
    #hippoCtr{
        position: absolute;
        z-index: 18;
        top: 40%;
        right: -5%;
        height: 80%;
        width: 80%;
    }
    #shad1{
        position: absolute;
        z-index: 17;
        top: 30%;
        right: -3%;
        height: 80%;
        width: 80%;
        opacity: 0;
        animation: visible 1s linear infinite;
        animation-delay: 0.8s;
        filter: invert(20%);
    }
    #shad2{
        position: absolute;
        z-index: 16;
        top: 20%;
        right: -1%;
        height: 80%;
        width: 80%;
        opacity: 0;
        animation: visible 1s linear infinite;
        animation-delay: 0.9s;
        filter: invert(40%);
    }
    #shad3{
        position: absolute;
        z-index: 15;
        top: 10%;
        right: 1%;
        height: 80%;
        width: 80%;
        opacity: 0;
        animation: visible 1s linear infinite;
        animation-delay: 1s;
        filter: invert(60%);
    }
    #shad4{
        position: absolute;
        z-index: 14;
        top: 0%;
        right: 3%;
        height: 80%;
        width: 80%;
        opacity: 0;
        animation: visible 1s linear infinite;
        animation-delay: 1.2s;
        filter: invert(80%);
    }

    @keyframes visible{
        0%{
            opacity: 1;
        }
        100%{
            opacity: 1;
        }
    }
</style>


