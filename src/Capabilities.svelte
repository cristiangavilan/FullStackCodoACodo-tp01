<script>
    const capabilities = [
        {name:'Desarrollo Frontend', value: 98},
        {name:'Desarrollo Backend', value: 99},
        {name:'Diseño UX/UI', value: 97},
        {name:'Marketing', value: 98},
        {name:'Creatividad', value: 96},
    ];
</script>
<div class="bg-tertiary animate__animated animate__fadeIn">
    <div class="p-4">
        <div class="row">
            <div class="col">
                <h1 class="text-light">Capacidades</h1>
                <p class="text-light">Medimos nuestras fortalezas</p>
            </div>
        </div>
        <div class="row">
            <div class="col-lg-6">
                <img class="img-fluid" src="build/img/tengo-work_together.svg" alt="build/img/tengo-work_together.svg">
            </div>
            <div class="col-lg-6">
                {#each capabilities as {name, value}}
                    <h5 class="mt-2 text-light" >{name} {value}%</h5>
                     <div class="progress">
                        <div class="progress-bar bg-secondary" role="progressbar" style="width: {value}%" aria-valuenow="{value}" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</div>