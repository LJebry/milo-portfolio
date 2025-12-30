<script>
	import RichPresence from '../molecules/RichPresence.svelte';
	import Tooltip from '../atoms/Tooltip.svelte';

	// i didnt write this idk
	let getAge = () => {
		let birthDate = new Date('2004/03/13');
		const ageMs = Date.now() - birthDate.getTime();
		const preciseAge = (ageMs / 31536000000).toFixed(10);
		return preciseAge;
	};

	let age = getAge();
	setInterval(() => {
		age = getAge();
	}, 1000);
</script>

<section id="about" class="wrapper">
	<div>
		<RichPresence />
	</div>
	<div class="text">
		<h2>bio</h2>
		<p>
			Hey there, I'm <Tooltip tip="short for Milciades">
				<span>Milo!</span>
			</Tooltip> :] I'm a <Tooltip tip={age}><span>{Math.floor(Number(age))}</span></Tooltip>
			year old digital artist and designer based in New York. I’ve taken art seriously since
			<span>2017</span>, and have been doodling silly characters since <span>2020</span>. I also
			started to pivot into graphic design, which landed me to study at <Tooltip
				tip="Stay tuned for my graduation!"
			>
				<a
					href="https://www.citytech.cuny.edu/communication-design/"
					target="_blank"
					rel="noreferrer"
				>
					<span>CUNY City Tech</span>
				</a>
			</Tooltip>for Communication Design. In my free time, I like to do
			<Tooltip tip="commissions are open!">
				<!--
				TODO: change link to commission page (instagram)-->

				<a href="https://github.com/xafn" target="_blank" rel="noreferrer">
					<span>art commissions</span>
				</a>
			</Tooltip>
			and draw some of my favorite characters from games and shows I like. Thanks for stopping by!
		</p>
	</div>
</section>

<style lang="scss">
	@import '../../styles/mixins.scss';

	section {
		margin-bottom: 6rem;
		display: grid;
		gap: 4.5rem;
		grid-template-columns: 1fr 1fr;
		align-items: center;
	}

	.text {
		position: relative;
		line-height: 1.75rem;
	}

	span {
		font-weight: 400;
		font-family: var(--font-two);
		font-size: 0.9rem;
		background-color: var(--elevation-one);
		border-radius: 7px;
		color: var(--accent);
		padding: 0.2rem 0.5rem 0.2rem;
		width: fit-content;
	}

	a {
		text-decoration: none;
	}

	.text::before {
		@include outlineText(
			$content: 'afn',
			$translateX: 97%,
			$translateY: -5%,
			$fontSize: 300px,
			$opacity: 0.22
		);
	}

	h2 {
		display: none;
		margin-top: 1rem;
	}

	@media (max-width: 868px) {
		section {
			display: flex;
			flex-direction: column;
			align-items: normal;
		}

		h2 {
			display: block;
			margin-bottom: 1rem;
		}
	}
</style>
