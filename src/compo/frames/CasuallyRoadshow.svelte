<script>
    import Beluga from "casually-css/@svelte/beluga.svelte"
    import Swiss from "casually-css/@svelte/swiss.svelte"
    import Matcha from "casually-css/@svelte/matcha.svelte"
    import Orange from "casually-css/@svelte/orange.svelte"
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
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        </div>
        {/if}
        {#if visFlexies}
        <div class="flexyCtr" id="flexyFrmLeft" in:fly="{{ x: 2000, duration: 600 }}">
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
            <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        </div>
        {/if}
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
        top: 45%;
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
        animation-delay: 1.6s;
        animation: pulse 0.4s ease-in-out infinite;
        animation-iteration-count: 8;
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
        height: 100%;
        width: 100%;
        position: absolute;
        z-index: 1;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }

    .flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 30vh;
    }

    #flexyFrmLeft{
        transform: rotateY(180deg);
        animation: swimright 24s infinite;
    }

    #flexyFrmRight{
        animation: swimleft 24s infinite;
    }

    @keyframes swimleft{
        0%{
            transform: translateX(60vw);
        }
        100%{
            transform: translateX(0vw);
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

