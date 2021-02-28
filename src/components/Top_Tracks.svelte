<script lang="ts">
    import { onMount, onDestroy } from 'svelte';
    import { Tracks } from '../store/top_tracks';

    let TracksList = [];

    /* console.log(photos) */

    const fetchImage = onMount(async () => {
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


	});
    

	const unsubscribe = Tracks.subscribe(value => {
		TracksList = value;
	});



</script>

<style>

    .track-list {
        min-width: 30rem;
    }

</style>


<div class="track-list">

    {#await fetchImage}
        <p>...waiting</p>
    {:then data}

        {#each TracksList as Track}
            <p>{Track.name}</p> 
        {/each}

    {:catch error}
        <p>An error occurred!</p>
    {/await}

</div>
