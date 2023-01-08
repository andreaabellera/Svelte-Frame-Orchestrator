<script>
    import Octopus from "casually-css/@svelte/octopus.svelte"
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
        width: 100%;
    }
</style>

