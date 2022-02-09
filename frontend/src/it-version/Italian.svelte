<script context="module">
    import home_page from "./home_page.svelte";
    import educazione from "./educazione.svelte";
    export const italian_nav = [
        { title: "Home Page", component: home_page, header: "Andrea Lugini" },
        { title: "Educazione", component:educazione, header: "Educazione" },
        { title: "prova3" },
        { title: "prova4" }
    ];       
</script>