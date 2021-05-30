<script>
import Card from "./components/Card.svelte";
import Footer from "./components/Footer.svelte";

const categoryServices = [{
        id: 'project',
        name: 'Projects'
    },
    {
        id: 'graphic',
        name: 'Gráfica'
    },
    {
        id: 'ui',
        name: 'UX/UI'
    },
    {
        id: 'branding',
        name: 'Branding'
    }
];
const cards = [{
        title: 'UI/UX diseño',
        subtitle: 'Lorem ipsum dolor sit amet, consectetur',
        categories: ['project', 'ui', 'branding'],
        image: 'build/img/services/services-01.jpg'
    },
    {
        title: 'Redes Sociales',
        subtitle: 'Ipsum aspernatur et porro mollitia sit eos quia',
        categories: ['project', 'ui', 'graphic'],
        image: 'build/img/services/services-02.jpg'
    },
    {
        title: 'Marketing',
        subtitle: 'officia fugiat qui sint optio obcaecati sapiente',
        categories: ['project', 'ui', 'branding'],
        image: 'build/img/services/services-03.jpg'
    },
    {
        title: 'Gráfica',
        subtitle: 'Lorem ipsum dolor sit amet consectetur adipisicing',
        categories: ['project', 'ui', 'graphic'],
        image: 'build/img/services/services-04.jpg'
    },
    {
        title: 'Marketing Digital',
        subtitle: 'Lorem ipsum dolor sit amet consectetur adipisicing',
        categories: ['project', 'ui', 'graphic'],
        image: 'build/img/services/services-05.jpg'
    },
    {
        title: 'Branding',
        subtitle: 'officia fugiat qui sint optio obcaecati sapiente',
        categories: ['project', 'ui', 'branding'],
        image: 'build/img/services/services-06.jpg'
    },
    {
        title: 'Negocios',
        subtitle: 'Ipsum aspernatur et porro mollitia sit eos quiasgy',
        categories: ['project', 'ui', 'branding'],
        image: 'build/img/services/services-07.jpg'
    },
    {
        title: 'Branding',
        subtitle: 'officia fugiat qui sint optio obcaecati sapiente',
        categories: ['project', 'ui', 'branding'],
        image: 'build/img/services/services-08.jpg'
    },
];

let cardsFilter = cards;

const lookUpCategories = (categories) => {
    let cattt = [];
    categories.map(category => {
        let aCat = categoryServices.find(fullCategory => fullCategory.id === category)
        cattt.push(aCat.name)
    })
    return cattt;
}

const filterCategory = (filter) => {
    let cardsFilters = [];
    cards.map(card => {
        if (card.categories.find(element => element === filter)) {
            cardsFilters.push(card);
        }
    });
    cardsFilter = cardsFilters;
}
</script>

<div class="bg-secondary animate__animated animate__fadeIn">
    <div class= "p-4">
        <h1 class="text-dark">Servicios</h1>
        <p>Hacemos que el futuro sea hoy</p>
        <div class="row">
            <div class="col">
                <ul class="nav nav-pills mb-3" role="tablist">
                    {#each categoryServices as { id, name }, index }
                    <li class="nav-item col m-1 animate__animated animate__fadeIn" role="presentation">
                        <button class="nav-link col mx-2 btn-outline-primary {index === 0 ? 'active' : ''}" on:click={() => filterCategory(id)} data-toggle="tab" role="tab" aria-controls="{name}" aria-selected="true">{name}</button>
                    </li>
                    {/each}
                </ul>
            </div>
        </div>
        <div class="row row-cols-lg-4 row-cols-md-3 row-cols-sm-2 row-cols-1 m-2">
            {#each cardsFilter as {title,subtitle,image, categories}}
            <div class="col mb-4 text-center animate__animated animate__fadeIn">
                <Card title={title} description={subtitle} image={image} pills={lookUpCategories(categories)} />
            </div>
            {/each}
        </div>
    </div>
</div>

<Footer />
