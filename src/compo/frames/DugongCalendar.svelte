<script>
    import Dugong from "casually-css/@svelte/dugong.svelte"
    import Calendar from "casually-css/@svelte/calendar.svelte"


    // Thank you https://krazydad.com/tutorials/makecolors.php

    $: bodyCols = [0,127,254]
    $: bodyTint = [0,127,254]
    let i = 0
    setInterval(() => {
        bodyCols[0] = (Math.sin(0.1*i + 0) * 55 + 200) -50
        bodyCols[1] = (Math.sin(0.1*i + 2) * 55 + 200) -50
        bodyCols[2] = (Math.sin(0.1*i + 4) * 55 + 200) -50

        bodyTint[0] = (Math.sin(0.1*i + 0) * 25 + 230) -50
        bodyTint[1] = (Math.sin(0.1*i + 2) * 25 + 230) -50
        bodyTint[2] = (Math.sin(0.1*i + 4) * 25 + 230) -50
        i++
    }, 60)

    $: month = "May"
    $: dayStart = 0
    $: days = 31
    $: calBodyColor = "lightblue"
    $: calCelColor = "rgb(231, 240, 243)"
    $: calTextColor = "whitesmoke"
    let id1 = setInterval(next, 1200)
    function next() {
        month = "June"
        dayStart = 3
        days = 30
        calBodyColor = "gainsboro"
        calCelColor = "white"
        calTextColor = "navy"
        clearInterval(id1)
    }
</script>

<div id="reelCtr">
    <div id="flexyCtr">
        <div id="dugongCtr" style="height:70px;width:70px;">
            <Dugong 
                bodyColor={"rgb("+bodyCols[0]+","+bodyCols[1]+","+bodyCols[2]+")"}
                bodyTint={"rgb("+bodyTint[0]+","+bodyTint[1]+","+bodyTint[2]+")"}
                talk={{iterationCount:"0"}}
                swim={{duration:"2s"}}
                flipTail={{duration:"2s"}}
                flipFinL={{duration:"2s"}}
                flipFinR={{duration:"2s"}}
            />
        </div>
        <div id="calendarCtr" style="height:45px;width:75px;">
            <Calendar 
                month={month}
                year={"2022"}
                dayStart={dayStart}
                days={days}
                bodyColor = {calBodyColor}
                celColor = {calCelColor}
                monthColor = {calTextColor}
                flap={{duration:"4s"}}
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
    #dugongCtr{
        height: 70ex !important;
        width: 70ex !important;
        transform: translateX(9em);
    }
    #calendarCtr{
        height: 290px !important;
        width: 480px !important;
        transform: translate(-9em,-9em);
    }
</style>

