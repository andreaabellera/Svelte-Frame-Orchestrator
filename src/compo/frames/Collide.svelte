<script>
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
</script>

<div id="reelCtr">
    <div id="flexyCtr">
        <div id="bisonCtr" style="height:52px;width:70px;">
            <Bison 
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                dancing={{duration:"1.2s"}}
            />
        </div>
        <div id="hippoCtr" style="height:45px;width:75px;">
            <Hippo 
                bouncing={{duration:"0.6s"}}
                snap={{iterationCount:"0"}}
            />
        </div>
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: grid;
        align-items: center;
    }
    #flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: flex-end;
        height: max-content;
    }
    #bisonCtr{
        height: 52ex !important;
        width: 70ex !important;
        transform: translateY(-20px);
        animation: bumpL ease-in-out 3s;
    }
    #hippoCtr{
        height: 290px !important;
        width: 480px !important;
        transform: rotateY(180deg);
        animation: bumpR ease-in-out 3s;
    }

    @keyframes bumpL{
        20%{
            transform: translateX(-5em) rotateZ(45deg) translateY(-20px);
        }
        40%{
            transform: translateX(24em) rotateZ(-60deg) translateY(-20px);
        }
    }

    @keyframes bumpR{
        20%{
            transform: translateX(5em) rotateZ(-45deg) rotateY(180deg);
        }
        40%{
            transform: translateX(-24em) rotateZ(60deg) rotateY(180deg);
        }
    }
</style>



