<script>
    import Beluga from "casually-css/beluga/beluga.svelte"
</script>

<div id="reelCtr">
    The Orchestrator is currently empty.
    <div id="test">
        <Beluga 
            eyeColor={"black"} 
            bodyColor={"lightgreen"} 
            bodyShade={"mediumseagreen"} 
            flipFin={{delay:"2s", duration:"1.5s"}} 
            belSwim={{iterationCount:0}}
            hStretch={{delay:"2s"}}
        />
    </div>
</div>

<style>
    #reelCtr{
        font-size: 36px;
    }

    #test{
        transform: scale(50%);
    }
</style>

