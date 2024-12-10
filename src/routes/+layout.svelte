<script lang="ts">
	import '../app.css';
	import Navbar from '../components/Navbar.svelte';
	const { children } = $props();
</script>

<div class="flex h-screen w-screen bg-gray-800">
	<Navbar />
	<div class="mt-12 w-full p-12">{@render children()}</div>
</div>
