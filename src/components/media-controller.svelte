<script>

    export let isPlaying
    
    console.log(isPlaying)

</script>

<style type="text/css" media="screen">
    svg {
        width: 4rem;
        height: 4rem;
        cursor: pointer;
    }

    svg ellipse {
        display: inline;
        fill: none;
        stroke: orangered;
        stroke-width: 6;
        stroke-miterlimit: 4;
        stroke-opacity: .8;

    }

    svg path.play {
        fill: orangered;
        fill-opacity: 0;
    }
    
    /* svg g.pause { */
    /* } */

    svg g.pause path {
        fill: none;
        display: none;
        stroke: orangered;
        stroke-width: 6;
        stroke-linecap: round;

    }

    svg path.show {
        fill-opacity: 1 !important;
        display: inline;
    }
    svg g.show path {
        display: inline;
    }
    
</style>


<svg
   xmlns="http://www.w3.org/2000/svg"
   viewBox="0 0 135 134.99999"
   version="1.1"
   id="svg8">
  <defs
     id="defs2">
</defs>

  <ellipse
     id="path1612"
     cx="-67.499992"
     cy="67.5"
     rx="61.500046"
     ry="61.50005"
     transform="rotate(-90)" />
  <g
      class="pause"
    class:show="{isPlaying === true}"
     transform="translate(-0.17777825,-0.18127833)">
    <path
       d="M 51.271205,42.984758 V 92.552532"
       id="path1673" />
    <path
      class="pause"
       d="M 84.08435,42.810016 V 92.37779"
       id="path1673-6" />
  </g>

  <path
    class:show="{isPlaying == false}"
      class="play"
     transform="translate(5,0)"
     d="m 86.259187,63.361495 -31.584,-22.646 c -3.369,-2.416 -8.059,-0.008 -8.059,4.138 v 45.293 c 0,4.146 4.69,6.554 8.059,4.138 l 31.583,-22.647 c 2.834,-2.031 2.834,-6.244 10e-4,-8.276 z" />

  <ellipse
     id="path1612-7"
     cx="-67.499992"
     cy="67.5"
     rx="61.500046"
     ry="61.50005"
     transform="rotate(-90)" />
</svg>
