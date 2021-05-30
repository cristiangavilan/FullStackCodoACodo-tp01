<script>
import { link } from 'svelte-routing';
let msgs = [{
        title: 'Estrategias para tu negocio',
        subtitle: 'Tenemos una gran variedad de lineas de servicios para tu negocio',
        linked:'services'
    },
    {
        title: 'Fuerte presencia en redes sociales',
        subtitle: 'Éstos son algunos casos de éxito',
        linked:'works'
    },
    {
        title: 'Compromiso de equipo',
        subtitle: 'Un grupo de profesionales dedicados a dar soluciones tecnológicas',
        linked:'about'
    }
];
</script>

<div id="carouselHome" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
        <li data-target="#carouselHome" data-slide-to="0" class="active"></li>
        <li data-target="#carouselHome" data-slide-to="1"></li>
        <li data-target="#carouselHome" data-slide-to="2" ></li>
    </ol>

    <div class="carousel-inner animate__animated animate__fadeIn">
        <img class="rounded mx-auto d-block fixed-bottom w-75 mb-2" src="build/img/tengo-developer_activity.svg" alt="...">
        {#each msgs as {title,subtitle, linked}, index}
        <div class= { index === 0 ? 'carousel-item active' : 'carousel-item'}>
            <div class="row  d-flex justify-content-center">
                <div class="col m-4 p-4">
                    <h1 class="panel-title">{title}</h1>
                    <p>{subtitle}</p>
                    <a class="btn btn-outline-primary btn-lg py-4" href="/{linked}" use:link role="button">Ver mas..</a>
                </div>
            </div>
        </div>
        {/each}
    </div>
    <!-- <a class="carousel-control-prev text-decoration-none" href="#carouselHome" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next text-decoration-none" href="#carouselHome" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a> -->
</div>
