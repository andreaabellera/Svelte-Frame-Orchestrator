<script>
    export let color = "#ffc0cb"
    export let height = "5em"
    export let width = "5em"
</script>

<div class="meta-container" style="height:{height}; width:{width};">
        <div class="blossom">
            <div class="half-height"><div class="petal" style="background-color:{color}"></div></div>
            <div class="half-height"><div class="petal" style="background-color:{color}"></div></div>
            <div class="half-height"><div class="petal" style="background-color:{color}"></div></div>
            <div class="half-height"><div class="petal" style="background-color:{color}"></div></div>
            <div class="half-height"><div class="petal" style="background-color:{color}"></div></div>
            <div class="mid"></div>
        </div>
</div>

<style>

.blossom{
    position: relative;
    height: inherit;
    height: inherit;
    animation: spin 0.8s ease-in-out;
}

.mid{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    height: 30%;
    width: 30%;
    z-index: 4;
    background-color: white;
}

.half-height{
    height: 100%;
    width: 100%;
    position: absolute;
    z-index: 5;
    display: grid;
    grid-template-rows: 50% 50%;
}

.half-height:nth-of-type(2){
    transform: rotate(72deg);
    }
.half-height:nth-of-type(3){
    transform: rotate(144deg);
}
.half-height:nth-of-type(4){
    transform: rotate(216deg);
}
.half-height:nth-of-type(5){
    transform: rotate(288deg);
}

.petal{
    height: 100%;
    width: 45%;
    border-top-left-radius: 100%;
    border-top-right-radius: 100%;
    border-bottom-left-radius: 100%;
    box-shadow: 0.05em 0.1em 0.3em rgba(0,0,0,0.3);
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(144deg);
  }
}


</style>