<script lang="ts">
	export let title: string;
	export let link: string;
	export let description: string;
</script>

<div class="max-w-xs space-y-2">
	<p class="text-lg font-bold">{title} | <a href={link}>link</a></p>
	<p>{description}</p>
</div>
