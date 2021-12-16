<script lang="ts">
	import Nav from '$lib/Navbar/Navbar.svelte';
</script>

<Nav />

<main>
	<slot />
</main>

<footer>
	<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
</footer>

<style global lang="scss">
	@use 'src/styles/global';
</style>
