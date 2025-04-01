<script lang="ts">
	import SecondaryButton from '../SecondaryButton.svelte';

	let { title, showLabel = false, details, button = '', image = '', reverseRow = false } = $props();
</script>

<div class="flex w-full {reverseRow ? 'flex-row-reverse' : ''} flex-row items-center">
	{#if image}
		<div class="flex basis-1/2 {reverseRow ? 'justify-end' : 'justify-start'} ">
			<img class="h-[572px] max-w-[500px]" src="/images/{image}.png" alt="auditories" />
		</div>
	{/if}
	<div class="basis-1/2 w-full">
		<div class="flex w-full flex-col">
			<div class="flex flex-row justify-between">
				<div class="flex flex-col">
					<p class="text-3xl font-semibold text-[#397A80]">{title}</p>
					<p class="font-light text-[#A1ADAF]">González Ruiz Auditores</p>
				</div>
				{#if showLabel}
					<div
						class="flex items-center rounded-xl border-2 border-[#397A80] px-5 text-2xl font-bold text-[#397A80]"
					>
						{title[0]}
					</div>
				{/if}
			</div>
			<hr class="bg-primary mt-8 h-0.5 border-0" />
			<p class="mt-8 text-justify leading-7 tracking-widest">{details}</p>
			<div class="mt-12 flex justify-center">
				{#if button.length}
					<SecondaryButton title={button} />
				{/if}
			</div>
		</div>
	</div>
</div>
