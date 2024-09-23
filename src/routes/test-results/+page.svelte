<script lang="ts">
	import { page } from '$app/stores';

	const url = $page.url;

	import { Courses } from '$lib/constants';
</script>

<br />
<h1>Test Results</h1>
<br />
<div class="flex gap-4">
	{#each Courses as course}
		<a href={`${url}/${course.id}`} class="btn variant-ghost">{course.name}</a>
	{/each}
</div>

<style>
	h1 {
		font-size: 2rem;
	}
</style>
