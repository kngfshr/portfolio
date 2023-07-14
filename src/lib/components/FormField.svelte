<script lang="ts">
	export let id: string;
	export let label: string;
	export let placeholder: string = 'Type here';
	export let type: 'text' | 'url' = 'text';
	export let value: string = '';
</script>

<div class="form-control w-full max-w-xs">
	<label for={id} class="label">
		<span class="label-text">{label}</span>
	</label>
	<input
		id={`input_${id}`}
		{type}
		name={id}
		{placeholder}
		class="input input-bordered w-full max-w-xs"
		{value}
	/>
</div>
