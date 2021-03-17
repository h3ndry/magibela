<script charset="utf-8">
   import MediaController from './media-controller.svelte' 
    import { createEventDispatcher } from 'svelte';

    export let track;
    let isPlaying = false
    let ellipseLength = 386.4305725097656
    let progress = 386.4305725097656

	const dispatch = createEventDispatcher();

	function handleMediaControoler(e) {
        const tracksDOM = e.target.closest('.track-list .inner')
        const audioDOM = e.target.closest('.media-controller').querySelector('audio')
        const preview_duration = 30
        
    
        /* console.log(tracksDOM.querySelector(".ellipse-overlay").getTotalLength()) */
        if (!audioDOM.paused) {
            audioDOM.pause()
            isPlaying = false

            return
        }
    
		dispatch('stop', {
			node: tracksDOM
		});

        audioDOM.play()
        isPlaying = true

        audioDOM.ontimeupdate = () => {
            let currentTime = audioDOM.currentTime;
            progress = ellipseLength - (currentTime / preview_duration) * ellipseLength 
        }

        /* if (audioDOM.ontimeupdate){ */
        /* console.log("is display") */
        /* } else { */
        /* console.log("whast happering") */
        /* } */
	}
    
    let track_img = track.album.images[1]
    console.log(track)

</script>

<style>
    .track {

        display: grid;
        grid-template-columns: 5.25rem 1rem 2fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        grid-column-gap: 1.5rem;

        min-height: 8rem;
        padding: 1rem 2rem;
        border-radius: 10px;
        background: var(--bg-color-2) }
        
    .track-image {
        grid-column: 1 / 2;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;

        display: grid;
        justify-content: center;
        align-content: center;

        width: 5.25rem;
        height: 5.25rem;
        position: relative;
        border-radius: 15px;
        overflow: hidden;
        background: var(--bg-color-1) }
    
    .track-image img {
        width: 110%;
        transform: translateX(-5%);
    }
    .track-image .overlay {
        position: absolute;
        width: 5.25rem;
        height: 5.25rem;
        opacity: .3;
        background: var(--bg-color-1)
    }

    .media-controller{
        grid-column: 4 / -1;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;
        margin: 0;
        padding: 0;

        display: grid;
        justify-content: center;
        align-content: center;

        border-radius: 50%;
        width: 4rem;
        height: 4rem; }
        /* background: var(--bg-color-1) } */
    
    .artist-name, .track-name {
        padding: 0;
        margin: 0;
        opacity: .8;
        /* background-color: var(--bg-color-1); */
        align-self: center;
        grid-column: 2 / span 2; }

    /* .track-name { */
    /*     /1* align-self: center; *1/ */
    /*     /1* justify-self: right *1/ } */

    /* .artist-name { */
    /*     /1* align-self: center; *1/ */
    /*     /1* align-items: bottom; *1/ */
        
    /*    } */

    .icon {
        height: 1.5rem;
        width: 1.5rem;
        background-color: var(--bg-color-1);
        border-radius: 50%;
    }

</style>

<div class="track">
    <div class="track-image">
        <div class="overlay"></div>
        <img src={track_img.url} alt={track.album.album_type} />
    </div>

    <h3 class="artist-name">{track.name}</h3>
    <h3 class="track-name">ft blah blah</h3>

    <span class="icon"></span>
    <span class="icon"></span>

    <figure on:click={handleMediaControoler} class="media-controller"> 
         <audio kind="caption">
             <source
                src={track.preview_url}
                type="audio/ogg"
                kind="caption"
             />
            Your browser does not support the audio element.
        </audio> 
        <MediaController 
            progress={progress}
            ellipseLength={ellipseLength}
            isPlaying={isPlaying}
            on:click />

    </figure>

</div>
