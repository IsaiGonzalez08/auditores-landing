<script lang="ts">
	import SecondaryButton from '../SecondaryButton.svelte';

	let { title, showLabel = false, details, button = '', image = '', reverseRow = false } = $props();
</script>

<div
	class="flex w-full {reverseRow
		? 'lg:flex-row-reverse'
		: ''} items-center gap-5 md:gap-10 p-7 md:flex-col-reverse lg:flex-row lg:gap-0 lg:p-0"
>
	{#if image}
		<div class="hidden basis-1/2 md:flex {reverseRow ? 'justify-end' : 'justify-start'} ">
			<img class="md:h-[300px] md:w-[300px] md:rounded-2xl lg:rounded-none lg:h-[500px] lg:min-w-[500px]" src="/images/{image}.png" alt="auditories" />
		</div>
	{/if}
	<div class="w-full xl:basis-1/2 lg:p-6 xl:p-0">
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
			<p class="mt-8 text-justify text-sm tracking-widest sm:text-base sm:leading-7">{details}</p>
			<div class="mt-12 flex justify-center">
				{#if button.length}
					<SecondaryButton title={button} />
				{/if}
			</div>
		</div>
	</div>
</div>
