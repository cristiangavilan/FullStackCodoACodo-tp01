<script>
export let title = '';
export let description = '';
export let image = '';
export let pills = [];
</script>

<div class="card animate__animated animate__fadeIn">
    <img src="{image}" class="card-img-top" alt="{image}">
    <div class="card-body">
        <h5 class="card-title">{title}</h5>
        <p class="card-text tertiary" >{description}</p>
        {#each pills as pill}
        <span class="badge badge-pill bg-tertiary mx-1 p-1">{pill}</span>
        {/each}
    </div>
</div>
