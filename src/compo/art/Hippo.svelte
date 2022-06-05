<script>
  export let height = "18em";
  export let width = "30em";
</script>

<div class="meta-container" style="height:{height}; width:{width};">
    <div class="artboard">
        <div class="hippo">
            <span class="hippo-bod">
              <span class="hippo-tail">
                <div></div>
                <div class="tail1 se-sharp"></div>
                <div></div>
                <div class="tail2">   <div class="tail-line"></div>   </div>
                <div class="tail3"></div>
              </span>
            </span>
            <span class="hippo-leg front-near">
              <div class="nails">   <div class="nail se"></div>   </div>
              <div class="nails">   <div class="nail sw"></div>   </div>
              <div class="nails">   <div class="nail se"></div>   </div>
              <div class="nails">   <div class="nail sw"></div>   </div>
              <div class="nails">   <div class="nail se"></div>   </div>
            </span>
            <span class="hippo-leg front-far"></span>
            <span class="hippo-leg back-near">
              <div class="nails">   <div class="nail se"></div>   </div>
              <div class="nails">   <div class="nail sw"></div>   </div>
              <div class="nails">   <div class="nail se"></div>   </div>
              <div class="nails">   <div class="nail sw"></div>   </div>
              <div class="nails">   <div class="nail se"></div>   </div>
            </span>
            <span class="hippo-leg back-far"></span>
            <span class="hippo-head">
              <div class="head-junction1 se-sharp skin">
                <span class="ear">
                  <div class="ear-in"></div>
                </span>
              </div>
              <div class="skin sw-sharp"></div>
              <div class="head-junction2 skin"></div>
              <div class="skin"></div>
              <div class="head-junction3 skin">
                <span class="eye1"></span>
                <span class="eye2"></span>
              </div>
              <div class="skin sw-sharp"></div>
              <div></div>
              <div class="head-junction4 ne skin"></div>
              <div class="skin nw-sharp"></div>
              <div></div>
              <div></div>
              <div></div>
              <div class="south-cap">
                <div class="skin ne-sharp"></div>
                <div class="skin nw-sharp"></div>
              </div>
            </span>
            <span class="hippo-jaw">
              <div class="ne skin mouth-area">
                <div class="ne mouth"></div>
              </div>
              <div class="nw skin end mouth-area">
                <div class="nw mouth">
                  <span class="tooth"></span>
                  <span class="tooth"></span>
                </div>
              </div>
            </span>
        </div>
    </div>
</div>

<style>
    .meta-container{
        /* height: 18em;
        width: 30em; */
    }

    :root{
    --outline: #222222;
    --body: #BDB8AA;
    --eye: #222222;
    --ear: #F0B3BF;
    --teeth: whitesmoke;
    --mouth: #E0A3AF; 
    --nail: gainsboro;
    }

    .artboard{
    height: inherit;
    width: inherit;
    }

    .hippo{
    position: relative;
    }

    .hippo:hover{
      cursor: url(https://ipfs.fleek.co/ipfs/bafybeiafet7hldlwiwpj5bbftxizcspsvi3ernckqpklgbuup2lq6rtq6m), pointer;
    }

    .hippo-bod{
    position: absolute;
    z-index: 2;
    background-color: var(--body);
    height: 14.5em;
    width: 22em;
    border-top-left-radius: 15em;
    border-top-right-radius: 100%;
    border-bottom-left-radius: 80%;
    border-bottom-right-radius: 80%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-style: solid;
    left: 1em;
    animation: bouncing 1s ease-out;
    animation-iteration-count: infinite;
    }

    .hippo-tail{
    position: relative;
    z-index: 3;
    height: auto;
    width: 3em;
    display: grid;
    grid-template-rows: 3.5em 3.5em 2em;
    grid-template-columns: 50% 50%;
    left: -1.5em;
    top: 3.8em;
    animation: whip 10s ease-out;
    animation-iteration-count: infinite;
    }

    .hippo-tail .se-sharp{
    border-top-width: 0em;
    }

    .tail1{
    background-color: var(--body);
    border-color: var(--outline);
    border-left-style: solid;
    }

    .tail2{
    background-color: var(--body);
    border-width: 0.4em;
    border-color: var(--outline);
    border-left-style: solid;
    clip-path: polygon(0% 0%, 69% 0%, 29% 100%, 0% 100%);
    }

    .tail-line{
    width: 0.4em;
    height: 100%;
    background-color: var(--outline);
    transform: rotate(5deg);
    clip-path: polygon(70% 0%, 100% 0%, 100% 100%, 0% 100%);
    }

    .tail3{
    background-color: var(--body);
    grid-column: 1/3;
    border-top-right-radius: 50%;
    border-top-left-radius: 1em;
    border-bottom-left-radius: 50%;
    transform: rotate(90deg);
    border-width: 0.4em;
    border-color: var(--outline);
    border-style: solid;
    }

    .hippo-leg{
    position: absolute;
    height: 3.5em;
    width: 5em;
    background-color: var(--body);
    border-width: 0.4em;
    border-color: var(--outline);
    border-left-style: solid;
    border-right-style: solid;
    border-bottom-style: solid;
    border-top-left-radius: 10%;
    border-top-right-radius: 40%;
    border-bottom-left-radius: 1em;
    border-bottom-right-radius: 1em;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    }

    .front-near{
    z-index: 3;
    top: 13em;
    left: 13em;
    overflow: hidden;
    }

    .front-far{
    z-index: 1;
    top: 12em;
    left: 15em;
    filter: brightness(40%);
    }

    .back-near{
    z-index: 3;
    top: 13em;
    left: 5em;
    overflow: hidden;
    }

    .back-far{
    z-index: 1;
    top: 12em;
    left: 7em;
    filter: brightness(40%);
    }

    .nails{
    height: 0.8em;
    width: 0.4em;
    }

    .nails .se{
    border-top-style: none;
    border-left-style: none;
    }
    .nails .sw{
    border-top-style: none;
    border-right-style: none;
    }

    .nail{
    background-color: var(--nail);
    }

    .hippo-head{
    position: absolute;
    z-index: 5;
    right: 0;
    display: grid;
    height: 11em;
    width: 14em;
    grid-template-columns: 12% 8% 20% 40% 20%;
    grid-template-rows: 30% 25% 35% 10%;
    }

    .hippo-head:hover{
    animation: snap 1s ease-in-out;
    animation-iteration-count: infinite;
    }

    .skin{
    background-color: var(--body);
    }

    .head-junction1{
    grid-column: 1/4;
    position: relative;
    }

    .hippo-head .se-sharp{
    border-left-width: 0em;
    }

    .hippo-head .ne{
    border-left-width: 0em;
    border-bottom-width: 0em;
    }

    .head-junction2{
    grid-column: 1/3;
    }

    .ear{
    position: absolute;
    left: 0.4em;
    height: 1.8em;
    width: 2.2em;
    background-color: var(--body);
    border-top-left-radius: 100%;
    border-top-right-radius: 100%;
    border-bottom-left-radius: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-left-style: solid;
    border-top-style: solid;
    display: grid;
    justify-items: flex-end;
    align-items: flex-end;
    transform: rotate(50deg);
    animation: wiggle 5s ease-in;
    animation-iteration-count: infinite;
    }

    .ear-in{
    height: 60%;
    width: 70%;
    border-radius: 100%;
    background-color: var(--ear);
    }

    .head-junction3{
    grid-column: 4/5;
    grid-row: 2/4; 
    position: relative;
    }

    .head-junction4{
    grid-column: 2/4;
    grid-row: 3/4;
    /*clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 70% 90%, 50% 80%);*/
    }

    .eye1{
    position: absolute;
    height: 1em;
    width: 0.6em;
    background-color: var(--eye);
    border-radius: 50%;
    left: 1.7em;
    top: 1em;
    }

    .eye2{
    position: absolute;
    height: 1em;
    width: 0.6em;
    background-color: var(--eye);
    border-radius: 50%;
    right: 0em;
    }

    .hippo-jaw{
    position: absolute;
    z-index: 4;
    right: 0.8em;
    top: 6.4em;
    display: grid;
    height: 5em;
    width: 13em;
    grid-template-columns: 40% 60%;
    transform: rotate(5deg) skewY(6deg);
    }

    .hippo-jaw .ne{
    border-left-width: 0em;
    border-bottom-left-radius: 90%;
    }

    .end{
    border-top-right-radius: 4em;
    }

    .mouth{
    background-color: var(--mouth);
    height: 50%;
    position: relative;
    overflow: hidden;
    }

    .mouth-area{
    height: 100%;
    width: 100%;
    display: grid;
    }

    .mouth-area .ne{
    height: 70%;
    width: 60%;
    border-width: 0em;
    justify-self: flex-end;
    }

    .mouth-area .nw{
    height: 70%;
    width: 95%;
    border-width: 0em;
    }

    .tooth{
    position: absolute;
    background-color: var(--teeth);
    height: 0.8em;
    width: 0.6em;
    }

    .tooth:nth-child(1){
    bottom: 0em;
    left: 4.1em;
    transform: rotate(-5deg);
    }

    .tooth:nth-child(2){
    bottom: 2.5em;
    left: 6.6em;
    transform: rotate(-65deg);
    }

    /*===================
    // CURVE SHAPES 
    ===================*/

    .se{
    border-top-left-radius: 20em;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-top-style: solid;
    border-left-style: solid;
    border-top-left-radius: 100%;
    }

    .se-sharp{
    border-top-left-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-top-style: solid;
    border-left-style: solid;
    border-top-left-radius: 100%;
    }

    .ne{
    border-bottom-left-radius: 20em;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-bottom-style: solid;
    border-left-style: solid;
    border-bottom-left-radius: 16em;
    }

    .ne-sharp{
    border-bottom-left-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-bottom-style: solid;
    border-left-style: solid;
    border-bottom-left-radius: 100%;
    }

    .nw{
    border-bottom-right-radius: 20em;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-bottom-style: solid;
    border-right-style: solid;
    border-bottom-right-radius: 16em;
    }

    .nw-sharp{
    border-bottom-right-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-bottom-style: solid;
    border-right-style: solid;
    border-bottom-right-radius: 100%;
    }

    .sw{
    border-top-right-radius: 20em;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-top-style: solid;
    border-right-style: solid;
    border-top-right-radius: 100%;
    }

    .sw-sharp{
    border-top-right-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.4em;
    border-color: var(--outline);
    border-top-style: solid;
    border-right-style: solid;
    border-top-right-radius: 100%;
    }

    .south-cap{
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-columns: 60% 40%;
    }

    @keyframes bouncing{
        0%{
            top: 0em;
        }
        15%{
            top: 0.4em;
        }
        30%{
            top: 0em;
        }
        45%{
            top: 0.4em;
        }
        60%{
            top: 0.4em;
        }
    }

    @keyframes snap{
    0%{
        transform: rotate(0deg);
    }
    25%{
        transform: rotate(0deg);
    }
    50%{
        transform: rotate(-30deg) translateY(-1em);
    }
    75%{
        transform: rotate(0deg);
    }
    100%{
        transform: rotate(0deg);
    }
    }

    @keyframes wiggle{
    78%{
        transform: rotate(50deg);
        top: 0;
    }
    80%{
        transform: rotate(0deg);
        top: 0.6em;
    }
    82%{
        transform: rotate(50deg);
        top: 0;
    }
    }

    @keyframes whip{
    0%{
        transform: rotate(0deg);
        top: 3.8em;
        left: -1.5em;
    }
    2%{
        transform: rotate(30deg);
        top: 1.8em;
        left: -2.5em;
    }
    10%{
        transform: rotate(0deg);
        top: 3.8em;
        left: -1.5em;
    }
    }
</style>