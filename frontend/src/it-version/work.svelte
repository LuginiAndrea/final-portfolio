<script>
    import neki from "./work-exp/neki.svelte";
    import ammagamma from "./work-exp/ammagamma.svelte";
    let page_idx = 0;
    const max_page = 1;
    const work_exp_nav = [neki, ammagamma];


</script>

<div>
    <!-- Button to navigate work pages -->
    {#if page_idx > 0}
        <button class="change-pg-button left" on:click={() => {page_idx -= 1;}}/>
    {/if}
    {#if page_idx < max_page}
        <button class="change-pg-button right" on:click={() => {page_idx += 1;}}/>
    {/if}
    <!-- End button -->
    {#key page_idx} 
        <svelte:component this={work_exp_nav[page_idx]}/> 
    {/key}
</div>



    
<style>
    div {
        position: relative;
    }
    .change-pg-button {
        position: absolute;
        top: 0;
        right: 10px;
        display: inline-block;
        width: 90px;
        height: 90px;
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        border-radius: 50%;
        text-decoration: none;
        font-size: 16px;
        cursor: pointer;
    }
    .right {
        background-image: url("right-arrow.png");
    }
    .left {
        background-image: url("left-arrow.png");
    }

    @media(max-width: 550px) {
        .change-pg-button {
            width: 50px;
            height: 50px;
        }
    }
</style>