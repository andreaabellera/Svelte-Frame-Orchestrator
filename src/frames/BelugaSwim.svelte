<script>
    import Beluga from "casually-css/@svelte/beluga.svelte"
</script>

<div id="reelCtr">
    <div class="flexyCtr" id="flexy1">
        <Beluga bodyColor="lightblue" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga bodyColor="orchid" bodyShade="purple" eyeColor="darkslateblue"/>
        <Beluga bodyColor="gainsboro" bodyShade="grey" eyeColor="darkslateblue"/>
        <Beluga bodyColor="aquamarine" bodyShade="darkslategrey" eyeColor="darkslateblue"/>
    </div>
    <div class="flexyCtr" id="flexy2">
        <Beluga bodyColor="lightsalmon" bodyShade="crimson" eyeColor="darkslateblue"/>
        <Beluga bodyColor="gold" bodyShade="darkgoldenrod" eyeColor="darkslateblue"/>
        <Beluga bodyColor="lightgreen" bodyShade="mediumseagreen" eyeColor="darkslateblue"/>
        <Beluga bodyColor="blanchedalmond" bodyShade="tan" eyeColor="darkslateblue"/>
    </div>
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        background-color: steelblue;
    }

    .flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 30vh;
    }

    #flexy1{
        transform: rotateY(180deg);
        animation: swimright 8s infinite;
    }

    #flexy2{
        animation: swimleft 8s infinite;
    }

    @keyframes swimleft{
        0%{
            transform: translateX(20vw);
        }
        100%{
            transform: translateX(-20vw);
        }
    }

    @keyframes swimright{
        0%{
            transform: rotateY(180deg) translateX(20vw);
        }
        100%{
            transform: rotateY(180deg) translateX(-20vw);
        }
    }
</style>

