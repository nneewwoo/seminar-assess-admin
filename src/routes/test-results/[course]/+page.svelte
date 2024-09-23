<script lang="ts">
	import { page } from '$app/stores';
	const { course } = $page.params;

	import { Courses } from '$lib/constants';
</script>

{#if !Courses.some((item) => item.id === course)}
	<h1>Course not found</h1>
{:else}
	<h1>Test Results for {course}</h1>
{/if}
