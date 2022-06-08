<div class="meta-container">
    <div class="artboard">
        <div class="blossom">
          <div class="stabilize">
            <div class="half-height"><div class="petal"></div></div>
            <div class="half-height"><div class="petal"></div></div>
            <div class="half-height"><div class="petal"></div></div>
            <div class="half-height"><div class="petal"></div></div>
            <div class="half-height"><div class="petal"></div></div>
          </div>
        </div>
        <div class="teastring">
          <div class="string"></div>
          <div class="paper">
            <div class="paper-top"></div>
            <div class="paper-bottom"></div>
          </div>
        </div>
        <div class="matcha-set">
          <div class="matchaCup">
            <div class="matchaCup-front">
              <div class="matchaCup-front-top"></div>
              <div class="matchaCup-front-bottom"></div>
            </div>
            <div class="matcha">
              <div class="stabilize">
                <div class="surface"></div>
              </div>
            </div>
            <div class="matchaCup-back"></div>
          </div>
          <div class="wood">
            <div class="wood-inner"></div>
          </div>
        </div>
        <div class="handle"></div>
    </div>
</div>

<style>
    .meta-container{
        height: 17em;
        width: 20em;
    }

    @media screen and (max-width: 600px) {
        .meta-container{
            margin-top: 1.5em;
            transform: scale(0.8) translateX(5vw);
        }
    }

    :root{
    --matchaCup: #3e4044;
    --cupInner: #aa3333;
    --matcha: linear-gradient(120deg, #608850 0%, #78AE60, #88BB80 80%, #67A070 90%, #656840 100%);
    --wood: #565144;
    --paper: #dd9922;
    --woodTop: linear-gradient(to top, tan, rgb(170, 146, 113));
    --blossom: #ffc0cb;
    }

    .artboard, .matchaCup{
    position: relative;
    height: inherit;
    height: inherit;
    }

    .matcha-set:hover, .teastring:hover, .blossom:hover{
    cursor: pointer;
    }

    .matcha-set{
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-rows: 1fr auto; 
    }

    .matchaCup-front{
    position: absolute;
    z-index: 5;
    top: 4em;
    height: 10em;
    width: 15.5em;
    display: grid;
    grid-template-rows: 30% 1fr;
    }

    .matchaCup-front-top{
    background-image: radial-gradient(ellipse at top, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 71%, var(--matchaCup) 71.5%);
    }

    .matchaCup-front-bottom{
    background-image: linear-gradient(to top, #1e1e1e 0%, var(--matchaCup) 100%);
    border-bottom-left-radius: 9em;
    border-bottom-right-radius: 9em;
    }

    .matcha{
    position: absolute;
    z-index: 4;
    background-image: var(--matcha);
    top: 2.5em;
    height: 7em;
    width: 15.5em;
    border-radius: 100%;
    overflow: hidden;
    }

    .stabilize{
    height: 100%;
    width: 100%;
    position: relative;
    }

    .surface{
    position: absolute;
    height: 100%;
    width: 100%;
    background-image: radial-gradient(ellipse, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 100%);
    animation: surface 3s ease-out infinite;
    }

    .matchaCup-back{
    position: absolute;
    z-index: 3;
    background-image: radial-gradient(ellipse at bottom, #2e2e2e 0%, var(--cupInner) 70%);
    height: 8em;
    width: 15.5em;
    border-radius: 100%;
    }

    .wood{
    position: relative;
    overflow: hidden;
    background-color: var(--wood);
    height: 6.5em;
    width: 100%;
    transform: translateX(-1.85em);
    border-radius: 40%;
    }

    .wood-inner{
    position: absolute;
    height: 55%;
    width: 100%;
    background-image: var(--woodTop);
    border-radius: 9em;
    }

    .teastring{
    position: absolute;
    z-index: 6;
    top: 37%;
    left: 20%;
    height: 40%;
    width: 2em;
    display: grid;
    grid-template-rows: 1fr 50%; 
    justify-items: center;
    }

    .string{
    background-color: gainsboro;
    width: 2px;
    transform: translateY(0.5em);
    z-index: 2;
    }

    .paper{
    height: 100%;
    width: 100%;
    display: grid;
    grid-template-rows: 50%, 50%;
    }

    .paper-top{
    clip-path: polygon(0% 100%, 50% 0%, 100% 100%);
    background-image: radial-gradient(circle, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 20%, var(--paper) 20%, var(--paper) 100%);
    }

    .paper-bottom{
    background-color: var(--paper);
    }

    .blossom{
    position: absolute;
    z-index: 7;
    top: 60%;
    right: 15%;
    height: 5em;
    width: 5em;
    }

    .petal{
    height: 100%;
    width: 2.3em;
    background-color: var(--blossom);
    border-top-left-radius: 100%;
    border-top-right-radius: 100%;
    border-bottom-left-radius: 100%;
    }

    .half-height{
    height: 100%;
    width: 100%;
    position: absolute;
    display: grid;
    grid-template-rows: 50% 50%;
    }

    .half-height:nth-of-type(2){
    transform: rotate(72deg);
    filter:brightness(90%);
    }
    .half-height:nth-of-type(3){
    transform: rotate(144deg);
    filter:brightness(83%);
    }
    .half-height:nth-of-type(4){
    transform: rotate(216deg);
    filter:brightness(75%);
    }
    .half-height:nth-of-type(5){
    transform: rotate(288deg);
    filter:brightness(83%);
    }

    .handle{
    position: absolute;
    z-index: 1;
    height: 4em;
    width: 3.5em;
    top: 4em;
    right: 0;
    filter: brightness(85%);
    border-style: solid;
    border-width: 1.25em;
    border-color: var(--matchaCup);
    border-bottom-right-radius: 3em;
    border-top-right-radius: 3em;
    border-top-left-radius: 3em;
    }

    @keyframes surface{
        0% {
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.01) 3%, rgba(255,255,255,0.15) 5%, rgba(255,255,255,0.1) 10%, rgba(255,255,255,0.01) 15%, rgba(255,255,255,0.01) 43%, rgba(255,255,255,0.1) 45%, rgba(255,255,255,0.01) 85%);
        }
        20% {
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 5%, rgba(255,255,255,0.15) 10%, rgba(255,255,255,0.1) 15%, rgba(255,255,255,0.01) 20%, rgba(255,255,255,0.01) 30%, rgba(255,255,255,0.1) 50%, rgba(255,255,255,0.01) 90%);
        }
        35% {
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 10%, rgba(255,255,255,0.15) 15%, rgba(255,255,255,0.1) 20%, rgba(255,255,255,0.01) 25%, rgba(255,255,255,0.01) 48%, rgba(255,255,255,0.1) 55%, rgba(255,255,255,0.01) 95%);
        }
        50%{
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.01) 0%, rgba(255,255,255,0.01) 15%, rgba(255,255,255,0.15) 20%, rgba(255,255,255,0.1) 25%, rgba(255,255,255,0.01) 30%, rgba(255,255,255,0.01) 58%, rgba(255,255,255,0.1) 60%, rgba(255,255,255,0.01) 100%);
        }
        70%{
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.01) 20%, rgba(255,255,255,0.15) 35%, rgba(255,255,255,0.05) 55%, rgba(255,255,255,0.01) 60%, rgba(255,255,255,0.01) 68%, rgba(255,255,255,0.1) 70%);
        }
        85%{
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.15) 5%, rgba(255,255,255,0.1) 10%, rgba(255,255,255,0.01) 30%, rgba(255,255,255,0.01) 45%, rgba(255,255,255,0.1) 60%, rgba(255,255,255,0.01) 80%);
        }
        100% {
            background-image: radial-gradient(ellipse, rgba(255,255,255,0.15) 0%, rgba(255,255,255,0.1) 15%, rgba(255,255,255,0.01) 15%, rgba(255,255,255,0.01) 30%, rgba(255,255,255,0.1) 68%, rgba(255,255,255,0.01) 100%);
        }
    }
</style>