<script lang="ts">
	let { label, textarea = false, type, value = $bindable('') } = $props();
</script>

<div class="flex w-full flex-col gap-2">
	<label class="text-sm font-medium text-[#397A80]" for="">{label}</label>
	{#if textarea}
		<textarea
			class="min-h-44 resize-none rounded-xl border-none bg-[#F3F3F3]"
			bind:value
			placeholder={label}
		></textarea>
	{:else}
		<input class="rounded-xl border-none bg-[#F3F3F3] min-h-12 placeholder:text-[#768485]" {type} bind:value placeholder={label} />
	{/if}
</div>
