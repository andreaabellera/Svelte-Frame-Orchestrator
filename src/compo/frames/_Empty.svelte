<script>
    // Also doubles as Casually CSS Svelte test environment for now

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

<link href="https://fonts.googleapis.com/css2?family=Work+Sans:wght@200;300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet">
<div id="reelCtr">
    <div id="casuallyReel">
            <a href="https://github.com/andreaabellera/Casually-CSS">
                <div id="casually">Casually CSS</div>
            </a>
            <a href="https://andreaabellera.github.io/Casually-CSS/">
                <div id="site">andreaabellera.github.io/Casually-CSS/</div>
            </a>
    </div>
    <div style="height: 30vh; width: max-content; margin-top: 50vh;"> <Octopus /> </div>
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

    a{
        text-decoration: none;
        color: black;
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
        animation-delay: 1.6s;
        animation: pulse 0.4s ease-in-out infinite;
        animation-iteration-count: 12;
    }

    #site{
        font-size: 2em;
        font-family: "Work Sans", sans-serif;
        font-weight: 700;
        color: black;
        /* text-shadow: -0.06em 0.06em 0 whitesmoke; */
        width: 100%;
    }

    /*#test{
        width: 20vw;
        height: 20vh;
        margin-left: 10vw;
        background-color: gainsboro;
    }*/
</style>

