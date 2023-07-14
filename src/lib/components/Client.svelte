<script lang="ts">
	export let name: string;
	export let website: string;
	export let imageUrl: string;
</script>

<div class="max-w-xs space-y-2">
	<!-- Idea A: Just a simple image, click on it and it takes you to their website -->
	<a href={website} target="_blank" rel="noreferrer noopener">
		<img src={imageUrl} alt={name} />
	</a>
</div>
