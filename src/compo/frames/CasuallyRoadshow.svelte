<script>
    import Beluga from "casually-css/@svelte/beluga.svelte"
    import Bike from "casually-css/@svelte/bike.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
    import Blossom from "casually-css/@svelte/blossom.svelte"
    import Boba from "casually-css/@svelte/boba.svelte"
    import Button from "casually-css/@svelte/button.svelte"
    import Calendar from "casually-css/@svelte/calendar.svelte"
    import Cookie from "casually-css/@svelte/cookie.svelte"
    import Dugong from "casually-css/@svelte/dugong.svelte"
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Lollipop from "casually-css/@svelte/lollipop.svelte"
    import Matcha from "casually-css/@svelte/matcha.svelte"
    import Octopus from "casually-css/@svelte/octopus.svelte"
    import Orange from "casually-css/@svelte/orange.svelte"
    import Swiss from "casually-css/@svelte/swiss.svelte"
    import { fly } from "svelte/transition";
    import { bounceIn } from 'svelte/easing';

    // Pop in
    function zoom({ duration }) {
		return {
			duration,
			css: t => {
				const eased = bounceIn(t);

				return `
					transform: scale(${eased}) rotate(${eased * 360}deg);`
			}
		};
	}

    let vis = false
    let id1 = setInterval(next1, 40)
    function next1() {
        vis = true
        clearInterval(id1)
    }
    let visFlexies = false
    let id2 = setInterval(next2, 600)
    function next2() {
        visFlexies = true
        clearInterval(id2)
    }

    // Thank you https://krazydad.com/tutorials/makecolors.php

    $: bodyCols = [0,127,254]
    $: bodyTint = [0,127,254]
    let i = 0
    setInterval(() => {
        bodyCols[0] = (Math.sin(0.1*i + 0) * 55 + 200)
        bodyCols[1] = (Math.sin(0.1*i + 2) * 55 + 200)
        bodyCols[2] = (Math.sin(0.1*i + 4) * 55 + 200)

        bodyTint[0] = (Math.sin(0.1*i + 0) * 25 + 230)
        bodyTint[1] = (Math.sin(0.1*i + 2) * 25 + 230)
        bodyTint[2] = (Math.sin(0.1*i + 4) * 25 + 230)
        i++
    }, 60)
</script>

<link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@200;300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet">
<div id="reelCtr">
    <div id="casuallyReel">
        {#if vis}
        <div id="casually" in:zoom="{{duration: 1800}}">
            Casually CSS
        </div>
        <div id="site">andreaabellera.github.io/Casually-CSS/</div>
        {/if}
    </div>
    <div id="flexyReel">
        {#if visFlexies}
        <div class="flexyCtr" id="flexyFrmRight" in:fly="{{ x: 2000, duration: 600 }}">
            <div class="ctr">
            <Beluga swim={{iterationCount:"0"}} flipFin={{duration:"4s"}} flipTail={{duration:"4s"}} hStretch={{duration:"4s"}} hStretch2={{duration:"4s"}} vStretch={{duration:"4s"}} bodyColor={"rgb("+bodyTint[0]+","+bodyTint[1]+","+bodyTint[2]+")"} bodyShade={"rgb("+bodyCols[0]+","+bodyCols[1]+","+bodyCols[2]+")"} />
            </div>
            <div class="ctr">
            <Blossom spin={{duration:"4s"}} bodyColor={"rgb("+bodyCols[0]+","+bodyCols[1]+","+bodyCols[2]+")"} />
            </div>
            <div class="ctr">
            <Hippo bouncing={{duration:"2s"}} snap={{iterationCount:"0"}} bodyColor={"rgb("+(bodyCols[0]-50)+","+(bodyCols[1]-50)+","+(bodyCols[2]-50)+")"} />
            </div>
            <div class="ctr">
            <Dugong bodyColor={"rgb("+(bodyCols[0]-50)+","+(bodyCols[1]-50)+","+(bodyCols[2]-50)+")"} bodyTint={"rgb("+(bodyTint[0]-50)+","+(bodyTint[1]-50)+","+(bodyTint[2]-50)+")"} />
            </div>
            <div class="ctr">
            <Calendar flap={{duration:"4s"}} bodyColor={"rgb("+bodyCols[0]+","+bodyCols[1]+","+bodyCols[2]+")"} />
            </div>
            <div class="ctr">
            <Matcha bodyColor={"rgb("+(bodyCols[0]-100)+","+(bodyCols[1]-100)+","+(bodyCols[2]-100)+")"} drinkColor={"rgb("+bodyTint[0]+","+bodyTint[1]+","+bodyTint[2]+")"} />
            </div>
        </div>
        {/if}
        <!-- {#if visFlexies}
        <div class="flexyCtr" id="flexyFrmLeft" in:fly="{{ x: 2000, duration: 600 }}">
            <Beluga swim={{iterationCount:"0"}} bodyColor={"rgb("+bodyTint[1]+","+bodyTint[2]+","+bodyTint[0]+")"} bodyShade={"rgb("+bodyCols[1]+","+bodyCols[2]+","+bodyCols[0]+")"}/>
            <Lollipop />
            <Orange />
            <Boba />
            <Bison />
            <Cookie />
            <Bike />
            <Swiss />
        </div>
        {/if} -->
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
    }

    #casuallyReel{
        position: absolute;
        top: 30%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 18;
        width: 70vw;
        text-align: center;
    }

    #casually{
        font-size: 7em;
        padding-bottom: 0.5em; 
        font-family: "Fredoka One", cursive;
        color: whitesmoke;
        text-shadow: -0.06em 0.06em 0 rgba(75, 207, 255, 0.6);
        width: 100%;
        animation-delay: 2s;
        animation: pulse 0.4s ease-in-out infinite;
        animation-iteration-count: 16;
    }

    #site{
        font-size: 2em;
        font-family: "Work Sans", sans-serif;
        font-weight: 700;
        color: black;
        /* text-shadow: -0.06em 0.06em 0 whitesmoke; */
        width: 100%;
    }

    #flexyReel{
        height: 80%;
        width: 100%;
        position: absolute;
        z-index: 1;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
    }

    .flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 30vh;
    }

    .ctr{
        height: 100%;
        width: max-content;
        transform: scale(0.8);
    }

    /* #flexyFrmLeft{
        transform: rotateY(180deg);
        animation: swimright 16s infinite;
    } */

    #flexyFrmRight{
        animation: swimleft 10s infinite;
    }

    @keyframes swimleft{
        0%{
            transform: translateX(60vw);
        }
        100%{
            transform: translateX(-10vw);
        }
    }

    @keyframes swimright{
        0%{
            transform: rotateY(180deg) translateX(60vw);
        }
        100%{
            transform: rotateY(180deg) translateX(0vw);
        }
    }

    @keyframes pulse{
        0%{
            transform: scale(1);
        }
        35%{
            transform: scale(1.01);
        }
        70%{
            transform: scale(1);
        }
    }
</style>

