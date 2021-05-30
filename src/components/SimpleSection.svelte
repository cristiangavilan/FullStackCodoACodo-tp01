<script>
export let title = ''
export let subtitle = ''
export let image = ''
</script>

<div>
    <div class="p-4 animate__animated animate__fadeIn">
        <div class="row">
            <div class="col">
                <h1>{title}</h1>
                <p>{subtitle}</p>
            </div>
        </div>
        <div class="row">
            <div class="col align-center">
                <img class="rounded mx-auto d-block w-75" src="{image}" alt="{image}" style="z-index:-1">
            </div>
        </div>
    </div>
</div>
