<script lang="ts">
    import TopLeft from './shared/Top_Left.svelte'
    import Circle from './shared/Circle.svelte'
	import HeaderImg1 from '../../static/images/header_1.jpg';
	import HeaderImg2 from '../../static/images/header_2.jpg';
	import HeaderImg3 from '../../static/images/header_3.jpg';
	import HeaderImg4 from '../../static/images/header_4.jpg';

</script>

<style>
    header {
        position: relative;
        padding-top: 8rem;
          /* display: grid; */
          /* justify-content: center; */
          /* align-content: center; */
        height: 80vh }

    h3 {
        text-transform: capitalize;
        font-size: 1.4rem;
        line-height: 1.4; }

    h3.hero-text {
        margin-bottom: 4rem;
        padding-left: 1em;
        border-left: 4px solid var(--accent-color-1);
        max-width: 30rem }

    h3.text {
        font-weight: 300;
        margin-bottom: 0.2em;
        display: inline-block;
        padding-right: 1rem;
    }

    .icon a:hover svg {
        fill: var(--accent-color-1);
    }

    .stores .icon svg {
        width: 1.2rem;
        height: 1.2rem }

    .stores .icon:not(:last-child) {
        margin-right: 1rem }

    .icon  svg path {
        display: inline;
        fill: white }
    
    .content {
        margin-top: 4rem;
        position: relative;
        z-index: 1;
    }

    img {
        width: 100%;
    }
    .wrapper {
        position: relative;

    }

</style>

<header>
    <TopLeft />

    <div class="wrapper">

        <Circle height={16.875} right={-1} top={-6} > 
        <img alt="Success Kid" src="{HeaderImg1}">
    </Circle>

    <Circle height={7.875} right={20} top={-5} > 
        <img alt="Success Kid" src="{HeaderImg2}">
    </Circle>
    
    <Circle height={10} right={15} top={8} > 
        <img alt="Success Kid" src="{HeaderImg3}">
    </Circle>
    
    <Circle height={7.875} right={-1} top={15} > 
        <img alt="Success Kid" src="{HeaderImg4}">
    </Circle> 


        <div class="content">
            <h3 class="hero-text">To you, Who listen to my musice, You save my life and I want to let you. I can not Thank you enought</h3>
            <div class="stores">
               <h3 class="text">Listen on:</h3> 
               <span class="icon">
                    <a href="www.example.com">
                        <svg viewBox="0 0 4.2139001 4.2139401" >
                          <path d="m 2.1069,4.21394 c 1.1631,0 2.107,-0.94392 2.107,-2.10697 C 4.2139,0.94392 3.27,0 2.1069,0 0.9439,0 0,0.94392 0,2.10697 0,3.27002 0.9439,4.21394 2.1069,4.21394 Z M 2.9624,3.10006 v 1.7e-4 c -0.1417,0 -0.5893,-0.49655 -1.8472,-0.2388 -0.033,0.009 -0.076,0.0221 -0.1011,0.0221 -0.1607,0 -0.1914,-0.24037 -0.019,-0.27706 C 1.6909,2.45283 2.402,2.46635 3.0085,2.8291 3.1532,2.9215 3.0915,3.10002 2.9625,3.10002 Z M 3.1911,2.54294 C 3.1711,2.53794 3.1771,2.55504 3.0863,2.50734 2.5552,2.19304 1.7637,2.06628 1.0592,2.25748 c -0.041,0.0111 -0.063,0.0221 -0.1011,0.0221 -0.188,0 -0.2379,-0.28286 -0.033,-0.34062 0.828,-0.23265 1.7163,-0.0969 2.3347,0.27092 0.069,0.0407 0.096,0.0936 0.096,0.16733 -8e-4,0.0917 -0.072,0.16574 -0.1647,0.16574 z M 0.7985,1.22871 C 1.5926,0.99625 2.7945,1.06964 3.5418,1.50578 3.7333,1.61622 3.658,1.89557 3.4548,1.89557 L 3.4547,1.8954 C 3.4107,1.8954 3.3827,1.8843 3.3449,1.8622 2.7404,1.50121 1.6586,1.41465 0.9588,1.61007 c -0.031,0.008 -0.069,0.0219 -0.1098,0.0219 -0.1122,0 -0.1978,-0.0876 -0.1978,-0.20052 0,-0.11535 0.071,-0.18067 0.1478,-0.20279 z" />
                        </svg>
                    </a>
               </span>

               <span class="icon">
                   <a href="www.example.com">
                        <svg viewBox="0 0 188.00301 210.00101" >
                            <path d="M 179.322,90.03 25.786,2.266 C 23.139,0.754 20.192,0 17.245,0 17.185,0 17.126,0.008 17.067,0.008 16.671,0.012 16.276,0.032 15.882,0.063 15.704,0.077 15.527,0.096 15.349,0.116 15.041,0.15 14.734,0.193 14.428,0.244 14.317,0.263 14.205,0.269 14.094,0.29 L 14.1,0.298 C 12.187,0.651 10.32,1.325 8.585,2.332 3.271,5.415 0,11.094 0,17.237 v 175.527 c 0,6.143 3.271,11.822 8.585,14.905 1.734,1.007 3.601,1.682 5.514,2.035 l -0.005,0.007 c 0.1,0.019 0.201,0.025 0.3,0.041 0.329,0.056 0.659,0.102 0.99,0.137 0.166,0.018 0.331,0.036 0.497,0.049 0.389,0.031 0.777,0.049 1.167,0.054 0.066,0.001 0.131,0.009 0.197,0.009 2.947,0 5.894,-0.754 8.541,-2.266 L 179.322,119.97 c 5.368,-3.069 8.681,-8.777 8.681,-14.962 0,0 0,-0.003 0,-0.004 0,0 0,-0.003 0,-0.004 0,0 0,-0.003 0,-0.004 0,0 0,-0.003 0,-0.004 0,-6.184 -3.313,-11.892 -8.681,-14.962 z M 118.604,72.601 103.338,92.628 64.498,41.672 Z m 53.274,34.346 -107.38,61.381 67.234,-88.206 40.145,22.947 c 0.695,0.397 1.127,1.141 1.127,1.938 -0.001,0.8 -0.433,1.544 -1.126,1.94 z" />
                        </svg>
                   </a>
               </span>
               <span class="icon">
                    <a href="www.example.com">
                        <svg viewBox="0 0 419.95499 512">
                            <g transform="translate(-46.022)">
                                <path d="M 185.255,512 C 109.054,511.561 46.022,356.009 46.022,276.79 c 0,-129.404 97.075,-157.734 134.487,-157.734 16.86,0 34.863,6.621 50.742,12.48 11.104,4.087 22.588,8.306 28.975,8.306 3.823,0 12.832,-3.589 20.786,-6.738 16.963,-6.753 38.071,-15.146 62.651,-15.146 0.044,0 0.103,0 0.146,0 18.354,0 74.004,4.028 107.461,54.272 l 7.837,11.777 -11.279,8.511 c -16.113,12.158 -45.513,34.336 -45.513,78.267 0,52.031 33.296,72.041 49.292,81.665 7.061,4.248 14.37,8.628 14.37,18.208 0,6.255 -49.922,140.566 -122.417,140.566 -17.739,0 -30.278,-5.332 -41.338,-10.034 -11.191,-4.761 -20.845,-8.862 -36.797,-8.862 -8.086,0 -18.311,3.823 -29.136,7.881 C 221.496,505.73 204.752,512 185.753,512 Z" />
                                <path d="M 351.343,0 C 353.231,68.076 304.546,115.304 255.918,112.342 247.905,58.015 304.54,0 351.343,0 Z" />
                            </g>
                        </svg>
                    </a>
               </span>
            </div>
        </div>
    </div> 
</header>
