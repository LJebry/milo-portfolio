<script>
	import PhotoGrid from '../../components/molecules/PhotoGrid.svelte';
	import Tooltip from '../atoms/Tooltip.svelte';
</script>

<section>
	<div class="wrapper" id="pw">
		<Tooltip tip="Click on a photo">
			<h2><span>photo</span>:work</h2>
		</Tooltip>
	</div>
	<PhotoGrid />
</section>

<style lang="scss">
	span {
		color: var(--accent);
	}

	h2 {
		display: inline-block;
		margin-bottom: 1rem;
	}

	div {
		display: flex;
		justify-content: center;
		margin-top: 0;

		@media (max-width: 868px) {
			justify-content: left;
			margin-bottom: 0.3rem;
		}
	}
</style>
