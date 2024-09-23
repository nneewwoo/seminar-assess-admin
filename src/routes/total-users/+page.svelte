<script>
	let users = [
		{ id: 1, name: 'Alice' },
		{ id: 2, name: 'Bob' },
		{ id: 3, name: 'Charlie' }
	];
</script>

<main>
	<h1>Total Users: {users.length}</h1>
	<ul>
		{#each users as user}
			<li>{user.name}</li>
		{/each}
	</ul>
</main>

<style>
	main {
		font-family: Arial, sans-serif;
		padding: 1rem;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	li {
		background: #f4f4f4;
		margin: 0.5rem 0;
		padding: 0.5rem;
		border-radius: 4px;
		color: black;
	}
</style>
