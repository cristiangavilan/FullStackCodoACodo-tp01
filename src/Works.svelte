<script>
import Card from "./components/Card.svelte";
import Footer from "./components/Footer.svelte";

const cards = [{
        title: 'Social Media',
        subtitle: 'Ullamco laboris nisi ut aliquip ex',
        image: 'build/img/works/recent-work-01.jpg'
    },
    {
        title: 'Web Marketing',
        subtitle: 'Psum officia anim id est laborum.',
        image: 'build/img/works/recent-work-02.jpg'
    },
    {
        title: 'Posicionamiento',
        subtitle: 'Sum dolor sit consencutur',
        image: 'build/img/works/recent-work-03.jpg'
    },
    {
        title: 'Estudio de Mercado',
        subtitle: 'Lorem ipsum dolor sit amet',
        image: 'build/img/works/recent-work-04.jpg'
    },
    {
        title: 'Desarrollo de Marca',
        subtitle: 'Put enim ad minim veniam',
        image: 'build/img/works/recent-work-05.jpg'
    },
    {
        title: 'Diseño Creativo',
        subtitle: 'Mollit anim id est laborum.',
        image: 'build/img/works/recent-work-06.jpg'
    },
];
</script>
<div class="bg-tertiary animate__animated animate__fadeIn">
    <div class="p-4">
        <h1 class="text-light">Nuestros Trabajos</h1>
        <p class="text-light">Transformá tu forma de vender</p>
        <div class="row row-cols-md-3 row-cols-sm-2 row-cols-1 m-2">
            {#each cards as {title,subtitle,image}}
            <div class="col mb-4">
                <Card title={title} description={subtitle} image={image} />
            </div>
            {/each}
        </div>
    </div>
</div>

<Footer />
