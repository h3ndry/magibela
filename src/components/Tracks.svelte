<script lang="ts">
    import { onMount, onDestroy } from 'svelte';
    import { Tracks } from '../store/top_tracks';
    import Track from './Track.svelte'

    let TracksList = [];
    let loading = true;
    let erro = false

    /* console.log(photos) */

onMount(async () => {
    try {
        // This fuction controle the calls to the API
        const clientId = "9d7a5c3566744f378cea0c3bffeafc32"; // for privacy reason
        const clientSecret = "5d2b6f00972043de8d58b0d228cedc46"; // for privacy reasons
        const artistID = "4SOTLSC4YcH24R2OBF1Zm9";

        const res = await fetch("https://accounts.spotify.com/api/token", {
            method: "POST", 
            headers: {
                "Content-Type": "application/x-www-form-urlencoded",
                "Authorization": `Basic ${btoa(`${clientId}:${clientSecret}`)}`,
            },
            body: "grant_type=client_credentials",
        });

        const res_token = await res.json();


        const result = await fetch(`https://api.spotify.com/v1/artists/${artistID}/top-tracks?market=SA`, {
            method: 'GET',
            headers: { 'Authorization' : 'Bearer ' + res_token.access_token}
        });

        const res_top_tracks = await result.json()

        Tracks.update(() => (res_top_tracks.tracks))

        loading = false


    }  catch(er) {
        loading = false
        erro = true

    }

});
    

	Tracks.subscribe(value => {
        // first 4 track
        const first = value.slice(0,4)
		TracksList = first;
	});

function handleClick(e) {
        const tracksDOM = e.detail.node.querySelectorAll('audio')
        console.log(tracksDOM, 'I am from tracks')
        tracksDOM.forEach(trackDOM => (trackDOM.pause()))
    /* const audio = e.target.closest('.media-controller').querySelector('audio') */
    /* audio.play() */
        /* console.log(e.target.previousSibling) */
            }





</script>

<style>

    .track-list {
        min-height: 29.375rem;
        padding: 4rem 0; }

    .inner{
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2rem 1rem;
        /* grid-column-gap: 1rem; */
        /* grid-row-gap: 2rem; */
        max-width: 65rem }

</style>


<div class="track-list">
    <div class="inner">
        <h2>Top Songs on Spotify</h2>
        <button>show all</button>

        

        {#if loading && !erro}
            <p>...waiting</p>

        {:else if !loading && !erro}

            {#each TracksList as track (track.id)}
                <Track on:stop={handleClick} track={track} />
            {/each}

        {:else if !loading && erro}
            <p>...conection erro</p>
{/if}


    </div>

</div>
