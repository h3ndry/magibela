<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Hero from '$lib/Hero/Hero.svelte';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<Hero />



<section class="about" >

<h3>About My Life</h3>

<p> 
Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempo  r incididunt ut labore et dolore magna 
aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
</p>


<svg
   width="25.998896mm"
   height="102.13882mm"
   viewBox="0 0 25.998896 102.13882" >
  <defs
     id="defs12693">
    <clipPath
       clipPathUnits="userSpaceOnUse"
       id="clipPath1127">
      <rect
         style="opacity:1;fill:#c7392b;fill-opacity:1;stroke:none;stroke-width:124.809;stroke-linecap:round;stroke-miterlimit:4;stroke-dasharray:none"
         id="rect1129"
         width="338.05606"
         height="373.4552"
         x="64.648865"
         y="593.11981"
         rx="50"
         transform="rotate(23.770308)" />
    </clipPath>
    <linearGradient
       xlink:href="#linearGradient1102"
       id="linearGradient1104-6"
       x1="470.89432"
       y1="329.16437"
       x2="527.22162"
       y2="295.93527"
       gradientUnits="userSpaceOnUse"
       gradientTransform="matrix(0.25389197,0,0,0.25389197,-16.087676,-4.5711028)" />
    <linearGradient
       id="linearGradient1102">
      <stop
         style="stop-color:#ffffff;stop-opacity:1;"
         offset="0"
         id="stop1098" />
      <stop
         style="stop-color:#ffffff;stop-opacity:0;"
         offset="1"
         id="stop1100" />
    </linearGradient>
    <clipPath
       clipPathUnits="userSpaceOnUse"
       id="clipPath1127-3">
      <rect
         style="opacity:1;fill:#c7392b;fill-opacity:1;stroke:none;stroke-width:124.809;stroke-linecap:round;stroke-miterlimit:4;stroke-dasharray:none"
         id="rect1129-6"
         width="338.05606"
         height="373.4552"
         x="64.648865"
         y="593.11981"
         rx="50"
         transform="rotate(23.770308)" />
    </clipPath>
  </defs>
  <g
     id="layer1"
     transform="translate(-94.678718,-59.775235)">
    <rect
       style="fill:#c7392b;fill-opacity:1;stroke-width:1.09653"
       id="rect44-6-5-7"
       width="1023.4562"
       height="1451.7836"
       x="0"
       y="0"
       clip-path="url(#clipPath1127-3)"
       transform="matrix(0.22886234,0,0,0.22886234,94.678718,-74.048735)" />
    <circle
       style="opacity:0.463925;fill:url(#linearGradient1104-6);fill-opacity:1;stroke:none;stroke-width:5.49259;stroke-linecap:round;stroke-miterlimit:4;stroke-dasharray:none"
       id="path963-3-6-7-1"
       cx="109.26974"
       cy="73.675461"
       r="12.437258" />
  </g>
</svg>


</section>

<style  lang="scss">
    @use "src/styles/pages/home";
</style>
