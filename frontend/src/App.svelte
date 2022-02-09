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
    <footer>
        <ul>
            <li><img src="./img/light-github.png" alt="github logo"></li>
            <li><img src="./img/light-github.png" alt="github logo"></li>
            <li><img src="./img/light-github.png" alt="github logo"></li>
        </ul>
    </footer> 

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

    :global(html) {
        background-color: #222222;
    }

    :global(body) {
        margin: 0;
        padding: 0;
        display:flex; 
        flex-direction:column; 
    }

    main {
        color: #f8f8e8;
        font-family:'Courier New', Courier, monospace;
        margin: 50px 10px 0px 10px;
    }

    h1 {
        font-weight: 500;
        text-align: center;
        font-size: 8.5em;
        margin: auto;
        transition: ease all .5s;
    }

    @media(max-width: 550px) and (min-width: 500px) {
        h1 {
            font-size: 6.5em;
        }
        :global(p) {
            width: 70%;
        }
    }

    @media(max-width: 500px) {
        h1 {
            font-size: 5.5em;
        }
    }

    :global(p) {
        width: 80%;
        margin: auto;
        transition: ease all .5s;
    }

    footer {
        margin-top:auto; 
        background-color: black;
        width: 100%;
        text-align: center;
        font-size: 2em;
        border-top: 2px solid white;
    }

    footer ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
    }

    footer {
        padding: 8px 0px 0px 0px;
    }
    footer img {
        width: 50px;
        height: 50px;
    }

</style>