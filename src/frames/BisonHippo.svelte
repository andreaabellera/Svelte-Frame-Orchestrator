<script>
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
    import { fly } from 'svelte/transition'

    let vis = false
    let id1 = setInterval(next, 20)
    function next() {
        vis = true
        clearInterval(id1)
    }
</script>

<div id="reelCtr">
    {#if vis}
    <div id="gridFillL" in:fly="{{ y: -2000, duration: 600 }}"></div>
    <div id="gridFillR" in:fly="{{ y: 2000, duration: 600 }}"></div>
    {/if}
    <div id="flexyCtr">
        {#if vis}
        <div id="bisonCtr" in:fly="{{ y: -2000, duration: 600 }}" style="height:52px;width:70px;">
            <Bison 
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                dancing={{duration:"1.2s"}}
            />
        </div>
        <div id="hippoCtr" in:fly="{{ y: 2000, duration: 600 }}" style="height:45px;width:75px;">
            <Hippo 
                bouncing={{duration:"0.6s"}}
                snap={{iterationCount:"0"}}
            />
        </div>
        {/if}
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: grid;
        grid-template-columns: 50% 50%;
        align-items: center;
    }
    #flexyCtr{
        position: absolute;
        z-index: 3;
        grid-column: 1/3;
        width: 100%;
        display: flex;
        justify-content: space-evenly;
        align-items: flex-end;
        height: max-content;
    }
    #gridFillL{
        height: 100%;
        width: 100%;
        background-color: darkseagreen;
    }
    #gridFillR{
        height: 100%;
        width: 100%;
        background-color: mediumpurple;
    }
    #bisonCtr{
        height: 52ex !important;
        width: 70ex !important;
        transform: translateY(-20px);
    }
    #hippoCtr{
        height: 290px !important;
        width: 480px !important;
        transform: rotateY(180deg);
    }
</style>


