<script lang="ts">
	import { page } from '$app/stores';
	/* import logo from './svelte-logo.svg'; */
	let showMenu = false;

	function toggleMenu (  ) {
		showMenu = !showMenu	
	}	

</script>

<div class="navbar">
	<div class="inner">
		<a class="logo" href="/"> MaGibela </a>

		<aside>
			<svg viewBox="0 0 500 500" class:active={showMenu} on:click={toggleMenu}>
				<g transform="matrix(1.3333333,0,0,-1.3333333,-397.99812,534.00975)">
					<path
						d="m 325.52894,292.58628 h 320.93884 c 14.76322,0 26.74552,12.36189 26.74552,27.81409 0,13.90705 -11.9823,26.26873 -26.74552,26.26873 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-26.26873 0,-15.4522 11.98207,-27.81409 26.74531,-27.81409 z M 646.46778,240.04882 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-27.81387 0,-13.90706 11.98207,-26.26894 26.74531,-26.26894 h 320.93884 c 14.76322,0 26.74552,12.36188 26.74552,26.26894 0,15.45219 -11.9823,27.81387 -26.74552,27.81387 z m 0,-106.62026 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-27.81388 0,-13.907045 11.98207,-26.268932 26.74531,-26.268932 h 320.93884 c 14.76322,0 26.74552,12.361887 26.74552,26.268932 0,15.4522 -11.9823,27.81388 -26.74552,27.81388 z"
					/>
				</g>
			</svg>

			<nav class="nav mobi" class:visible={showMenu}>
				<ul>
					<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
					<li class:active={$page.path === '/about'}>
						<a sveltekit:prefetch href="/about">About</a>
					</li>
					<li class:active={$page.path === '/booking'}>
						<a sveltekit:prefetch href="/booking">Booking</a>
					</li>
					<li class:active={$page.path === '/contact'}>
						<a sveltekit:prefetch href="/contact">Contact</a>
					</li>
				</ul>
			</nav>
		</aside>

		<nav class="nav desk">
			<ul>
				<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
				<li class:active={$page.path === '/about'}>
					<a sveltekit:prefetch href="/about">About</a>
				</li>
				<li class:active={$page.path === '/booking'}>
					<a sveltekit:prefetch href="/booking">Booking</a>
				</li>
				<li class:active={$page.path === '/contact'}>
					<a sveltekit:prefetch href="/contact">Contact</a>
				</li>
			</ul>
		</nav>
	</div>
</div>

<style src="styles.scss" lang="scss"></style>
