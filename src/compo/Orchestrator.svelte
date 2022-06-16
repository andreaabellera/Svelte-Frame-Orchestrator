<script>;
    // Import all the frames
    import Empty from './frames/_Empty.svelte'
    
    import SummonBison from './frames/SummonBison.svelte'
    import SummonHippo from './frames/SummonHippo.svelte'
    import BisonHippo from './frames/BisonHippo.svelte'
    import FourGrid from './frames/FourGrid.svelte'
    import TwelveGrid from './frames/TwelveGrid.svelte'

    import Descent from './frames/Descent.svelte'
    import Collide from './frames/Collide.svelte'
    import Splash from './frames/Splash.svelte'
    import SweetCirc from './frames/SweetCirc.svelte'

    import HippoSnap from './frames/HippoSnap.svelte'
    import BelugaSwim from './frames/BelugaSwim.svelte'
    import SwissMatchaRoll from './frames/SwissMatchaRoll.svelte'

    import BikeOrange from './frames/BikeOrange.svelte'
    import DugongCalendar from './frames/DugongCalendar.svelte'
    import CasuallyRoadshow from './frames/CasuallyRoadshow.svelte'

    // Blueprint
    /*
    4:00 SummonBison /
    4:00 SummonHippo /
    2:00 BisonHippo /
    1:00 FourGrid /
    1:00 TwelveGrid /
    
    4:00 Descent
    1:00 Collide
    1:00 Splash
    2:00 SweetCirc
    
    1:00 HippoSnap
    3:00 BelugaSwim /
    1:00 HippoSnap
    3:00 SwissMatchaRoll

    3:00 BikeOrange
    3:00 DugongCalendar
    
    8:00 CasuallyRoadshow

    TOTAL 42:00
    */

    export let intervals = []
    let totalTime = 0
    let currFrame = 0
    for (let time of intervals) {
        totalTime += time
        let id = setInterval(loadFrame, totalTime)
        function loadFrame() {
            currFrame++
            clearInterval(id)
        }
    }
</script>

<div id="orchestrator">
    {#if intervals.length == 0}    
        <BisonHippo />
    {:else}
        {#if currFrame == 0}
            <SummonBison />
        {:else if currFrame == 1}
            <SummonHippo />
        {:else if currFrame == 2}
            <BisonHippo />
        {:else if currFrame == 3}
            <FourGrid />
        {:else if currFrame == 4}
            <TwelveGrid />
        {:else if currFrame == 5}
            <Descent />
        {:else if currFrame == 6}
            <Collide />
        {:else if currFrame == 7}
            <Splash />
        {:else if currFrame == 8}
            <SweetCirc />
        {:else if currFrame == 9}
            <HippoSnap />
        {:else if currFrame == 10}
            <BelugaSwim />
        {:else if currFrame == 11}
            <HippoSnap />
        {:else if currFrame == 12}
            <SwissMatchaRoll />
        {:else if currFrame == 13}
            <BikeOrange />
        {:else if currFrame == 14}
            <DugongCalendar />
        {:else if currFrame == 15}
            <CasuallyRoadshow />
        {/if}
    {/if}
</div>
