<script lang="ts">
	import axios from 'axios';

	let email: string;
	let password: string;
	const getuser = async () => {
		const response = await axios.get('http://localhost:5173/api/user');
		return response.data;
	};
	const login = () => {
		// const response = await axios.post('/api/login', { email, password });

		console.log('LOGIN', email, password);
	};
</script>

<br />
<div class="flex justify-center items-center">
	<div>
		<h2>SEMINAR ASSESS ADMIN WEBSITE</h2>
	</div>
</div>
<div class="flex justify-center items-center h-screen">
	<div class="w-90 p-6 shadow-lg bg-slate-400 rounded-md">
		<h1>Login</h1>
		<hr class="mt-3" />
		<div class="mt-3">
			<label for="email" class="block">Email</label>
			<input
				type="email"
				id="email"
				bind:value={email}
				class="w-full p-2 border border-slate-300 rounded-md text-black"
				placeholder="Email"
			/>
			<label for="password" class="block mt-3">Password</label>
			<input
				type="password"
				id="password"
				bind:value={password}
				class="w-full p-2 border border-slate-300 rounded-md text-black"
				placeholder="Password"
			/>
			<div class="flex justify-center mt-4">
				<button on:click={login} type="submit" class="btn variant-ghost">Login</button>
			</div>
		</div>
	</div>
</div>
{#await getuser()}
	<div>Loading...</div>
{:then user}
	<div>{JSON.stringify(user)}</div>
{:catch error}
	<div>{error.message}</div>
{/await}

<style>
	h2 {
		font-size: 2rem;
	}
</style>
