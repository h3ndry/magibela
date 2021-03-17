<script lang="ts">

    const year: number = Date.now()
</script>

<style>

    footer {
        padding-top: 3.5rem;
        font-weight: 300;
        background: var(--bg-color-2)
        
    }

    footer *  {
        opacity: .8;
    }

    .wrapper {
        max-width: 65rem;
        margin: 0 auto;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        /* grid-template-rows: 1fr 1rem; */
    }

    .link {
        padding-left: 5rem;
        
        
    }

    .wrapper > p {
        padding-top: 2rem;
        text-align: center;
        grid-column: 1 / -1;
    }

</style>

<footer>
    <div class="wrapper">

        <div class="site">
            <h3>McGibela</h3>
            <p>Duis aute irure dolor in reprehenderit voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint  </p>
        </div>

        <div class="link">
            <h3>Links</h3>
            <ul>
                <li><a href="http://www.url.com" target="_blank">Home</a></li>
                <li><a href="http://www.url.com" target="_blank">About</a></li>
                <li><a href="http://www.url.com" target="_blank">Booking</a></li>
                <li><a href="http://www.url.com" target="_blank">Contact</a></li>
            </ul>
        </div>
        <div class="social-network">
            <h3>Social Medial</h3>
            <ul>
                <li><a href="http://www.url.com" target="_blank">Twitter</a></li>
                <li><a href="http://www.url.com" target="_blank">Facebook</a></li>
                <li><a href="http://www.url.com" target="_blank">Instagram</a></li>
            </ul>
        </div>
    <p>Made with love by <a href="wwww.hendry.xyz" target="_blank">Hendry Khoza</a></p>

    </div>
</footer>
