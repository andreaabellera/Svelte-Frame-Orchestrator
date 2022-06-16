<script>
    import Beluga from "casually-css/@svelte/beluga.svelte"
</script>

<div id="reelCtr">
    <div class="flexyCtr" id="flexy1">
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
    </div>
    <div class="flexyCtr" id="flexy2">
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
        <Beluga swim={{iterationCount:"0"}} bodyColor="azure" bodyShade="cornflowerblue" eyeColor="darkslateblue"/>
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
    }

    .flexyCtr{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 30vh;
    }

    #flexy1{
        transform: rotateY(180deg);
        animation: swimright 16s infinite;
    }

    #flexy2{
        animation: swimleft 16s infinite;
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

