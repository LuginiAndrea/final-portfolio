<script>
    import {italian_nav} from "./it-version/Italian.svelte";
    import {english_nav} from "./en-version/English.svelte";
    
    const def_nav = navigator.language.includes("it") ? italian_nav : english_nav;
    let page_idx = 0;

    function changePage(i) {
        page_idx = i;
    }

</script>

<main>
    {#if page_idx == 0}
        <h1>Andrea Lugini</h1> 
        <svelte:component this={def_nav[0].component}/>
    {:else}
        <h1>Ciaoooo</h1>
    {/if}

    <ul class="navigation-ul">
        {#each def_nav as option, i}
            {#if page_idx !== i}
                <button class="change-page-button" on:click={() => changePage(i)}>{option.title}</button>
            {/if}
        {/each}
    </ul>    
</main>

<style>
    .change-page-button {
        margin: 10px;
        padding: 10px;
        border: 1px solid black;
        border-radius: 5px;
        background-color: #f0f0f0;
    }
    .navigation-ul {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        width: 20%;
        margin: auto;
    }
</style>