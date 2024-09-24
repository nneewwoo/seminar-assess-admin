<script lang="ts">
	import { ConicGradient } from '@skeletonlabs/skeleton';
	import type { ConicStop } from '@skeletonlabs/skeleton';
	const conicStops: ConicStop[] = [
		{ color: 'rgba(255,255,255,1)', start: 0, end: 10 },
		{ color: 'rgba(255,255,255,0.5)', start: 10, end: 35 },
		{ color: 'rgba(255,255,255,0.25)', start: 35, end: 100 }
	];
</script>

<main>
	<br />
	<h1 class="dark:text-white text-black">Hello, Admin!</h1>
	<br />
	<div>
		<a href="tna-results"><ConicGradient stops={conicStops}><h1>RESULTS</h1></ConicGradient></a>
	</div>
	<br />
	<div class="logo-cloud grid-cols-1 lg:!grid-cols-3 gap-5">
		<a class="logo-item" href="total-users">
			<span>Total of users</span>
		</a>
		<a class="logo-item" href="tna">
			<span>TNA</span>
		</a>
		<a class="logo-item" href="tna-results">
			<span>TNA results</span>
		</a>
		<a class="logo-item" href="test">
			<span>Test</span>
		</a>
		<a class="logo-item" href="test-results">
			<span>Test Results</span>
		</a>
		<a class="logo-item" href="guest-speaker">
			<span>Guest Speaker</span>
		</a>
		<a class="logo-item" href="evaluation">
			<span>Evaluation</span>
		</a>
		<a class="logo-item" href="evaluation-results">
			<span>Evaluation Results</span>
		</a>
	</div>

	<button class="btn btn-sm variant-ghost-surface fixed bottom-4 right-4">Logout</button>
</main>

<style>
	h1 {
		font-size: 2rem;
	}
</style>
