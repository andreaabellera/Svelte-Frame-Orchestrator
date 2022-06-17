<script>
    import Lollipop from "casually-css/@svelte/lollipop.svelte"
    import Cookie from "casually-css/@svelte/cookie.svelte"
</script>

<div id="reelCtr">
    <div id="cookieCtr">
        <Cookie outlineColor="rgb(218, 125, 179)" eat={{delay:"2s"}} />
    </div>

    <div id="sweetCirc">
        <div class="stabilize">
            <div class="halfgrid">
                <div id="lolCtr1" class="lolCtr">
                    <Lollipop eat={{delay:"1.2s"}} />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr2" class="lolCtr">
                    <Lollipop eat={{delay:"1.3s"}} bodyColor="lightsalmon" />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr3" class="lolCtr">
                    <Lollipop eat={{delay:"1.4s"}} />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr4" class="lolCtr">
                    <Lollipop eat={{delay:"1.5s"}} bodyColor="lightgreen" />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr5" class="lolCtr">
                    <Lollipop eat={{delay:"1.6s"}} />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr6" class="lolCtr">
                    <Lollipop eat={{delay:"1.7s"}} bodyColor="skyblue" />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr7" class="lolCtr">
                    <Lollipop eat={{delay:"1.8s"}} />
                </div>
            </div>
            <div class="halfgrid">
                <div id="lolCtr8" class="lolCtr">
                    <Lollipop eat={{delay:"1.9s"}} bodyColor="blanchedalmond" />
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: grid;
        justify-items: center;
        align-items: center;
    }
    #cookieCtr{
        height:max-content;
        width:max-content;
        position: absolute;
        left:50%;
        top:50%;
        transform: translate(-50%,-50%);
        z-index: 18;
    }
    #sweetCirc{
        position: absolute;
        height: 80%;
        width: 60%;
        left:75%;
        top:50%;
        transform: translate(-50%,-50%);
    }
    .stabilize{
        height: 100%;
        width: 100%;
        position: relative;
    }
    .halfgrid{
        position: absolute;
        height: 100%;
        width: max-content;
        display: grid;
        grid-template-rows: 50% 50%;
    }
    .lolCtr{
        height:100%;
        width:max-content;
        animation: spin 8s ease-in;
    }
    .halfgrid:nth-of-type(2){
        transform: rotate(45deg);
    }

    .halfgrid:nth-of-type(3){
        transform: rotate(90deg);
    }

    .halfgrid:nth-of-type(4){
        transform: rotate(135deg);
    }

    .halfgrid:nth-of-type(5){
        transform: rotate(180deg);
    }

    .halfgrid:nth-of-type(6){
        transform: rotate(225deg);
    }

    .halfgrid:nth-of-type(7){
        transform: rotate(270deg);
    }

    .halfgrid:nth-of-type(8){
        transform: rotate(315deg);
    }

    @keyframes spin{
        0%{
            transform: rotate(180deg);
        }
        10%{
            transform: rotate(0deg);
        }
    }
</style>

