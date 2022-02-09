<script>
    import {italian_nav} from "./it-version/Italian.svelte";
    import {english_nav} from "./en-version/English.svelte";
    import { fade } from 'svelte/transition';

    const [def_nav, lang] = navigator.language.includes("it") ? [italian_nav,"it"] : [english_nav,"en"];
    let page_idx = 0;

    function changePage(i) {
        page_idx = i;
    }

</script>

<svelte:head>
	<title>Lugini Andrea Portfolio</title>
	<meta name="description" content="Lugini Andrea's portfolio"/>
    <meta name="viewport" content="width=device-width, initial-scale=1"/>
	<html lang={lang} />
</svelte:head>

{#key page_idx}
    <main in:fade="{{delay: 500, duration: 500}}" out:fade="{{duration:500}}">
        <h1>{def_nav[page_idx].header}</h1> 
        <svelte:component this={def_nav[page_idx].component}/>

        <ul class="nav-list">
            {#each def_nav as option, i}
                {#if page_idx !== i}
                    <button class="change-page-button" on:click={() => changePage(i)}>{option.title}</button>
                {/if}
            {/each}
        </ul>   
    </main>
{/key}
    <footer>
        <ul>
            <li name="github-logo">
                <a href="https://github.com/LuginiAndrea" target="_blank">
                    <img src="./img/light-github.png" alt="github logo">
                </a>
            </li>
            <li name="remail">Email: lugiolugini@gmail.com</li>
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
    .nav-list {
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
        word-break: break-word;
    }

    main {
        color: #f8f8e8;
        font-family:'Courier New', Courier, monospace;
        margin: 50px auto 0px auto;
        font-size: 1.5em;
        width: 80%;
    }

    h1 {
        font-weight: 500;
        text-align: center;
        font-size: 8.5rem;
        margin: auto;
        transition: ease all .5s;
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
        font-size: 2rem;
        border-top: 2px solid white;
        padding: 10px 0px 0px 0px;
        color: #f8f8e8;
        height: 60px;
    }

    footer ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        transition: ease all .5s;
    }

    footer img {
        width: 50px;
        height: 50px;
        -moz-user-select: none;
        -khtml-user-select: none;
        -webkit-user-select: none;
        -o-user-select: none;
        user-select: none;
    }

    :global(a) {
        text-decoration: none;
        color: skyblue;
        transition: ease all .5s;
    }
    :global(a:link) {
        text-decoration: none;
        color: skyblue;
    }
    :global(a:visited) {
        color: skyblue;
    }
    :global(a:hover) {
        color: blue;
    }

    @media(max-width: 550px) and (min-width: 500px) {
        h1 {
            font-size: 6.5rem;
        }
        :global(p) {
            width: 70%;
        }
        main {
            font-size: 1em;
            width: 95%;
        }
    }

    @media(max-width: 500px) {
        h1 {
            font-size: 5.5rem;
        }
        main {
            font-size: 1em;
            width: 95%;
        }
        footer {
            font-size: 1.2rem;
            height: 50px;
        }
        footer img {
            width: 30px;
            height: 30px;
        }
    }


</style>