<script>
	let email = '';
	let username = '';
	let password = '';
	let confirmPassword = '';
	let errorMessage = '';

	function handleSubmit() {
		if (username === 'educative' && password === 'educative') {
			errorMessage = '';
			alert('Login successful!');
			username = '';
			password = '';
		} else {
			errorMessage = 'Invalid username or password';
		}
	}
</script>

<main class="flex flex-col justify-center content-center">
	<h2 class="font-semibold">Signup</h2>
	{#if errorMessage}
		<p class="error">{errorMessage}</p>
	{/if}
	<form on:submit|preventDefault={handleSubmit}>
		<label for="email">Email:</label>
		<input type="text" id="email" bind:value={email} class="bg-white rounded-sm" />

		<label for="username">Username:</label>
		<input type="text" id="username" bind:value={username} class="bg-white rounded-sm" />

		<label for="password">Password:</label>
		<input type="password" id="password" bind:value={password} class="bg-white rounded-sm" />

		<label for="password">Confirm Password:</label>
		<input
			type="password"
			id="confirmPassword"
			bind:value={confirmPassword}
			class="bg-white rounded-sm"
		/>

		<button type="submit" class="rounded-md">Signup</button>
	</form>
</main>

<style>
	main {
		max-width: 300px;
		margin: 0 auto;
		text-align: center;
	}

	label {
		display: block;
		margin-top: 10px;
	}

	input {
		width: 100%;
		padding: 5px;
		margin-top: 5px;
	}

	button {
		margin-top: 10px;
		background-color: #007bff;
		color: white;
		border: none;
		padding: 10px 15px;
		cursor: pointer;
	}

	.error {
		color: red;
		margin-top: 10px;
	}
</style>
