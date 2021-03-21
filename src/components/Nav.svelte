<script lang="ts">
	export let segment: string;
</script>

<style>
	nav {
		/* border-bottom: 1px solid rgba(255,62,0,0.1); */
		font-weight: 300;
		padding: .5em 1em;
        width: 100%;
        /* background-color: rgba(255, 255, 255, .03); */
        z-index: 99;

        position: fixed;
        top: 0
	}
    div.logo {
		font-weight: 400;
          display: grid;
          justify-content: center;
          align-content: center;
        /* background-color: red */
    }

    nav .wrapper  {
    margin: 0 auto;
        max-width: 68rem;
        display: flex;
        justify-content: space-between
    }

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
    <div class="wrapper">
    <div class="logo"><h2>MaGibela</h2></div>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">home</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">about</a></li>
		<li><a aria-current="{segment === 'booking' ? 'page' : undefined}" href="booking">Booking</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact">Contact</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen 
		<li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li>-->
	</ul>

    </div>
</nav>
