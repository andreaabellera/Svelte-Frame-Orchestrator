<script>
    export let text = "Casually CSS"
</script>

<div class="meta-container">
    <div class="artboard">
        <link href="https://fonts.googleapis.com/css2?family=Gentium+Basic:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
        <link href="https://fonts.googleapis.com/css2?family=Lancelot&display=swap" rel="stylesheet">
        <link href="https://fonts.googleapis.com/css2?family=PT+Sans:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
          <div class="bleu button">
            <span class="grad-overlay"></span>
            <span class="box-overlay"></span>
            <span class="glare"></span>
            <span class="shade"></span>
            <span class="ult-overlay"></span>
            <span class="glare2"></span>
            <span class="btn-text ptSans">{text}</span>
        </div>
    </div>
</div>

<style>
.meta-container{
    height: 5em;
    width: 20em;
}

.artboard{
  height: inherit;
  width: inherit;
}

.button{
  height: inherit;
  width: inherit;
  position: relative;
  border-top-right-radius: 90%;
  border-bottom-right-radius: 10em;
    border-bottom-left-radius: 100%;
 border-top-left-radius: 10em;
  border: 2px solid;
  display: grid;
  justify-items: center;
  align-items: center;
  overflow: hidden;
  box-shadow: 0.05em 0.1em 0.3em rgba(0,0,0,0.3);
}

.bleu{
  background-color: rgba(198, 60, 104, 0.684);
  background: linear-gradient(to right, #daa2aac2, #da79798e);
  border-top-color: #b25b0544;
  border-right-color: #ab840343;
  border-bottom-color: #c33f023d;
  border-left-color: #aa63053d;	
}

.bleu:hover{
  transition: 0.3s ease-out;
  filter: brightness(105%);
  cursor: url(https://ipfs.fleek.co/ipfs/bafybeicuryldiwjiv5qynwnswb6qxv2lujyxvcv3oodzrbegtq247jubvm), pointer;
}

.bleu:active{
  filter: brightness(90%);
  background: linear-gradient(to right, #9400006d, rgba(152, 19, 19, 0.388)13);
}

.grad-overlay{
  position: absolute;
  z-index: 2;
  bottom: 0;
  height: 50%;
  width: 100%;
  background: linear-gradient(350deg, rgba(169, 9, 177, 0.3, rgba(200, 73, 255, 0.1)0.1));
}

.box-overlay{
  position: relative;
  z-index: 4;
  height: 80%;
  width: 96%;
  background-image: linear-gradient(to right, rgba(255,255,255,0.1), rgba(255,255,255,0.05));
}

.glare {
  position: absolute;
  z-index: 3;
  top: 5%;
  left: 2%;
  border-radius: 30%;
  height: 0.6em;
  width: 95%;
  padding: 8px 0;
  background-image: linear-gradient(to right, rgba(200, 190, 255, 0.049) 2%, rgba(255, 255, 255, 0.121) 10%, rgba(255, 187, 0, 0.133) 80%, rgba(0, 0, 255, 0));
}

.glare2{
  position: absolute;
  z-index: 7;
  top: 0;
  left: 0;
  height: 40%;
  width: 40%;
  padding: 8px 0;
  background-image: radial-gradient(rgba(255, 255, 255, 0.296), rgba(255,255,255,0), rgba(255,255,255,0));
}

.shade {
  position: absolute;
  z-index: 2;
  bottom: 10%;
  left: 4%;
  border-radius: 40%;
  height: 0.8em;
  width: 93%;
  padding: 8px 0;
  background-image: radial-gradient(rgba(139, 127, 0, 0.518rgba(232, 196, 148, 0.501)96, 148) 100%);
}

.ult-overlay{
  position: absolute;
  z-index: 6;
  height: 100%;
  width: 100%;
  background-image: radial-gradient(rgba(203, 125, 35, 0.4rgba(182, 71, 7, 0.4).4rgba(255, 250, 190, 0.5).5));
}

.btn-text{
  position: absolute;
  z-index: 8;
  /* font-family: 'Gentium Basic', serif;
  font-weight: 800; */
  /* font-family: 'Lancelot', cursive; */
    font-family: 'PT Sans', sans-serif;
    font-weight: 700;
  font-size: 3ex;
  color: #EEEEE6;
  text-shadow: rgba(80, 73, 73, 0.5) -2px -2px 2px;
}


</style>