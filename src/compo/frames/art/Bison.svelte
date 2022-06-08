<div class="meta-container">
    <div class="artboard">
        <div class="bison">
            <div class="bison-upper">
              <div class="bison-horn horn-left"></div>
              <div class="bison-horn horn-right"></div>
              <div class="bison-mustache fur"></div>
              <div class="bison-ear ear-left"></div>
              <div class="bison-ear ear-right"></div>
              <div class="bison-head">
                <div class="head-top">
                  <div class="se-sharp fur"></div>
                  <div class="sw-sharp fur"></div>
                </div>
                <div class="head-bottom">
                  <div class="ne-sharp fur stabilize">
                    <div class="eye eye-left">
                      <div class="eye-pupil-left"></div>
                    </div>
                  </div>
                  <div class="fur stabilize">
                    <div class="bison-nose">
                      <div class="nose-top">
                        <div class="nostril-left"></div>
                        <div class="nostril-right"></div>
                      </div>
                      <div class="nose-bottom"></div>
                    </div>
                  </div>
                  <div class="nw-sharp fur stabilize">
                    <div class="eye eye-right">
                      <div class="eye-pupil-right"></div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="bison-hair">
                <div class="se-sharp hair sect1"></div>
                <div class="sw-sharp hair sect2"></div>
                <div class="seg1">
                  <div class="ne-sharp hair"></div>
                </div>
                <div class="seg2">
                  <div class="hair"></div>
                  <div class="nw-sharp hair"></div>
                </div>
                <div class="seg3">
                  <div class="hair"></div>
                  <div class="ne-sharp hair"></div>
                </div>
                <div class="seg3">
                  <div class="hair"></div>
                  <div class="nw-sharp hair"></div>
                </div>
                <div class="seg4">
                  <div class="nw-sharp hair"></div>
                </div>
              </div>
              <div class="bison-body"></div>
              <div class="bison-tail">
                <div></div>
                <div class="tail1 se-sharp"></div>
                <div></div>
                <div class="tail2">   <div class="tail-line"></div>   </div>
                <div class="tail3"></div>
              </div>
            </div>
            <div class="bison-leg front-near">
              <div class="leg-top fur"></div>
              <div class="leg-bottom fur"></div>
            </div>
            <div class="bison-leg front-far">
              <div class="leg-top fur"></div>
              <div class="leg-bottom fur"></div>
            </div>
            <div class="bison-leg back-near">
              <div class="leg-top fur"></div>
              <div class="leg-bottom fur"></div>
            </div>
            <div class="bison-leg back-far">
              <div class="leg-top fur"></div>
              <div class="leg-bottom fur"></div>
            </div>
        </div>
    </div>
</div>

<style>
    .meta-container{
        height: 26em;
        width: 35em;
    }

    :root{
    --outlineBison: #222222;
    --hair: #564C45;
    --fur: #80725E;
    --horn: #E7E3DA;
    --nose: #554D50;
    }

    .artboard{
    position: relative;
    height: inherit;
    height: inherit;
    }

    .bison, .bison-upper{
    position: relative;
    z-index: 3;
    height: inherit;
    width: inherit;
    }

    .bison:hover{
    cursor: url(https://ipfs.fleek.co/ipfs/bafybeiafet7hldlwiwpj5bbftxizcspsvi3ernckqpklgbuup2lq6rtq6m), pointer;
    }

    .bison-upper{
        animation: dancing 2s ease-in-out infinite;
    }

    .hair{
    background-color: var(--hair);
    }

    .fur{
    background-color: var(--fur);
    }

    .bison-body{
    position: absolute;
    z-index: 2;
    left: 2em;
    top: 2em;
    height: 18em;
    width: 26em;
    background-color: var(--fur);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-style: solid;
    border-top-left-radius: 100%;
    border-top-right-radius: 60%;
    border-bottom-left-radius: 50%;
    border-bottom-right-radius: 90%;
    }

    .bison-head{
    position: absolute;
    z-index: 4;
    right: 3.5em;
    top: 2em;
    height: 15em;
    width: 12em;
    display: grid;
    grid-template-rows: 35% 65%;
    }

    .bison-nose{
    position: absolute;
    z-index: 6;
    height: 3em;
    width: 4em;
    left: 1.2em;
    top: 60%;
    display: grid;
    grid-template-rows: 65% 35%;
    justify-items: center;
    }

    .nose-top{
    position: relative;
    width: 100%;
    background-color: var(--nose);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-style: solid;
    border-top-left-radius: 90%;
    border-top-right-radius: 90%;
    border-bottom-left-radius: 40%;
    border-bottom-right-radius: 40%;
    overflow: hidden;
    }

    .nostril-left{
    position: absolute;
    z-index: 8;
    top: 0.5em;
    height: 0.75em;
    width: 1em;
    background-color: var(--outlineBison);
    border-radius: 100%;
    transform: rotate(45deg);
    }

    .nostril-right{
    position: absolute;
    z-index: 8;
    right: 0;
    top: 0.5em;
    height: 0.75em;
    width: 1em;
    background-color: var(--outlineBison);
    border-radius: 100%;
    transform: rotate(-45deg);
    }

    .nose-bottom{
    background-color: var(--nose);
    border-width: 0.3em;
    width: 80%;
    border-color: var(--outlineBison);
    border-style: solid;
    border-top-style: none;
    border-bottom-left-radius: 3em;
    border-bottom-right-radius: 3em;
    }

    .nose-bottom:hover{
        animation: chewing 8s linear infinite;
    }

    .bison-mustache{
    position: absolute;
    z-index: 6;
    right: 6em;
    top: 17em;
    height: 1.5em;
    width: 4.8em;
    filter: brightness(40%);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-style: solid;
    border-top-style: none;
    border-bottom-left-radius: 5em;
    border-bottom-right-radius: 5em;
    }

    .head-top{
    display: grid;
    grid-template-columns: 60% 45%;
    }

    .head-bottom{
    display: grid;
    grid-template-columns: 35% 40% 30%;
    border-color: var(--outlineBison);
    border-bottom-left-radius: 65%;
    border-bottom-right-radius: 50%;
    }

    .bison-horn{
    position: absolute;
    z-index: 4;
    top: 1.5em;
    height: 4em;
    width: 4em;
    background-image: radial-gradient(ellipse at top right, 
    rgba(0,0,0,0) 0%, rgba(0,0,0,0) 50%, 
    var(--outlineBison) 51%, var(--outlineBison) 54%, var(--horn) 55%);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-bottom-style: solid;
    border-left-style: solid;
    border-bottom-left-radius: 80%;
    border-top-left-radius: 50%;
    }

    .horn-left{
    left: 18em;
    }

    .horn-right{
    left: 29em;
    transform: rotateY(180deg);
    }

    .bison-ear{
    position: absolute;
    z-index: 5;
    top: 6em;
    background-color: var(--fur);
    height: 2.5em;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    }

    .ear-left{
    right: 15em;
    width: 3em;
    border-style: solid;
    border-right-style: none;
    border-bottom-left-radius: 90%;
    border-top-left-radius: 10%;
    border-top-right-radius: 40%;
    }

    .ear-right{
    right: 0;
    width: 3em;
    border-style: solid;
    border-left-style: none;
    border-bottom-right-radius: 90%;
    border-top-right-radius: 10%;
    border-top-left-radius: 40%;
    }

    .stabilize{
    position: relative;
    }

    .eye{
    position: absolute;
    top: 1em;
    z-index: 6;
    height: 2.5em;
    background-color: whitesmoke;
    border-width: 0.2em;
    border-color: var(--outlineBison);
    border-style: solid;
    overflow: hidden;
    display: flex;
    align-items: flex-end;
    animation: gazing 10s linear infinite;
    }

    .eye-left{
    right: 0;
    border-top-left-radius: 2em;
    border-bottom-left-radius: 3em;
    border-bottom-right-radius: 40%;
    border-top-right-radius: 40%;
    width: 1.25em;
    justify-content: flex-end;
    }

    .eye-right{
    left: 40%;
    border-top-right-radius: 2em;
    border-bottom-right-radius: 3em;
    border-bottom-left-radius: 40%;
    border-top-left-radius: 40%;
    width: 1em;
    }

    .eye-pupil-left{
    height: 80%;
    width: 70%;
    background-color: var(--outlineBison);
    border-top-left-radius: 3em;
    border-bottom-left-radius: 3em;
    }

    .eye-pupil-right{
    height: 80%;
    width: 70%;
    background-color: var(--outlineBison);
    border-top-right-radius: 3em;
    border-bottom-right-radius: 3em;
    }

    .bison-hair{
    position: absolute;
    z-index: 3;
    top: 0;
    right: 2.5em;
    height: 23em;
    width: 24em;
    display: grid;
    grid-template-rows: 6em 1fr;
    grid-template-columns: 35% 10% 20% 10% 25%;
    }

    .bison-tail{
    animation: swaying 0.8s ease-in-out infinite;
    }

    .sect1{
    grid-column: 1/4;
    }

    .sect2{
    grid-column: 4/6;
    }

    .seg1{
    height: 85%;
    }

    .seg2{
    display: grid;
    grid-template-rows: 70% 15%;
    }

    .seg3{
    display: grid;
    grid-template-rows: 70% 30%;
    }

    .seg4{
    display: grid;
    grid-template-rows: 80% 20%;
    }

    .bison-tail{
    position: relative;
    z-index: 3;
    height: auto;
    width: 3.5em;
    display: grid;
    grid-template-rows: 4.5em 4.5em 1em;
    grid-template-columns: 50% 50%;
    left: 0;
    top: 10em;
    }

    .bison-tail .se-sharp{
    border-top-width: 0em;
    }

    .tail1{
    background-color: var(--fur);
    border-color: var(--outlineBison);
    border-left-style: solid;
    }

    .tail2{
    background-color: var(--fur);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-left-style: solid;
    clip-path: polygon(0% 0%, 69% 0%, 29% 100%, 0% 100%);
    }

    .tail-line{
    width: 0.3em;
    height: 100%;
    background-color: var(--outlineBison);
    transform: rotate(5deg);
    clip-path: polygon(70% 0%, 100% 0%, 100% 100%, 0% 100%);
    }

    .tail3{
    background-color: var(--hair);
    grid-column: 1/3;
    border-top-right-radius: 50%;
    border-top-left-radius: 1em;
    border-bottom-left-radius: 50%;
    transform: rotate(90deg);
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-style: solid;
    }


    .bison-leg{
    position: absolute;
    height: 9em;
    width: 6em;
    display: grid;
    grid-template-rows: 50% 50%;
    grid-template-columns: 45% 55%;
    }

    .leg-top{
    grid-column: 1/3;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-left-style: solid;
    border-right-style: solid;
    border-bottom-style: solid;
    border-bottom-right-radius: 80%;
    border-bottom-left-radius: 90%;
    }

    .leg-bottom{
    grid-column: 1/2;
    grid-row: 2/3;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-left-style: solid;
    border-right-style: solid;
    border-bottom-style: solid;
    border-top-left-radius: 40%;
    transform: translate(1em, -1em);
    }

    .front-near{
    z-index: 2;
    top: 18em;
    left: 16em;
    overflow: hidden;
    animation: footwork 8s ease-in-out infinite;
    }

    .front-far{
    z-index: 1;
    top: 17em;
    left: 24em;
    filter: brightness(40%);
    animation: footwork 8s ease-in-out infinite;
    animation-delay: 6s;
    }

    .back-near{
    z-index: 5;
    top: 18em;
    left: 5em;
    overflow: hidden;
    animation: footwork 8s ease-in-out infinite;
    animation-delay: 4s;
    }

    .back-far{
    z-index: 1;
    top: 17em;
    left: 11em;
    filter: brightness(40%);
    animation: footwork 8s ease-in-out infinite;
    animation-delay: 2s;
    }

    /*===================
    // COLORS
    ===================*/

    .fur{
    background-color: var(--fur);
    }

    .hair{
    background-color: var(--hair);
    }

    /*===================
    // CURVE SHAPES 
    ===================*/

    .se-sharp{
    border-top-left-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-top-style: solid;
    border-left-style: solid;
    }

    .ne-sharp{
    border-bottom-left-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-bottom-style: solid;
    border-left-style: solid;
    }

    .nw-sharp{
    border-bottom-right-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-bottom-style: solid;
    border-right-style: solid;
    }

    .sw-sharp{
    border-top-right-radius: 100%;
    height: 100%;
    width: 100%;
    border-width: 0.3em;
    border-color: var(--outlineBison);
    border-top-style: solid;
    border-right-style: solid;
    }


    @keyframes chewing{
    0%{
        width: 80%;
    }
    5%{
        width: 50%;
    }
    10%{
        width: 80%;
    }
    15%{
        width: 50%;
    }
    20%{
        width: 80%;
    }
    25%{
        width: 50%;
    }
    30%{
        width: 80%;
    }
    }

    @keyframes gazing{
    10%{
        align-items: center;
    }
    80%{
        align-items: flex-start;
    }
    81%{
        align-items: center;
    }
    82%{
        align-items: flex-end;
    }
    }

    @keyframes swaying{
    0%{
        transform: rotate(0deg);
    }
    50%{
        transform: rotate(3deg);
    }
    100%{
        transform: rotate(0deg);
    }
    }

    @keyframes dancing{
    0%{
        transform: translate(0em, 0em);
    }
    25%{
        transform: translate(0.5em, 1em) rotate(3deg);
    }
    50%{
        transform: translate(1em, 0em);
    }
    75%{
        transform: translate(0.5em, 1em);
    }
    100%{
        transform: translate(0em, 0em);
    }
    }

    @keyframes footwork{
    0%{
        transform: translateY(0em);
    }
    3%{
        transform: translateY(-0.5em);
    }
    5%{
        transform: translateY(0em);
    }
    }
</style>