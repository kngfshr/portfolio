<script lang="ts">
	import { AlertTriangle } from 'tabler-icons-svelte';
	import '../app.css';
</script>

<div class="relative isolate gap-x-6 bg-gray-50 px-6 py-2.5 sm:px-3.5">
	<p class="text-sm md:text-md leading-6 text-gray-900 text-center mx-auto">
		This site is under construction. We strongly believe in shipping fast and iterating faster!
	</p>
</div>

<div class="z-0 relative flex flex-col items-center py-24 px-4 md:px-24 w-screen overflow-x-hidden">
	<slot />
</div>
