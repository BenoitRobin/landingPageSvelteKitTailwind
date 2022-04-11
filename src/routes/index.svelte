<script>
	import Navbar from '../$lib/components/Navbar.svelte';
	import Accueil from '../$lib/components/Accueil.svelte';
    import Pastille from '../$lib/components/Pastille.svelte';
    import Services from '../$lib/components/Services.svelte';
</script>

<section>
	<Navbar />
	<Accueil />
    <Pastille />
</section>

<Services />

<style>
    section {
        background: url('../$lib/assets/stylish-mesh-bg.jpg') no-repeat;
        background-size: cover;
        position: relative;
    }
</style>