<script>
    import { fly } from 'svelte/transition';
    let programming = true;
</script>

<div>
<ul class="skills-list" transition:fly="{{ x: -300, duration: 2000 }}">
    <li>
        <a href="./misc/lugini_andrea_statement_of_results.pdf" target="_blank">CAE Certification</a> :english language
    </li>
    <li>
        <img src="./img/cambridge.png" alt="Cambridge certification center" style="width:110px; height:110px">
    </li>
    <li>
        Backend development with <a href="https://nodejs.org/en/">NodeJS</a>, <a href="https://expressjs.com/en/">Express</a>,
        and <a href="https://www.typescriptlang.org/">Typescript</a>
    </li>
    <li>
        <img src="./img/typescript.png" alt="Typescript" style="height:100px;width:100px"> 
    </li>
    <li>
        Software development in <a href="https://www.cplusplus.com/">C++</a> with GUI made with <a href="https://www.qt.io/">QT</a>
    </li>
    <li>
        <img src="./img/qt.png" alt="Qt" style="height:100px;width:140px">
    </li>
    <li>
        Software development in <a href="https://www.java.com/en/">Java</a>
    </li>
    <li>
        <img src="./img/java.png" alt="Java" style="height:110px;width:170px">
    </li>
    <li>
        Frontend development with
            <a href="https://en.reactjs.org/">React</a>,
            <a href="https://svelte.dev/">Svelte</a>,
            <a href="https://tailwindcss.com/">TailwindCSS</a> and the programming languages
            <a href="https://www.javascript.com/">Javascript</a> and
            <a href="https://www.typescriptlang.org/">Typescript</a>. 
    </li>
    <li>
        <img src="./img/react.png" alt="React" style="height:130px;width:140px"> 
    </li>
    <li>
        Design and e implementation of Databases with <a href="https://www.mysql.com/en/">SQL</a>
    </li>
    <li>
        <img src="./img/sql.png" alt="SQL" style="height:130px;width:130px">
    </li>
</ul>
</div>

<style>
    ul {
        display: flex;
        flex-direction: column;
        /* flex-wrap: wrap; */
        align-items: center;
        list-style-type: none;
        text-align: center;
        margin: 0;
        padding: 0;
    }
    li {
        padding-top:20px;
        padding-bottom: 20px;
    }
</style>