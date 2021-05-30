<script>
    import { link } from 'svelte-routing';
</script>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  		<a class="navbar-brand" href="/" use:link >
			<img src="build/img/tengo-logo.svg"  width="30%" alt="">
            <!-- {name} -->
		</a>
		<button class="navbar-toggler" 
				type="button" 
				data-toggle="collapse" 
				data-target="#navbarSupportedContent" 
				aria-controls="navbarSupportedContent" 
				aria-expanded="false" 
				aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		</button>

		<div class="collapse navbar-collapse" id="navbarSupportedContent">
			<ul class="navbar-nav mr-auto">
			<li class="nav-item col">
                <a class="nav-link" 
                    href="/" use:link>Inicio
				</a>
			</li>
			<li class="nav-item col">
                <a class="nav-link" 
                    href="services" use:link>Servicios
				</a>
			</li>
			<li class="nav-item col">
                <a class="nav-link" 
                    href="works" use:link>Trabajos
				</a>
			</li>
			<li class="nav-item col">
				<a class="nav-link" 
					href="about" use:link >Nosotros
				</a>
			</li>

			<li class="nav-item col">
				<a class="nav-link" 
					href="contact" use:link>Contacto
				</a>
			</li>
			</ul>
			<form class="form-inline my-2 my-lg-0">
			<input class="form-control mr-sm-2" type="search" placeholder="..." aria-label="Search">
			<button class="btn btn-outline-success my-2 my-sm-0" type="submit">Buscar</button>
			</form>
		</div>
	</nav>