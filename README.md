![Svelte Frame Orchestrator clip demo](/public/banner.gif)
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
Head to `src/App.svelte` to setup frames and audio

### Change or Add Reel Music
The easiest way is directly replace `public/jingle.mp3` with an audio file of the same filename and extension type, but you can also define a different title:
- Add desired audio file inside the `public` directory  
- In [src/App.svelte](/src/App.svelte), locate the line  
`let audioPath = '/jingle.mp3'`  
and replace `jingle.mp3` with your audio's filename

### Creating a Reel
Head to [src/App.svelte](/src/App.svelte) and locate the **reel** array variable
```
/*=============================================
    reel
        Defines the sequence of frames and duration they stay on screen
        Frame attributes:
        . component: .svelte component - component name to load into window  
        . duration: integer - time to display component in milliseconds 
===============================================*/
let reel = [
    // Every row below is a 'frame', a single entry played on the resulting video reel
    { component: SummonBison, duration: 4000 },
    { component: SummonHippo, duration: 4000 },
    { component: BisonHippo, duration: 2000 },
    { component: FourGrid, duration: 1000 },
    ... entries omitted ...
    { component: CasuallyRoadshow, duration: 11000 }
]
```

**Explanation:** The first frame displays a specific component lasting for 4 seconds. Then, it's instantly replaced with the second frame that features a different component that lasts for 4 seconds. It is then replaced by the third frame lasting 2 seconds, then the fourth lasting 1 second. Similar behavior shall continue until the last frame which lasts 11 seconds.

### Changing the Sample Frames
Presently, the Orchestrator is loaded with 16 sample frames that makes up the [Casually CSS Teaser](https://www.youtube.com/watch?v=zKJXCX3J_-k). The sample reel can be played as is. To create your own reel, do the following:
1. With the exception of **_Empty.svelte**, delete the other files present in **src/frames**
2. **_Empty.svelte** will be your default start/end frame. Clear the current code and develop the appearance of the Svelte component to your liking
3. Produce as many new frames (in form of .svelte files) as you wish
4. Import all frames to use into [src/App.svelte](/src/App.svelte)
5. Delete all entries under the `reel` array to start fresh  
`let reel = []`
5. Separated by commas, add an object entry into the `reel` array for every frame to be played
> *Each entry must include an imported Svelte component name, and the duration to display it for. The sample convention below can be followed*  
`{component: ImportedComponentName, duration: 1000}`