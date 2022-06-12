<script>
    import Beluga from "casually-css/@svelte/beluga.svelte"
    
    /*import create from "casually-css"
    let neoDiv = appender()
    neoDiv.id="neoDiv"
    neoDiv.style.height="50vh"
    neoDiv.style.width="50vw"
    create(neoDiv, 'bison')
    function appender(){
        let newDiv = document.createElement("div")
        document.body.appendChild(newDiv)
        return newDiv
    }*/
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

