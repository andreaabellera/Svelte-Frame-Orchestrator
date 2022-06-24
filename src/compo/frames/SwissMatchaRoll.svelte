<script>
    import Swiss from "casually-css/@svelte/swiss.svelte"
    import Matcha from "casually-css/@svelte/matcha.svelte"
    import Orange from "casually-css/@svelte/orange.svelte"
    import { fly } from 'svelte/transition'

    let vis = [false,false, false,false,false, false,false,false,false]
    let id1 = setInterval(next1, 20)
    function next1() {
        vis[0] = true
        clearInterval(id1)
    }
    let id2 = setInterval(next2, 300)
    let tick = 1
    function next2() {
        vis[tick] = true
        tick++
        if(tick == vis.length)
            clearInterval(id2)
    }
</script>

<div id="reelCtr">
    {#if vis[0]}
    <div class="flexyCtr" id="flexy1" in:fly="{{ y: 800, duration: 600 }}">
        <div class="flexy1content"><Swiss /></div>
        {#if vis[1]}
        <div class="flexy1content" in:fly="{{ y: 800, duration: 600 }}">
            <Swiss bodyColor="mediumturquoise" logoColor="orange" />
        </div>
        {/if}
    </div>
    {/if}
    {#if vis[2]}
    <div class="flexyCtr" id="flexy2" in:fly="{{ y: 800, duration: 600 }}">
        <div class="flexy2content"><Matcha /></div>
        {#if vis[3]}
        <div class="flexy2content" in:fly="{{ y: 800, duration: 600 }}">
            <Matcha />
        </div>
        {/if}
        {#if vis[4]}
        <div class="flexy2content" in:fly="{{ y: 800, duration: 600 }}">
            <Matcha />
        </div>
        {/if}
    </div>
    {/if}
    {#if vis[5]}
    <div class="flexyCtr" id="flexy3" in:fly="{{ y: 800, duration: 600 }}">
        <div class="flexy3content"><Orange /></div>
        {#if vis[6]}
        <div class="flexy3content" in:fly="{{ y: 800, duration: 600 }}">
            <Orange bodyColor="yellowgreen" />
        </div>
        {/if}
        {#if vis[7]}
        <div class="flexy3content" in:fly="{{ y: 800, duration: 600 }}">
            <Orange bodyColor="lightsalmon" />
        </div>
        {/if}
        {#if vis[8]}
        <div class="flexy3content" in:fly="{{ y: 800, duration: 600 }}">
            <Orange bodyColor="yellow" />
        </div>
        {/if}
    </div>
    {/if}
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        background-color: lightsteelblue;
    }

    .flexyCtr{
        display: grid;
        justify-items: center;
        align-items: center;
        height: 20vh;
    }

    #flexy1{
        width: 45%;
        grid-template-columns: 50% 50%;
    }

    #flexy2{
        width: 60%;
        grid-template-columns: 33% 1fr 33%;
    }

    #flexy3{
        width: 75%;
        grid-template-columns: 25% 25% 25% 25%;
    }

    .flexy1content, .flexy2content, .flexy3content{
        height: inherit;
        width: inherit;
    }
</style>


