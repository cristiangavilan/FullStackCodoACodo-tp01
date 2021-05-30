<script>
import { link } from 'svelte-routing';
let linkNetworks = ['facebook', 'linkedin', 'whatsapp', 'flickr', 'medium'];
let sections = [
    {id:'Inicio', url:'home'},
    {id:'Servicios', url:'services'},
    {id:'Trabajos', url:'works'},
    {id:'Nosotros', url:'about'},
    // {id:'Equipo', url:'team'},
    // {id:'¿Porqué Elegirnos?', url:'election'},
    // {id:'Capacidades', url:'capabilities'},
    // {id:'Suscribirte', url:'subscribe'},
    {id:'Contacto', url:'contact'},
];
let date = new Date();
</script>

<div class="bg-five animate__animated animate__fadeIn">
    <div class="p-4">

        <div class="row">
            <div class="col-lg-4">
                <a class="navbar-brand" href="home" use:link>
                    <img src="build/img/tengo-logo.svg" alt="logo">
                </a>
                <p class="text-light">Buscanos en nuestras redes sociales:</p>
                <ul class="list-inline">
                    {#each linkNetworks as ln}
                    <li class="list-inline-item m-0">
                        <a class="text-light" target="_blank" href="http://{ln}.com/">
                            <i class='bx bxl-{ln}-square bx-md text-light'></i>
                        </a>
                    </li>
                    {/each}
                </ul>
            </div>
            <div class="col-lg-4">
                <h3 class="text-light">Secciones</h3>
                <ul class="list-inline">
                    {#each sections as {id,url}}
                    <div class="row">
                        <div class="col">
                            <li class="list-inline-item m-0">
                                <a href="{url}" style="text-decoration:none" use:link>
                                    <p class="text-light">{id}</p>
                                </a>
                            </li>
                        </div>
                    </div>
                    {/each}
                </ul>
            </div>
            <div class="col-lg-4">
                <h3 class="text-light">Esperamos tu consulta en:</h3>
                <ul class="list-inline">
                    <div class="row">
                        <div class="col">
                            <li class="list-inline-item m-0 text-light">
                                <i class='bx-fw bx bx-phone'></i> 299-4517-438
                            </li>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <li class="list-inline-item m-0 text-light">
                                <i class='bx-fw bx bx-mail-send'></i> info@tengo.com.ar
                            </li>
                        </div>
                    </div>
                </ul>
            </div>
        </div>
    </div>
    <div class="card-footer">
       Tengo © Copyright {date.getFullYear()}. Todos los derechos reservados (Cristian Gavilan).
       Trabajo para el curso FullStack Web, del programa Codo a Codo.
    </div>
</div>
