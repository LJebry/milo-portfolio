<script>
	import Social from '../atoms/Social.svelte';

	import { LinkedInIcon } from '@indaco/svelte-iconoir/linkedin';
	import { MailIcon } from '@indaco/svelte-iconoir/mail';
</script>

<div class="socials-container">
	<Social tip="LinkedIn" link="https://www.linkedin.com/in/milciades-boitel-2a3008351/">
		<LinkedInIcon color="var(--accent)" />
	</Social>

	<Social tip="milciadesboitel18@gmail.com" link="mailto:milciadesboitel18@gmail.com">
		<MailIcon color="var(--accent)" />
	</Social>
</div>

<style>
	.socials-container {
		display: flex;
		gap: 0.75rem;
	}
</style>
