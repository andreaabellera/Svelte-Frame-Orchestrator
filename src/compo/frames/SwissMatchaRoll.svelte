<script>
    import Swiss from "casually-css/@svelte/swiss.svelte"
    import Matcha from "casually-css/@svelte/matcha.svelte"
    import Orange from "casually-css/@svelte/orange.svelte"
</script>

<div id="reelCtr">
    <div class="flexyCtr" id="flexy1">
        <div id="flexy1content"><Swiss /></div>
        <div id="flexy1content"><Swiss bodyColor="mediumturquoise" logoColor="orange" /></div>
    </div>
    <div class="flexyCtr" id="flexy2">
        <div id="flexy2content"><Matcha /></div>
        <div id="flexy2content"><Matcha /></div>
        <div id="flexy2content"><Matcha /></div>
    </div>
    <div class="flexyCtr" id="flexy3">
        <div id="flexy3content"><Orange /></div>
        <div id="flexy3content"><Orange bodyColor="yellowgreen" /></div>
        <div id="flexy3content"><Orange bodyColor="lightsalmon" /></div>
        <div id="flexy3content"><Orange bodyColor="yellow" /></div>
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }

    .flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 20vh;
        transform: scale3d(0.7);
    }

    #flexy1content{
        height: 100%;
        width: max-content;
    }

    #flexy2content{
        height: 100%;
        width: max-content;
    }

    #flexy3content{
        height: 100%;
        width: max-content;
    }
</style>


