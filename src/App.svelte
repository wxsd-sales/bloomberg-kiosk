<script>
	import Booking from './Booking.svelte';
	import Branding from './Branding.svelte';
	import Controls from './Controls.svelte';
	import Dashboard from './Dashboard.svelte';
	import Apps from './Apps.svelte';
	import { theme$ } from './store';
	
	let themeVal;

	theme$.subscribe((theme) => {
		themeVal = theme;
	});

	const handleClick = () => {
		const html = document.getElementById('bloomberg');
		theme$.set(themeVal === 'dark' ? 'light' : 'dark');
		html.setAttribute('data-theme', themeVal);
	}
</script>

<button class="themeButton" on:click={handleClick}>{`${themeVal} Theme`}</button>
<main>
	<div class="grid">
		<div class="panel">
			<Branding />
			<Controls />
			<Booking />
		</div>
		<div class="panel" >
			<Dashboard />
			<Apps />
		</div>
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
	}

	.themeButton {
		position: absolute;
		right: 1.5rem;
		top: 1rem;
		width: 8rem;
	}

	.themeButton::first-letter{
		text-transform: capitalize;
	}

	.panel {
		height: 30rem;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>