<script>
    import Swiss from "casually-css/@svelte/swiss.svelte"
    import Matcha from "casually-css/@svelte/matcha.svelte"
    import Orange from "casually-css/@svelte/orange.svelte"
</script>

<div id="reelCtr">
    <div id="splash1" class="splash">
        <Swiss />
    </div>
    <div id="splash2" class="splash">
        <Matcha />
    </div>
    <div id="splash3" class="splash">
        <Orange />
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
    }
    .splash{
        height:max-content;
        width:max-content;
        position: absolute;
        left:50%;
        bottom:0;
        transform: translateX(-50%);
    }
    #splash1{
        animation: splash1 2s linear;
    }
    #splash2{
        animation: splash2 2s linear;
    }
    #splash3{
        animation: splash3 2s linear;
    }

    @keyframes splash1{
        0%{
            left: 50%;
            bottom: 0;
            transform: translateX(-50%) rotate(0deg);
        }
        60%{
            left: 0%;
            bottom: 40%;
            transform: translateX(-50%) rotate(-580deg);
        }
        100%{
            left: 0%;
            bottom: 40%;
            transform: translateX(-50%) rotate(-580deg);
        }
    }
    @keyframes splash2{
        0%{
            bottom: 0%;
            transform: translateX(-50%) rotate(0deg);
        }
        60%{
            bottom: 80%;
            transform: translateX(-40%) rotate(-360deg);
        }
        100%{
            bottom: 80%;
            transform: translateX(-40%) rotate(-360deg);
        }
    }
    @keyframes splash3{
        0%{
            left: 50%;
            bottom: 0;
            transform: translateX(-50%) rotate(0deg);
        }
        60%{
            left: 100%;
            bottom: 60%;
            transform: translateX(-50%) rotate(720deg);
        }
        100%{
            left: 100%;
            bottom: 60%;
            transform: translateX(-50%) rotate(720deg);
        }
    }

</style>

