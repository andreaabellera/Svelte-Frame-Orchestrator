<div class="meta-container">
    <div class="artboard">
        <div class="boba">
            <div class="above">
            <span class="straw">
                <span class="straw-body"></span>
                <span class="straw-end"></span>
            </span>
            </div>
            <div class="lid"></div>
            <div class="body">
            <span class="cup">
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="bobapearl"></span>
                <span class="drink"></span>
                <span class="straw">
                <span class="straw-body"></span>
                <span class="straw-end"></span>
                </span>
            </span>
            </div>
            <div class="bottom">
            <span class="base">
                <span class="base-drink"></span>
            </span>
            </div>
        </div>
    </div>
</div>

<style>
    .meta-container {
        height: 20em;
        width: 8em;
    }

    :root{
    --straw: salmon;
    --lid: mediumpurple;
    --drink: rgba(207, 123, 13, 0.4);
    --cup: lightgrey;
    --bobapearl: #5E5550;
    }

    .artboard{
    position: relative;
    height: inherit;
    height: inherit;
    }

    .boba{
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-rows: 1fr 0.5em 65% 1em; 
    }

    .boba:hover{
        cursor: pointer;
    }

    .above, .lid, .body, .bottom{
    position: relative;
    display: grid;
    justify-items: center;
    }

    .straw{
    position: absolute;
    z-index: 4;
    height: 100%;
    width: 1em;
    transform: translateY(0.5em);
    display: grid;
    grid-template-rows: 1fr 0.4em;
    }

    .straw-body{
    background-color: var(--straw);
    }

    .straw-end{
    background-color: var(--straw);
    border-bottom-left-radius: 100%;
    border-bottom-right-radius: 100%;
    }

    .lid{
    background-color: var(--lid);
    transform: translateY(0.25em);
    border-radius: 80%;
    z-index: 3;
    }

    .cup{
    position: absolute;
    z-index: 0;
    background-color: var(--cup);
    height: 100%;
    width: 85%;
    clip-path: polygon(0% 0%, 100% 0%, 85% 100%, 15% 100%);
    display: grid;
    }

    .drink{
    position: absolute;
    z-index: 8;
    background-color: var(--drink);
    height: 100%;
    width: 100%;
    bottom: 0;
    }

    .drink:hover{
    animation: slurp 3s ease-in;
    animation-iteration-count: infinite;
    }

    .body .straw{
    z-index: 2;
    transform: scaleY(110%);
    justify-self: center;
    }

    .body .straw-body, .body .straw-end{
    opacity: 0.4;
    }

    .bobapearl{
    position: absolute;
    z-index: 7;
    height: 1em;
    width: 1em;
    border-radius: 3em;
    background-color: var(--bobapearl);
    }

    .bobapearl:nth-child(0){
    bottom: 0em;
    left: 4em;
    }

    .bobapearl:nth-child(1){
    bottom: 2em;
    left: 3em;
    }

    .bobapearl:nth-child(2){
    bottom: 0em;
    left: 3em;
    }

    .bobapearl:nth-child(3){
    bottom: 0.1em;
    left: 1em;
    }

    .bobapearl:nth-child(4){
    bottom: 0.3em;
    left: 3.4em;
    }

    .bobapearl:nth-child(5){
    bottom: 0.5em;
    left: 2em;
    }

    .bobapearl:nth-child(6){
    bottom: 1.0em;
    left: 4em;
    }

    .bobapearl:nth-child(7){
    bottom: 0em;
    left: 4.4em;
    }

    .bobapearl:nth-child(8){
    bottom: 0.4em;
    left: 4.8em;
    }

    .bobapearl:nth-child(9){
    bottom: 1.7em;
    left: 4.3em;
    }

    .bobapearl:nth-child(10){
    bottom: 1.5em;
    right: 4.3em;
    }

    .bobapearl:nth-child(11){
    bottom: 1em;
    left: 2.8em;
    }

    .base{
    background-color: var(--cup);
    height: 100%;
    width: 60%;
    border-bottom-left-radius: 80%;
    border-bottom-right-radius: 80%;
    }

    .base-drink{
    position: absolute;
    background-color: var(--drink);
    height: 100%;
    width: 60%;
    border-bottom-left-radius: 80%;
    border-bottom-right-radius: 80%;
    transform: translateY(-0.5em);
    }

    @keyframes slurp {
    0% {
        height: 100%;
    }
    100% {
        height: 1%;
    }
}
</style>