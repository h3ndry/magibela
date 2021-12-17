<script lang="ts">
	import Navbar from '$lib/Navbar/Navbar.svelte';
	import TopRight from '$lib/top_right.svelte';
	import Footer from '$lib/footer/Footer.svelte';

</script>

<Navbar />

<TopRight />

<main>
	<slot />
</main>

<Footer />

<style global lang="scss">
	@use 'src/styles/global';
</style>
