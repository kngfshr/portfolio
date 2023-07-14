<script lang="ts">
	import '../app.css';
</script>

<div class="wrapper items-start md:items-center">
	<slot />
</div>

<style lang="postcss">
	.wrapper {
		@apply mt-16 md:mt-32 mb-4 mx-auto p-4 max-w-5xl;
		/* display: flex; */
		/* flex-direction: column; */
		min-height: 100vh;
	}
</style>
