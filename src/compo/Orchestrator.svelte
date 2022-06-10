<script>;
    // Import all the frames
    import Empty from './frames/_Empty.svelte';
    
    export let reel = [{ component: "Empty", duration: -1  }]

    // Blueprint
    /*
    2:00 SummonBison
    2:00 SummonHippo
    2:00 BisonHippo
    1:00 FourGrid
    1:00 TwelveGrid
    
    4:00 Descent
    1:00 Collide
    1:00 Splash
    2:00 SweetCirc
    
    1:00 HippoSnap
    3:00 BelugaSwim
    1:00 HippoSnap
    3:00 SwissMatchaRoll

    3:00 BikeOrange
    3:00 DugongCalendar
    
    8:00 CasuallyRoadshow

    TOTAL 38:00
    */
   let reels = ""
   reel.forEach(frame => {
       reels += `<${frame.component} />`
   });
</script>

<div id="orchestrator">
    {reels}
    <Empty />
</div>


<style>
    #orchestrator{
        font-size: 5em;
    }
</style>

