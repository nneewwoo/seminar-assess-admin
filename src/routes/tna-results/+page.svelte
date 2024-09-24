<script lang="ts">
	import { ConicGradient } from '@skeletonlabs/skeleton';
	import type { ConicStop } from '@skeletonlabs/skeleton';
	const conicStops: ConicStop[] = [
		{ color: 'rgba(255,0,0,1)', start: 0, end: 15 },
		{ color: 'rgba(0,255,0,0.5)', start: 10, end: 35 },
		{ color: 'rgba(0,0,255,0.25)', start: 35, end: 100 }
	];
</script>

<br />
<h1>TNA Results</h1>
<br />
<div class="container">
	<div class="chart">
		<ConicGradient stops={conicStops}></ConicGradient>
	</div>
	<div>
		<h1>Pie Chart</h1>
		<p>
			The chosen option stands out as the favorite among users, showcasing their highest interest.
		</p>
	</div>
</div>

<style>
	h1 {
		font-size: 2rem;
	}

	.container {
		display: flex;
		align-items: center;
	}
	.chart {
		margin-right: 20px;
		margin-left: 20px;
	}
</style>
