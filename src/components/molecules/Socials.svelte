<script>
	import Social from '../atoms/Social.svelte';

	import { LinkedInIcon } from '@indaco/svelte-iconoir/linkedin';
	import { MailIcon } from '@indaco/svelte-iconoir/mail';
	import { CoffeeCupIcon } from '@indaco/svelte-iconoir/coffee-cup';
</script>

<div class="socials-container">
	<Social tip="LinkedIn" link="https://www.linkedin.com/in/milciades-boitel-2a3008351/">
		<LinkedInIcon color="var(--accent)" />
	</Social>

	<Social tip="hey@afn.im" link="mailto:hey@afn.im">
		<MailIcon color="var(--accent)" />
	</Social>

	<Social tip="affan" link="https://ko-fi.com/affan">
		<CoffeeCupIcon color="var(--accent)" />
	</Social>
</div>

<style>
	.socials-container {
		display: flex;
		gap: 0.75rem;
	}
</style>
