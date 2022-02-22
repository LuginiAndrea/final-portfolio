<script>
    let page_to_view = 0;
</script>

{#if page_to_view === 0}
<div id="neki" class="outer-ul">
    <a href="https://neki.it/" target="_blank"><h1>Neki S.R.L.</h1></a>
    <h2>Saragozza, Spagna: 10/05/2021 - 25/05/2021</h2>
    <div class="card" name="products">
        <img src="./img/nek.png" style="float:right" alt="Neki logo"/> 
        L'azienda, composta da 12 dipendenti, si occupa della realizzazione e vendita di GPS mirati per 
        persone con difficoltà motorie/cognitive, con relativo servizio web, presente
        anche come app mobile.
    </div>
    <div class="card" name="products">
        Durante il mio periodo l'azienda non ha avuto particolari lavori da farmi fare ad
        eccezzione dell'attività di rimozione e disattivazione delle SIM di prodotti 
        difettosi. <br>
        Quindi, Con l'obiettivo di trarre il meglio da questa esperienza, ho sfruttato la maggior parte del tempo
        osservando il lavoro del programmatore dell'azienda e discutendo con lui delle sue attività.
    </div>
    <ul class="outer-ul">
        <li>
            Orario:
            <ul name="Orario:">
                <li>90 ore di lavoro</li>
                <li>Orario: 10:00-16:00</li>
                <li>Weekend libero</li>
            </ul>
        </li>
        <li>
            Obiettivo:
            <ul name="Obiettivo:">
                <li>Acquisizione competenze</li>
            </ul>
        </li>
        <li>
            Tutor:
            <ul name="Tutoraggio:">
                <li>Assenza di un tutor designato</li>
                <li>Il programmatore aziendale, Pablo, ha svolto nei miei confronti un ruolo simile</li>
            </ul>
        </li>
        <li>
            Competenze acquisite:
            <ul name="Competenze acquisite">
                <li>NodeJS</li>
                <li>Typescript</li>
                <li>React</li>
                <li>Progrmmazione Web Server</li>
            </ul>
        </li>
    </ul>
</div>
{:else}
    <ul id="ammagamma">
        <li>
            <h1>Ammagamma S.R.L.</h1>
            <h2>Saragozza, Spagna: 10/05/2021 - 25/05/2021</h2>
            <div class="card" name="products">
                <img src="./img/nek.png" style="float:right" alt="Neki logo"/> 
                L'azienda, composta da 12 dipendenti, si occupa della realizzazione e vendita di GPS mirati per 
                persone con difficoltà motorie/cognitive, con relativo servizio web, presente
                anche come app mobile.
            </div>
            <div class="card" name="products">
                Durante il mio periodo l'azienda non ha avuto particolari lavori da farmi fare ad
                eccezzione dell'attività di rimozione e disattivazione delle SIM di prodotti 
                difettosi. <br>
                Con l'obiettivo di sfruttare al massimo la mia permanenza, ho sfruttato la maggior parte del tempo
                osservando il lavoro del programmatore dell'azienda e discutendo con lui delle sue attività.
            </div>
            <ul>
                <li>
                    Orario:
                    <ul name="Orario:">
                        <li>90 ore di lavoro</li>
                        <li>Orario: 10:00-16:00</li>
                        <li>Weekend libero</li>
                    </ul>
                </li>
                <li>
                    Obiettivo:
                    <ul name="Obiettivo:">
                        <li>Acquisizione competenze</li>
                    </ul>
                </li>
                <li>
                    Tutor:
                    <ul name="Tutoraggio:">
                        <li>Assenza di un tutor designato</li>
                        <li>Il programmatore aziendale, Pablo, ha svolto nei miei confronti un ruolo simile</li>
                    </ul>
                </li>
                <li>
                    Competenze acquisite:
                    <ul name="Competenze acquisite">
                        <li>NodeJS</li>
                        <li>Typescript</li>
                        <li>React</li>
                        <li>Progrmmazione Web Server</li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
{/if}



    
<style>
    img{
        height: 150px;
        width: 150px;
    }
    .outer-ul {
        margin-top: 20px;
    }
    .outer-ul>li {
        padding: 20px;
    }
    img {
        margin-left: 10px;
    }
</style>