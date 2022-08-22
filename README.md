# Svelte Frame Orchestrator
Play a sequence of full-page Svelte components (called **frames**) in an interval. The resulting "video" is called a **reel**.
Instead of documents slides like Powerpoint, or video frames like .mp4 clips, the Svelte Frame Orchestrator plays web components.

## Run the App
Open a terminal on **svelte-frame-orchestrator**  
1. Install dependencies with `npm install`  
2. Start the app with `npm run dev`  

### Controls
- Press **SPACE** to start playing the Orchestrator. Pressing again will reset the reel to the beginning
- Press **s** to toggle the jingle music on/off. Music is off by default

## Usage
The duration that a frame will stay onscreen before the next frame is loaded defined by an **array of integers prop** that is passed into the Orchestrator in [App.svelte](https://github.com/andreaabellera/svelte-frame-orchestrator/blob/main/src/App.svelte).
```
let myIntervals = [ 4000, 5000, 2000, 1000 ]
```
**Explanation:** The first frame will last for 4 seconds. Then, it's instantly replaced with the second frame that will last for 5 seconds. It is then replaced by the third frame lasting 2 seconds, then the fourth lasting 1 second.  

### Frames
Presently, the Orchestrator is loaded with 16 sample frames that makes up the [Casually CSS Teaser](https://www.youtube.com/watch?v=zKJXCX3J_-k). The sample reel can be played as is. To create your own reel, do the following:
1. With the exception of **_Empty.svelte**, delete the other files present in **src/compo/frames**
2. **_Empty.svelte** will be your default start/end frame. Clear the current code and develop the appearance of the Svelte component to your liking
3. Produce as many new frames (in form of .svelte files) as you wish
4. Import all frames to use into [Orchestrator](https://github.com/andreaabellera/svelte-frame-orchestrator/blob/main/src/compo/Orchestrator.svelte)
5. Manually change the components in if-else blocks to your desired sequence of frames. Remove or add more blocks as needed


*Procedure can be improved in a future distribution of this app*