<script>

    export let height;
    export let left;
    export let top;
    export let right;
</script>

<style>

    .circle {
        background-color: red;
        border-radius: 50%;
        overflow: hidden;
        position: absolute;
    }


    
</style>


<div class="circle" 
     style="
        top: {top}rem;
        right: {right}rem;
        height: {height}rem;
        width: {height}rem;" >
    <slot></slot>
</div>
