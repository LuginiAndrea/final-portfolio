<script context="module">
    import home_page from "./home_page.svelte";
    import educazione from "./educazione.svelte";
    import skills from "./skills.svelte";
    import work from "./work.svelte";
    export const italian_nav = [
        { title: "Home Page", component: home_page, header: "Andrea Lugini" },
        { title: "Studi", component:educazione, header: "Studi" },
        { title: "Skills", component: skills, header: "Skills" },
        { title: "Lavoro", component: work, header: "Lavoro"}
    ];       
</script>