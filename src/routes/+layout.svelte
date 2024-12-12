<script lang="ts">
	import '../app.css';
	import Navbar from '../components/Navbar.svelte';
	import Header from '../components/Header.svelte';
	const { children } = $props();
</script>

<div class="flex h-screen w-screen bg-gray-800">
	<Navbar />
	<div class="w-full h-full">
		<Header />
		<div class="mt-12 w-full p-12">
			{@render children()}
		</div>
	</div>
</div>
