<script>
	import Navbar from '../$lib/components/Navbar.svelte';
	import Accueil from '../$lib/components/Accueil.svelte';
	import Pastille from '../$lib/components/Pastille.svelte';
	import Services from '../$lib/components/Services.svelte';
	import Banner from '../$lib/components/Banner.svelte';
	import Pricing from '../$lib/components/Pricing.svelte';
	import Testimonials from '../$lib/components/Testimonials.svelte';
	import Contact from '../$lib/components/Contact.svelte';
</script>

<section>
	<Navbar />
	<Accueil />
	<Pastille />
</section>

<Services />

<Banner />

<Pricing />

<Testimonials />

<Contact />

<style>
	section {
		background: url('../$lib/assets/stylish-mesh-bg.jpg') no-repeat;
		background-size: cover;
		position: relative;
	}
</style>
