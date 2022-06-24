<script>
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
</script>

<div id="reelCtr">
    <div id="gridCtr">
        <div id="ctr1">
            <Hippo
                bodyColor="pink"
                eyeColor="mediumpurple"
                earColor="orchid"
                nailColor="blanchedalmond"
                outlineColor="#5e4e52"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div id="ctr2">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
            />
        </div>
        <div id="ctr3">
            <Hippo
                bouncing={{ duration: "0.4s" }}
                snap={{ iterationCount: "0" }}
            />
        </div>
        <div id="ctr4">
            <Hippo
                bodyColor="#3e3e3e"
                eyeColor="lightskyblue"
                outlineColor="darkslateblue"
            />
        </div>
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        display: grid;
        justify-items: center;
        align-items: center;
        background-color: antiquewhite;
    }
    #gridCtr{
        height: 90%;
        width: 70%;
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 50% 50%;
        grid-template-rows: 50% 50%;
    }
    #ctr1,#ctr4{
        transform: rotateY(180deg);
    }
    #ctr2{
        transform: scale(0.8);
    }
</style>


