<script lang="ts">
	import { page } from '$app/stores';
	const { course } = $page.params;

	import { Courses } from '$lib/constants';
	// const tableArr = [
	// 	{
	// 		name: 'John Doe',
	// 		'pre-test': 10,
	// 		'post-test': 90
	// 	},
	// 	{
	// 		name: 'Jane Doe',
	// 		'pre-test': 30,
	// 		'post-test': 20
	// 	},
	// 	{
	// 		name: 'John Smith',
	// 		'pre-test': 40,
	// 		'post-test': 50
	// 	}
	// ];
	// const total = tableArr.reduce((acc, curr) => acc + curr['post-test'], 0);
	// const total2 = tableArr.reduce((acc, curr) => acc + curr['pre-test'], 0);
</script>

{#if !Courses.some((item) => item.id === course)}
	<h1>Course not found</h1>
{:else}
	<h1>Test Results for {course}</h1>
{/if}

<!-- Responsive Container (recommended) -->
<div class="table-container">
	<!-- Native Table Element -->
	<table class="table table-hover">
		<thead>
			<tr>
				<th>Name</th>
				<th>Pre-test</th>
				<th>Post-test</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<!-- {#each tableArr as row, i}
					<tr>
						<td>{row.name}</td>
						<td>{row['pre-test']}</td>
						<td>{row['post-test']}</td>
					</tr>
				{/each} -->
			</tr>
		</tbody>
		<tfoot>
			<tr>
				<th colspan="3">Total</th>
				<!-- <td>{total2}</td>
				<td>{total}</td> -->
			</tr>
		</tfoot>
	</table>
</div>
