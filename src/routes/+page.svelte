<script>
	import NavHost from '../components/molecules/NavHost.svelte';
	import Hero from '../components/organisms/Hero.svelte';
	import About from '../components/organisms/About.svelte';
	import Art from '../components/organisms/Art.svelte';
	import Photos from '../components/organisms/Photos.svelte';
	import MoreWork from '../components/organisms/MoreWork.svelte';
	import Supporters from '../components/organisms/Supporters.svelte';
	import Footer from '../components/molecules/Footer.svelte';
</script>

<NavHost />
<main>
	<Hero />
	<About />
	<Art />
	<Photos />
	<MoreWork />
	<Supporters />
	<Footer />
</main>

<style lang="scss">
	main {
		width: 100%;
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
	}
</style>