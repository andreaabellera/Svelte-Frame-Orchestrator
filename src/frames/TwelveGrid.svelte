<script>
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
</script>

<div id="reelCtr">
    <div id="gridCtr">
        <div class="ctr" id="ctr1">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div class="ctr" id="ctr2">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
            />
        </div>
        <div class="ctr" id="ctr3">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div class="ctr" id="ctr4">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
            />
        </div>

        <div class="ctr" id="ctr5">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
            />
        </div>
        <div class="ctr" id="ctr6">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div class="ctr" id="ctr7">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
            />
        </div>
        <div class="ctr" id="ctr8">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>

        <div class="ctr" id="ctr9">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div class="ctr" id="ctr10">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
            />
        </div>
        <div class="ctr" id="ctr11">
            <Hippo
                bodyColor="lightsteelblue"
                eyeColor="#4e4e5e"
                earColor="orchid"
                nailColor="mediumpurple"
                outlineColor="#4e4e5e"
                snap={{ delay: "0.5s" }}
            />
        </div>
        <div class="ctr" id="ctr12">
            <Bison
                dancing={{ iterationCount: "0" }}
                footworkFL={{delay:"0.5s",duration:"4s"}}
                footworkFR={{delay:"2s",duration:"4s"}}
                footworkBL={{delay:"1s",duration:"4s"}}
                footworkBR={{delay:"1.5s",duration:"4s"}}
                bodyColor="lightsteelblue"
                hairColor="steelblue"
                noseColor="lightgrey"
                outlineColor="#4e4e5e"
                hornColor="silver"
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
        background-color: darkgrey;
    }
    #gridCtr{
        height: 95%;
        width: 70%;
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 25% 25% 25% 25%;
        grid-template-rows: 33vh 33vh 33vh;
        transform: translateX(-10vh);
    }
    .ctr{
        transform: scale(0.5);
    }
    #ctr1,#ctr4,#ctr6,#ctr11,#ctr12{
        transform: scale(0.5) rotateY(180deg);
    }
</style>

