<script lang="ts">
	import Navbar from '$lib/Navbar/Navbar.svelte';
	import TopRight from '$lib/top_right.svelte';

</script>



<Navbar />

<TopRight />

<!--
<div>
{@html Top}
</div>
-->


<main>
	<slot />
</main>

<footer>
	<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
</footer>

<style global lang="scss">
	@use 'src/styles/global';
</style>
