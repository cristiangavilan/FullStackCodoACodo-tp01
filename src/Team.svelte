<script>
import Capabilities from "./Capabilities.svelte";
import Election from "./Election.svelte";
import Subscribe from "./Subscribe.svelte";

    const team = [
        {name:'Jhoana Cash', position:'Business Analyst', image:'build/img/team/team-01.jpg'},
        {name:'Sophie Graff', position:'UX/UI Analyst', image:'build/img/team/team-02.jpg'},
        {name:'Manolo Pantallas', position:'Frontend Developer', image:'build/img/team/team-03.jpg'},
        {name:'Dante Datillos', position:'Backend Developer', image:'build/img/team/team-04.jpg'},
    ];
</script>
<div class="bg-secondary animate__animated animate__fadeIn">
    <div class="p-4">
        <div class="row">
            <div class="col">
                <h1>Equipo</h1>
                <p>Profesionales dedicados a realizar productos y servicios de calidad</p>
            </div>
        </div>
        <div class="row text-center">
            {#each team as {name, position, image}}
            <div class="col-lg-6">
                <img class="img-fluid rounded" src="{image}" alt="{image}">
                <h3 class="mt-2" >{name}</h3>
                <p>{position}</p>
            </div>
            
            {/each}
        </div>
    </div>
</div>
<Election />
<Capabilities />
<Subscribe />