<script>
    import Lollipop from "casually-css/@svelte/lollipop.svelte"
    import Bison from "casually-css/@svelte/bison.svelte"
    import Hippo from "casually-css/@svelte/hippo.svelte"
    import Boba from "casually-css/@svelte/boba.svelte"
    import Dugong from "casually-css/@svelte/dugong.svelte"
    import { elasticIn } from 'svelte/easing';

    // Pop in
    function zoom({ duration }) {
		return {
			duration,
			css: t => {
				const eased = elasticIn(t);

				return `
					transform: scale(${eased}) rotate(${eased * 720}deg);`
			}
		};
	}

    let vis = [false,false,false,false,false,false,false,false]
    let id1 = setInterval(next, 500)
    let tick = 0
    function next() {
        vis[tick] = true
        tick++
        if(tick == vis.length)
            clearInterval(id1)
    }
</script>

<div id="reelCtr">
    <div id="linya"></div>
    {#if vis[0]}
    <div id="ctr1" class="ctr" in:zoom="{{duration: 4000}}">
        <Boba pearlColor="#3e3e3e" lidColor="grey" />
    </div>
    {/if}
    {#if vis[1]}
    <div id="ctr2" class="ctr" in:zoom="{{duration: 4000}}">
        <Dugong bodyColor="ghostWhite" bodyTint="white" bodyShade="lightgrey" outlineColor="#3e3e3e" />
    </div>
    {/if}
    {#if vis[2]}
    <div id="ctr3" class="ctr" in:zoom="{{duration: 4000}}">
        <Lollipop bodyColor="pink" outlineColor="#3e3e3e" />
    </div>
    {/if}
    {#if vis[3]}
    <div id="ctr4" class="ctr" in:zoom="{{duration: 4000}}">
        <Bison bodyColor="tan" hairColor="gainsboro" noseColor="lightgrey" outlineColor="#3e3e3e" />
    </div>
    {/if}
    {#if vis[4]}
    <div id="ctr5" class="ctr" in:zoom="{{duration: 4000}}">
        <Hippo bodyColor="ghostwhite" />
    </div>
    {/if}
</div>

<style>
    #reelCtr{
        height: 100%;
        width: 100%;
        position: relative;
        background-color: khaki;
    }
    #linya{
        position: absolute;
        width: 3vw;
        background-color: #3e3e3e;
        left: 50%;
        height: 0%;
        transform: translateX(-50%);
        animation: desc 16s ease-in-out;
        clip-path: polygon(0% 0%, 100% 0%, 100% 85%, 50% 100%, 0% 85%);
    }
    .ctr{
        height: max-content;
        width: max-content;
        animation: rise 16s linear;
    }
    #ctr1{
        position: absolute;
        left: 20%;
        top: 30%;
    }
    #ctr2{
        position: absolute;
        left: 50%;
        top: 55%;
    }
    #ctr3{
        position: absolute;
        left: 70%;
        top: 42%;
    }
    #ctr4{
        position: absolute;
        left: 15%;
        top: 55%;
    }
    #ctr5{
        position: absolute;
        left: 60%;
        top: 48%;
        transform: rotateY(180deg) !important;
    }

    @keyframes rise{
        0%{
            transform: translateY(0em);
        }
        25%{
            transform: translateY(-100em);
        }
        90%{
            transform: translateY(-100em);
        }
    }

    @keyframes desc{
        0%{
            height: 0%;
        }
        10%{
            height: 50%;
        }
        99%{
            height: 50%;
        }
    }
</style>


