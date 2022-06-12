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
   
    /*
    export let reel = [{ component: "Empty", duration: -1  }]
    let reels = ""
    reel.forEach(frame => {
       reels += `<${frame.component} />`
    });*/
</script>

<div id="orchestrator">
    <Empty />
</div>


<style>
    #orchestrator{
        font-size: 5em;
    }
</style>

