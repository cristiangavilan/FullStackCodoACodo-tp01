<script>
	import { link } from 'svelte-routing';
    import Footer from "./components/Footer.svelte";
    import SimpleSection from "./components/SimpleSection.svelte";
</script>

<SimpleSection 
    title="Contacto" 
    subtitle="Somos tu mejor opción para tu negocio" 
    image="build/img/tengo-on_the_office.svg" />

<div class="bg-secondary animate__animated animate__fadeIn">
    <div class="p-4">
        <div class="row">
            <div class="col">
                <h1>Escribinos:</h1>
            </div>
        </div>    
        <div class="row">
            <div class="col">
                <form class="row" method="get" action="/" role="form">

                    <div class="col-lg-6 mb-4">
                        <div class="form-floating">
                            <label for="floatingname">Nombre</label>
                            <input type="text" class="form-control form-control-lg" id="floatingname" name="inputname" placeholder="name">
                        </div>
                    </div><!-- End Input Name -->

                    <div class="col-lg-6 mb-4">
                        <div class="form-floating">
                            <label for="floatingemail">Correo Electrónico</label>
                            <input type="email" class="form-control form-control-lg" id="floatingemail" name="inputemail" placeholder="e-mail">
                        </div>
                    </div><!-- End Input Email -->

                    <div class="col-lg-6 mb-4">
                        <div class="form-floating">
                            <label for="floatingphone ">Teléfono</label>
                            <input type="number" class="form-control form-control-lg" id="floatingphone" name="inputphone" placeholder="phone">
                        </div>
                    </div><!-- End Input Phone -->

                    <div class="col-lg-6 mb-4">
                        <div class="form-floating">
                            <label for="floatingcompany">Empresa</label>
                            <input type="text" class="form-control form-control-lg" id="floatingcompany" name="inputcompany" placeholder="company">
                        </div>
                    </div><!-- End Input Company Name -->

                    <div class="col-12">
                        <div class="form-floating mb-4">
                            <label for="floatingsubject">Asunto</label>
                            <input type="text" class="form-control form-control-lg" id="floatingsubject" name="inputsubject" placeholder="subject">
                        </div>
                    </div><!-- End Input Subject -->

                    <div class="col-12">
                        <div class="form-floating mb-3">
                            <label for="floatingtextarea">Mensaje</label>
                            <textarea class="form-control" rows="8" placeholder="message" id="floatingtextarea"></textarea>
                        </div>
                    </div><!-- End Textarea Message -->

                    <div class="col-md-12 col-12 m-auto text-end">
                        <a class="btn btn-outline-primary px-md-5 px-4 py-2" href="contact" use:link>Enviar Mensaje</a>
                    </div>

                </form>
            </div>
        </div>
    </div>
</div>

<Footer />