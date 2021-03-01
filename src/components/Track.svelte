
<style>
    .track {
        display: grid;
        grid-template-columns: 4.66rem 1rem 2fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        grid-column-gap: 1rem;

        min-height: 8rem;
        padding: 1rem 2rem;
        border-radius: 10px;
        background: var(--bg-color-2) }
        
    .track-image {
        grid-column: 1 / 2;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;

        display: grid;
        justify-content: center;
        align-content: center;

        width: 5.25rem;
        height: 5.25rem;
        border-radius: 15px;
        background: var(--bg-color-1) }

    .media-controller{
        grid-column: 4 / -1;
        grid-row: 1 / -1;
        align-self: center;
        justify-self: right;

        display: grid;
        justify-content: center;
        align-content: center;

        border-radius: 50%;
        width: 4rem;
        height: 4rem;
        background: var(--bg-color-1) }
    
    .artist-name, .track-name {
        padding: 0;
        margin: 0;
        opacity: .8;
        background-color: var(--bg-color-1);
        align-self: center;
        grid-column: 2 / span 2; }

    .track-name {
        /* align-self: center; */
        /* justify-self: right */ }

    .artist-name {
        /* align-self: center; */
        /* align-items: bottom; */
        
       }

    .icon {
        height: 1.5rem;
        width: 1.5rem;
        background-color: var(--bg-color-1);
        border-radius: 50%;
    }

</style>

<div class="track">
    <div class="track-image"></div>

    <h3 class="artist-name">&nbsp;</h3>
    <h3 class="track-name">&nbsp;</h3>

    <span class="icon"></span>
    <span class="icon"></span>

    <div class="media-controller"></div>

</div>
