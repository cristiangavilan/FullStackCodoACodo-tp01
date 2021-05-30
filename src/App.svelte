<script>
	import { Router, Route } from 'svelte-routing';
	
	import Navbar from './Navbar.svelte';
	import Home from './Home.svelte';
	import Services from './Services.svelte';
	import Works from './Works.svelte';
	import About from './About.svelte';
	import Team from './Team.svelte';
	import Election from './Election.svelte';
	import Capabilities from './Capabilities.svelte';
	import Subscribe from './Subscribe.svelte';
	import Contact from './Contact.svelte';

</script>

<Router>
	<Navbar />
	  
	<div>
		<Route path="/"> <Home /> </Route>  
		<Route path="home"> <Home /> </Route>  
		<Route path="services"> <Services /> </Route>
		<Route path="works"> <Works /> </Route>
		<Route path="about"> <About/> </Route>  
		<Route path="team"> <Team /> </Route>
		<Route path="election"> <Election /> </Route>
		<Route path="capabilities"> <Capabilities /> </Route>
		<Route path="subscribe"> <Subscribe /> </Route>
		<Route path="contact"> <Contact/> </Route> 
		<Route path="**"> <Home /> </Route>
	</div>
	
</Router>