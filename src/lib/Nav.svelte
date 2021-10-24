<script lang="ts">
	import { page } from '$app/stores';
	/* import logo from './svelte-logo.svg'; */
	let showMenu = false;
</script>

<nav>
	<a class="logo" href="https://kit.svelte.dev"> MaGibela </a>

	<svg class="menu" viewBox="0 0 500 500" on:click={() => (showMenu = !showMenu)}>
		<g transform="matrix(1.3333333,0,0,-1.3333333,-397.99812,534.00975)"
			><path
				d="m 325.52894,292.58628 h 320.93884 c 14.76322,0 26.74552,12.36189 26.74552,27.81409 0,13.90705 -11.9823,26.26873 -26.74552,26.26873 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-26.26873 0,-15.4522 11.98207,-27.81409 26.74531,-27.81409 z M 646.46778,240.04882 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-27.81387 0,-13.90706 11.98207,-26.26894 26.74531,-26.26894 h 320.93884 c 14.76322,0 26.74552,12.36188 26.74552,26.26894 0,15.45219 -11.9823,27.81387 -26.74552,27.81387 z m 0,-106.62026 H 325.52894 c -14.76324,0 -26.74531,-12.36168 -26.74531,-27.81388 0,-13.907045 11.98207,-26.268932 26.74531,-26.268932 h 320.93884 c 14.76322,0 26.74552,12.361887 26.74552,26.268932 0,15.4522 -11.9823,27.81388 -26.74552,27.81388 z"
				id="path2210"
			/></g
		></svg
	>

	<div class="nav-list" class:active={showMenu}>
		<ul>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.path === '/about'}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
			<li class:active={$page.path === '/about'}>
				<a sveltekit:prefetch href="/about">Booking</a>
			</li>
			<li class:active={$page.path === '/about'}>
				<a sveltekit:prefetch href="/about">Contact</a>
			</li>
			<!--<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>-->
		</ul>
	</div>
</nav>

<style>
	nav {
		/* overflow-x: hidden; */
		position: relative;
		display: block;
		display: flex;
		width: 90%;
		justify-content: space-between;
		max-width: 1024px;
		margin: 0 auto;
		padding: 1rem 0;
	}

	.nav-list {
		display: none;

		right: -10%;
		top: 0;
		position: absolute;
		background-color: #3b3b3b;
		height: 100vh;
	}

	.nav-list.active {
		display: flex;
	}

	 ul {
		padding: 0;
		margin: 0;
		height: 3em;

		padding: 4rem;

		/* justify-content: center; */
		/* align-items: center; */
		list-style: none;
		background-size: contain;
	}

	.menu {
		height: 2rem;
		width: 2rem;
		position: relative;
		z-index: 100;
	}

	.menu path {
		fill: var(--pure-white);
		stroke-width: 3;
	}

	li {
		height: 100%;
		margin: 2rem auto;
		text-align: center;
	}

	/* li.active::before { */
	/* 	--size: 6px; */
	/* 	content: ''; */
	/* 	width: 0; */
	/* 	height: 0; */
	/* 	position: absolute; */
	/* 	top: 0; */
	/* 	left: calc(50% - var(--size)); */
	/* 	border: var(--size) solid transparent; */
	/* 	border-top: var(--size) solid var(--accent-color); */
	/* } */

	.logo {
		align-items: center;
		display: flex;
		font-weight: bold;
		color: var(--pure-white);
		font-size: 1.5rem;
		letter-spacing: 1px;
	}

	.nav-list a {
		align-items: center;
		width: 100%;
		height: 100%;
		/* font-weight: 700; */
		font-size: 1rem;
		text-transform: capitalize;
		text-decoration: none;
		/* background-color: red; */
		transition: color 0.2s linear;

		text-align: right;
	}

	a:hover {
		color: var(--accent-color);
	}

	@media (min-width: 450px) {
		.menu {
			display: none;
		}

	ul {
		padding: 0;
		justify-content: center;
		align-items: center;
		padding: 0;
		display: flex;
	}

		.nav-list {
		position: relative;
			display: flex;
			background-color: transparent;
			height: auto;
		right: unset;
		top: unset;
			/* background-color: red; */
		}


		.nav-list a {
			display: flex;
		padding: 0 .5rem;
        /* height: 3rem; */
		/* letter-spacing: 0.1em; */
		}
	}

    li {
		/* margin: 0 auto; */

    }


</style>
