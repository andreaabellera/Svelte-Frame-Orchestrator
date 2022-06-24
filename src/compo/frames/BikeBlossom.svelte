<script>
    import Bike from "casually-css/@svelte/bike.svelte"
    import Blossom from "casually-css/@svelte/blossom.svelte"
</script>

<div id="reelCtr">
    <div id="ctr1" class="ctr">
        <Bike 
            spin={{duration:"3s"}}
        />
    </div>
    <div id="ctr2" class="ctr">
        <Blossom 
            midColor="gold"
            spin={{duration:"2s"}}
        />
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        background-color: burlywood;
    }
    .ctr{
        position: absolute;
    }
    #ctr1{
        top: 10%;
        left: 15%;
        height: 40%;
        width: 40%;
        animation: drive 2s ease-in-out infinite;
    }
    #ctr2{
        height: 7em;
        width: 7em;
        top: 60%;
        right: 25%;
    }

    @keyframes drive{
        0%{
            transform: translateX(0) rotateY(0deg);
        }
        /* 40%{
            transform: translateX(30vh) rotateY(0deg);
        } */
        50%{
            transform: translateX(30vh);
        }
        /* 90%{
            transform: translateX(0) rotateY(180deg);
        } */
        100%{
            transform: translateX(0);
        }
    }
</style>


