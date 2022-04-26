<script>
	import Booking from './Booking.svelte';
	import Branding from './Branding.svelte';
	import Controls from './Controls.svelte';
	import Dashboard from './Dashboard.svelte';
	import Apps from './Apps.svelte';
	
	let themeVal = 'dark';
	
	function handleClick()  {
		const html = document.getElementById('bloomberg');
		themeVal = themeVal === 'dark' ? 'light': 'dark';
		html.setAttribute('data-theme', themeVal);
	}
</script>

<button class="themeButton" on:click={handleClick}>{`${themeVal} Theme`}</button>
<main>
	<div class="grid">
		<div>
			<Branding />
			<Controls />
			<Booking />
		</div>
		<div>
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
		margin-top: 3rem;
	}

	.themeButton {
		position: absolute;
		right: 1rem;
		top: 1rem;
		width: 8rem;
	}

	.themeButton::first-letter{
		text-transform: capitalize;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>